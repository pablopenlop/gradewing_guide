# Deploying Software

## Git Flow: Branching and Deployment Strategy


![Image title](assets/images/GitFlow.png){ width="700" }


### **Main Branch**
Known as **`main`**, it is a permanent branch and is only updated whenever a new software version is promoted to Production from the **Release** or **Hotfix** branch. Each new version is always associated with a **Tag** corresponding to a **Docker Image**.

### **Develop Branch**
Known as **`dev`**, it is a permanent branch where continuous work is performed. Commits are made as needed until a new version of the Gradewing software is ready for deployment to **Stage**.

### **Release Branch**
This is a temporary branch called **`Release`**. Commits are **never** made directly to this branch.

*   It is created via "**New Branch**" in GitHub, using **`dev`** as the source branch.
*   Using the software included in this branch, a **deployment to Stage** is performed from the Hetzner terminal, where the new software will be exhaustively tested.
*   Once the software is certified, a **Tag** is applied, and the corresponding **Docker Image** is labeled.
*   Using this tagged Docker Image, the **deployment to Production** is carried out (without a new build).
*   Next, a **merge** is performed within the Hetzner terminal from the **`Release`** branch into **`main`**. At this point, the three branches are leveled (excluding any commits made to `dev` after the `Release` branch was created).
*   Finally, the temporary **`Release`** branch is deleted from both Hetzner and GitHub, leaving only the two permanent branches: **`dev`** and **`main`**.

### **Hotfix Branch**
This is a temporary and exceptional branch called **`Hotfix`**. Usually, only a single commit is made on this branch to push an urgent fix to Production.

*   It is created via "**New Branch**" in GitHub, using **`main`** as the source branch.
*   Using the software included in this branch, an **urgent deployment to Stage** is performed from the Hetzner terminal to verify the hotfix.
*   Once verified, a **Tag** is applied, and the corresponding **Docker Image** is labeled.
*   Using this tagged Docker Image, the **deployment to Production** is carried out (without a new build).
*   Next, a **double merge** is performed within the Hetzner terminal from the **`Hotfix`** branch into both **`main` and `dev`**. This ensures that both `Hotfix` and `main` branches are leveled (noting that `dev` may have accumulated many previous commits).
*   Finally, the temporary **`Hotfix`** branch is deleted from both Hetzner and GitHub, leaving only the two permanent branches: **`dev`** and **`main`**.


## Stage Deployment of a **New Software Version**

### 1. Creation of a new Release branch on GitHub
*   **Create new Branch**
*   **New Branch name:** Release
*   **Source:** dev

### 2. Connection to Hetzner and positioning in Gradewing from the terminal

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





