# Deploying Software

## GitFlow: Branching and Deployment Strategy


![Image title](assets/images/GitFlow.png){ width="570" }
#### **Main Branch**
Known as **`main`**, it is a permanent branch and is only updated whenever a new software version is promoted to Production from the **Release** or **Hotfix** branch. Each new version is always associated with a **Tag** corresponding to a **Docker Image**.

#### **Develop Branch**
Known as **`dev`**, it is a permanent branch where continuous work is performed. Commits are made as needed until a new version of the Gradewing software is ready for deployment to **Stage**.

#### **Release Branch**
This is a temporary branch called **`Release`**. Commits are **never** made directly to this branch.

*   It is created via "**New Branch**" in GitHub, using **`dev`** as the source branch.
*   Using the software included in this branch, a **deployment to Stage** is performed from the Hetzner terminal, where the new software will be exhaustively tested.
*   Once the software is certified, a **Tag** is applied, and the corresponding **Docker Image** is labeled.
*   Using this tagged Docker Image, the **deployment to Production** is carried out (without a new build).
*   Next, a **merge** is performed within the Hetzner terminal from the **`Release`** branch into **`main`**. At this point, the three branches are leveled (excluding any commits made to `dev` after the `Release` branch was created).
*   Finally, the temporary **`Release`** branch is deleted from both Hetzner and GitHub, leaving only the two permanent branches: **`dev`** and **`main`**.

#### **Hotfix Branch**
This is a temporary and exceptional branch called **`Hotfix`**. Usually, only a single commit is made on this branch to push an urgent fix to Production.

*   It is created via "**New Branch**" in GitHub, using **`main`** as the source branch.
*   Using the software included in this branch, an **urgent deployment to Stage** is performed from the Hetzner terminal to verify the hotfix.
*   Once verified, a **Tag** is applied, and the corresponding **Docker Image** is labeled.
*   Using this tagged Docker Image, the **deployment to Production** is carried out (without a new build).
*   Next, a **double merge** is performed within the Hetzner terminal from the **`Hotfix`** branch into both **`main` and `dev`**. This ensures that both `Hotfix` and `main` branches are leveled (noting that `dev` may have accumulated many previous commits).
*   Finally, the temporary **`Hotfix`** branch is deleted from both Hetzner and GitHub, leaving only the two permanent branches: **`dev`** and **`main`**.


## Stage Deployment of a **New Software Version**

#### 1. Creation of a new Release branch on GitHub
*   **Create new Branch**
*   **New Branch name:** Release
*   **Source:** dev

#### 2. Connection to Hetzner and positioning in Gradewing from the terminal

First, log in via SSH to the server:
```bash
ssh root@46.62.132.133
```
```bash
cd gradewing
```
```bash
cd gradewing
```

!!! note "Once you are positioned at root@gradewing-server:~/gradewing/gradewing#, you can run the necessary commands to deploy the software from GitHub"

#### 3. Localizing the software from the Release branch on the Hetzner server

```bash
git fetch origin
```
```bash
git checkout Release
```
```bash
git reset --hard HEAD
```
```bash
git pull origin Release
```

#### 4. Execution permissions

```bash
chmod +x ./run/*.sh
```

#### 5.1 Deployment to Stage of the new branch software already localized in Hetzner (keeping current data)

```bash
./run/03-start_staging.sh
```

#### 5.2 Deployment to Stage by deleting current data and, optionally, loading Production data

```bash
./run/04-stop_staging.sh
```
```bash
./run/03-start_staging.sh
```
!!! tip "Depending on the magnitude of the changes made, it might be advisable to replicate the Production data so as not to start with an empty environment."
```bash
./run/21-restore_to_staging.sh
```

#### 6. Stage Environment Verification

!!! note "By executing a single command, we verify the deployment in Stage (see Appendix I)."
```bash
check-stage				# -- VERIFICATION
```

## Production Deployment of a **New Software Version** certified in Stage


#### 1. Connection to Hetzner and positioning in Gradewing from the terminal

First, log in via SSH to the server:
```bash
ssh root@46.62.132.133
```
```bash
cd gradewing
```
```bash
cd gradewing
```
!!! note "Once you are positioned at root@gradewing-server:~/gradewing/gradewing#, you can run the necessary commands to deploy the software from GitHub"

#### 2. Execution permissions

```bash
chmod +x ./run/*.sh
```

#### 3. Docker Image Tagging (Image: `gradewing-web:vn.n`) and software on GitHub (Tag: `vn.n`)

!!! tip "This script identifies the most recent 'gradewing-web' image. Calculate a new version by adding 1 to the first digit, and use it in the posterior tagging script."

```bash
docker images --format "{{.Tag}}\t{{.CreatedSince}}" gradewing-web | grep "^v"   # -- VERIFICATION
```
```bash
./run/10-tag_web.sh
```

!!! note "Just in case."

```bash
docker images --format "{{.Tag}}\t{{.CreatedSince}}" gradewing-web | grep "^v"   # -- VERIFICATION
```

#### 4. Deployment of the tagged Docker image to Production (without Build)

```bash
./run/05-start_production.sh
```

#### 5. Production Environment Verification

!!! note "With a single command, we verify the deployment in Production (see Appendix II)."

```bash
check-prod				# -- VERIFICATION
```

#### 6. Merge into **main** from the **Release** branch, and deletion of said branch in Hetzner and GitHub

```bash
git fetch origin
```
```bash
git checkout main
```
```bash
git pull origin main
```

!!! info "The terminal should have shown: * branch main -> FETCH_HEAD - Already up to date"

```bash
git merge Release
```
```bash
git diff main..origin/Release			# -- VERIFICATION
```
!!! info "Nothing should have been displayed on the terminal"

```bash
git push origin main
```
```bash
git diff origin/main..origin/Release			# -- VERIFICATION
```
!!! info "Nothing should have been displayed on the terminal"

```bash
git log main..origin/dev --oneline			# -- VERIFICATION
```
!!! info "Pending commits from the dev branch will be displayed"

```bash
git branch -d Release
```
```bash
git push origin --delete Release
```

#### 7. Verification of branch status in Hetzner and GitHub

```bash
git branch -a				# -- VERIFICATION
```

!!! info "Correct state of the branches"
    **main** - remotes/origin/HEAD -> origin/main - remotes/origin/dev - remotes/origin/main

## Production Deployment of a **Hotfix**

#### 1. Creation of a new Release branch on GitHub
*   **Create new Branch**
*   **New Branch name:** Hotfix
*   **Source:** main

!!! warning "The software is modified within the **Hotfix** branch on GitHub, and the corresponding commit is made so that the changes can be later pulled into the Hetzner server."

#### 2. Connection to Hetzner and positioning in Gradewing from the terminal

First, log in via SSH to the server:
```bash
ssh root@46.62.132.133
```
```bash
cd gradewing
```
```bash
cd gradewing
```

!!! note "Once you are positioned at root@gradewing-server:~/gradewing/gradewing#, you can run the necessary commands to deploy the software from GitHub"

#### 3. Localizing the software from the Hotfix branch on the Hetzner server

```bash
git fetch origin
```
```bash
git checkout Hotfix
```
```bash
git reset --hard HEAD
```
```bash
git pull origin Hotfix
```

#### 4. Execution permissions

```bash
chmod +x ./run/*.sh
```

#### 5.1 Deployment to Stage of the new branch software already localized in Hetzner (keeping current data)

```bash
./run/03-start_staging.sh
```

#### 5.2 Deployment to Stage by deleting current data and, optionally, loading Production data

```bash
./run/04-stop_staging.sh
```
```bash
./run/03-start_staging.sh
```
!!! tip "Although** improbable, it might be advisable to replicate **Production data** to avoid starting with an empty environment."

```bash
./run/21-restore_to_staging.sh
```

#### 6. Stage Environment Verification

!!! note "By executing a single command, we verify the deployment in Stage (see Appendix I)."
```bash
check-stage				# -- VERIFICATION
```


#### 7. Docker Image Tagging (Image: `gradewing-web:vn.n`) and software on GitHub (Tag: `vn.n`)

!!! tip "This script identifies the most recent 'gradewing-web' image. Calculate a new version by adding 1 to the second digit, and use it in the posterior tagging script."

```bash
docker images --format "{{.Tag}}\t{{.CreatedSince}}" gradewing-web | grep "^v"   # -- VERIFICATION
```
```bash
./run/10-tag_web.sh
```

!!! note "Just in case."

```bash
docker images --format "{{.Tag}}\t{{.CreatedSince}}" gradewing-web | grep "^v"   # -- VERIFICATION
```

#### 8. Deployment of the tagged Docker image to Production (without Build)

```bash
./run/05-start_production.sh
```

#### 9. Production Environment Verification

!!! note "With a single command, we verify the deployment in Production (see Appendix II)."

```bash
check-prod				# -- VERIFICATION
```

#### 10. Merge into **main** and **dev** from the **Hotfix** branch, and deletion of said branch in Hetzner and GitHub

```bash
git fetch origin
```
```bash
git checkout main
```
```bash
git pull origin main
```
```bash
git merge Hotfix
```
```bash
git diff main..origin/Hotfix			# -- VERIFICATION
```
```bash
git push origin main
```
```bash
git diff origin/main..origin/Hotfix			# -- VERIFICATION
```
```bash
git checkout dev
```
```bash
git pull origin dev
```
```bash
git merge Hotfix
```
```bash
git diff dev..origin/Hotfix				# -- VERIFICATION
```
```bash
git push origin dev
```
```bash
git diff origin/dev..origin/Hotfix			# -- VERIFICATION
```
```bash
git log main..origin/dev --oneline			# -- VERIFICATION
```
```bash
git branch -d Hotfix
```
```bash
git push origin --delete Hotfix
```

#### 11. Verification of branch status in Hetzner and GitHub

```bash
git branch -a				# -- VERIFICATION
```

## Production Disaster Recovery: Deploying a previous software version while preserving data

!!! danger "Critical Disaster Recovery"
    This procedure must **ONLY** be used in the event of a critical failure in the current Production version. The objective is to perform a **Rollback** to a stable previous version while strictly **preserving the existing database**.

#### 1. Connection to Hetzner and positioning in Gradewing from the terminal

First, log in via SSH to the server:
```bash
ssh root@46.62.132.133
```
```bash
cd gradewing
```
```bash
cd gradewing
```

!!! note "Once you are positioned at root@gradewing-server:~/gradewing/gradewing#, you can run the necessary commands to deploy a stable previousversion."

#### 1. Deploying an older Docker Image

!!! info "Any of the five previous Docker Images, which were previously used in the Production environment, can be redeployed without altering the data.""

```bash
./run/05-start_production.sh
```
```bash
docker ps --format "table {{.Names}}\t{{.Image}}\t{{.Status}}"		# -- VERIFICATION
```

#### 2. Production Environment Verification

!!! note "With a single command, we verify the deployment in Production (see Appendix II)."

```bash
check-prod				# -- VERIFICATION
```

## Appendix I: Command to create the `check-stage` alias

To simplify the verification of the Stage environment, we use a custom alias that checks build status, images, resources, network, database migrations, Redis, and logs in a single execution.

#### Installation

Run the following command in your Hetzner terminal to add the alias to your `~/.bashrc` and activate it:

```bash
echo "alias check-stage='echo \"\n🔨 --- 1. BUILD STATUS & IMAGE ID ---\" && docker images | grep staging && echo \"\n🧹 --- 2. DANGLING IMAGES (Build Junk) ---\" && docker images -f \"dangling=true\" || echo \"No junk images\" && echo \"\n📊 --- 3. STAGING RESOURCES ---\" && docker stats --no-stream | grep staging && echo \"\n🌐 --- 4. STAGING NETWORK ---\" && docker network ls | grep staging && echo \"\n🧼 --- 5. STAGING DB & REDIS ---\" && docker exec GradewingDjango_staging python manage.py showmigrations | grep \"\[ \]\" || echo \"All migrated in Stage\" && docker exec GradewingDjango_staging python manage.py shell -c \"from django.core.cache import cache; cache.set('\''test'\'', '\''ok'\'', 5); print('\''Redis Stage Status:'\'', cache.get('\''test'\''))\" && echo \"\n⚠️ --- 6. BUILD & RUN LOGS ---\" && docker compose -f docker-compose.staging.yml logs --tail=50 | grep -Ei \"error|critical|fail\" || echo \"No errors in Staging\"'" >> ~/.bashrc && source ~/.bashrc
```
## Appendix II: Command to create the `check-prod` alias

To ensure the Production environment is running correctly, this custom alias performs a comprehensive check of versions, resources, storage, and database health in a single command.

#### Installation

Run the following command in your Hetzner terminal to add the alias to your `~/.bashrc` and activate it:

```bash
echo "alias check-prod='echo \"\n🚀 --- 1. STATUS & VERSIONS ---\" && docker ps --filter \"name=production\" --format \"table {{.Names}}\t{{.Status}}\t{{.Image}}\" && echo \"\n📦 --- 2. DOCKER IMAGES (v1.1.4 check) ---\" && docker images | grep -E \"REPOSITORY|v1.1.4|staging\" && echo \"\n📊 --- 3. RESOURCE USAGE (Stats) ---\" && docker stats --no-stream && echo \"\n🌐 --- 4. NETWORK ISOLATION ---\" && docker network ls | grep gradewing && echo \"\n💾 --- 5. DISK SPACE (Server) ---\" && df -h / && echo \"\n📂 --- 6. DOCKER SYSTEM DF ---\" && docker system df && echo \"\n🧼 --- 7. REDIS & MIGRATIONS ---\" && docker exec GradewingDjango_production python manage.py showmigrations | grep \"\[ \]\" || echo \"All migrated\" && docker exec GradewingDjango_production python manage.py shell -c \"from django.core.cache import cache; cache.set('\''test'\'', '\''ok'\'', 5); print('\''Redis Status:'\'', cache.get('\''test'\''))\" && echo \"\n⚠️ --- 8. ERRORS (Last 100 lines) ---\" && docker compose -f docker-compose.production.yml logs --tail=100 | grep -Ei \"error|critical|fail\" || echo \"No critical errors found\"'" >> ~/.bashrc && source ~/.bashrc
```









