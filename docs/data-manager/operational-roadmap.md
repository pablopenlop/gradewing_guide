# The Data Manager’s Operational Roadmap


## Phase 1: Initial Setup
Initial setup tasks required before the start of the academic cycle
### 1.1 School Details

### 1.2 Year Groups

Navigate to: `Setup > School > Year Groups` to manage year groups.

A Year Group represents a cohort of students in the same academic grade. Gradewing supports a standard seven-year structure, typically ranging from Year 7 to Year 13 (or local equivalents).
You can rename year groups at any time to match your school’s terminology.

Internal grading, student progress reports, and other features operate at year group level.

### 1.2 Academic Year

Navigate to: `Setup > Academic years` to add or manage academic years.

An *Academic Year* defines the school’s annual cycle, typically spanning from September to July.
It serves as the foundational organizational structure for most  academic data.

#### Multi-Year Continuity: 
Gradewing supports the creation of additional consecutive academic years at any time, all while maintaining the integrity and accessibility of historical data.

!!! note "Understanding Academic Year relationships"
    Student and Teacher records **transcend** individual academic years. They are linked to academic years through their enrolments.

    However: Teaching groups, pastoral groups, internal grading moments and student progress reports are tied to a **sole** academic year.


### 1.4 Custom subjects

Navigate to: `Setup > Custom subjects` to create or manage custom subjects.

 Any subject that is **not** included in our **Subject Qualification Repository** should be set up as a custom subject.
 For additional guidance and best practices, please refer to the [Custom Subjects Guide](data-manager/custom-subjects.md).  

<!-- !!! question "What is a custom subject?"
    Custom subjects are subjects that are not included in our default subject repository.
    Any subject without external assessment that does not lead to a qualification is considered a custom subject.
    For example, an IB MYP subject without an External Assessment is considered a custom subject.
    All KS3 subjects (pre-GCSE) are also considered custom subjects.


!!! question "What "
    Any subject that is **not** included in our **Subject Qualification Repository** should be set up as a custom subject. -->

!!! note "Custom Subjects are optional"
    If all your subjects are included in our default subject repository, you do not need to create any custom subjects.

## Phase 2: Populating the System

### 2.1 Students & Enrolments

Navigate to: `Setup > Students` to create student records and manage enrolments.

Student creation includes:

- academic year enrolments and subject enrolments
- group tags and learner statuses for enhanced analysis and tracking.
- guardian contact information to enable effective report sharing.

!!! danger "Critical setup task you should master"
    We recommend you read the [Student Setup Guide](data-manager/student-setup.md) to ensure a smooth and efficient setup process. 


For guidance and tips on managing students, please refer to the [Student Setup Guide](data-manager/student-setup.md).

### 2.2 Teachers

Navigate to: `Setup > Teachers` to create and manage teacher records.

The term *Teacher* refers to all Academic Staff––not just subject teachers. 

Teaching and pastoral groups must be assigned to existing teacher records during creation.
Linking a Teacher record to a User account grants the User access and responsibility for the academic data of their assigned groups.


### 2.3 Teaching Groups 

Navigate to: `Setup > Teaching groups` to create and manage teaching groups.

Teaching groups connect Students with their Subject Teachers during a given academic year.
Only students assigned to teaching groups are eligible to receive internal grades and appear in progress reports.

!!! success "Teaching Groups are essential"

    Each student should be assigned to **at least one** teaching group for each subject they are enroled in.

A student may be assigned to multiple teaching groups for a given subject.
A teaching group can be co-taught by multiple teachers, and include students from different year groups.
For additional guidance and best practices, please refer to the [Teaching Groups Setup Guide](data-manager/teaching-groups-setup.md).



### 2.4 Pastoral Groups

Navigate to: `Setup > Pastoral groups` to create and manage pastoral groups.

Pastoral groups are tutor (form) groups, advisory groups, enrichment groups, support groups, and any other type of pastoral grouping implemented in your school. 

Pastoral Groups link students with their assigned Pastoral Teachers, and allow these students to receive pastoral comments and other information in Student Progress reports.

!!! note "Teaching Groups vs Pastoral Groups"

    Teaching groups are formally associated to a subject with grading, whereas Pastoral Groups are not. 

A student may be assigned to multiple pastoral groups.
For guidance and best practices, please refer to the [Pastoral Groups Setup Guide](data-manager/teaching-groups-setup.md).

### 2.5 User Accounts & Permissions

Navigate to: `Admin > Users` to manage user accounts and permissions.

User accounts are required for staff to access the system and perform their roles.
Permissions are automatically assigned based on the user’s role (Teacher, Leadership, Data Manager or Admin).

Each User account should be **linked to a unique Teacher record** to ensure proper access and responsibility for academic data. Deleting a Teacher record will not deactivate the linked User account, and vice versa.

<!-- !!! success "User & Teacher linkage"
    Each User account should be linked to a unique Teacher record to ensure proper access and responsibility for academic data. Deleting a Teacher record will not deactivate the linked User account, and vice versa. -->


!!! danger "Data Manager accounts"
    Data Manager access should be granted only to a limited number of trusted staff members. Users with this permission have **full editing and deletion access** within the system.

## Phase 3: Grading

There are three distinct grading environments in Gradewing, each with its own setup and management process:
Examination results, Expected grades, and Internal grading moments.

### 3.1  Examination Results 
Navigate to: `Setup > Examinations` to record official examination results.

Examination results can be recorded for any subject found in our Subject Qualification Repository.
The Examination Gradebook meets the specific grading needs of each subject, including the recording of component / unit results for linear and modular qualifications.


!!! question "Why record Examination Results?"
    Recording exam grades in Gradewing allows you to:

    1. **Run (Value-Added) Analysis**: Evaluate examination outcomes against Expected Grades,  internal grades and standard benchmarks.
    2. **Confidently Set Expected Grades**: Gradewing automatically suggests Expected Grades for KS5 (A-level or IB DP) subjects based on KS4 exam data.
    3. **Maintain a Structured Examination Record**: At no extra cost.



### 3.2  Expected Grades 
Navigate to: `Setup > Expected grades` to set up and manage expected grades.

Expected grades are **statistical predictions** of student (final) attainment, based on **prior attainment or baseline assessments**.
Expected grades are typically set at the start of the academic year.

Gradewing provides a chances table via GEM (Grades Expectations Model) a data-grounded setting for KS5 (A-level or IB DP) subjects based on KS4 exam results. AI analyst to help you set the correct expected grade





!!! question "Why record Expected Grades?"
    They serve as benchmarks for student performance and form the baseline of **Value-Added** analysis.
     Progress vs. Expected grades can also be showcased in Student Progress reports.
  


### 3.3  Internal Grading Moments & Gradebooks

Navigate to: `Setup > Grading moments` to create and manage internal grading moments.
Internal grading moments are custom assessment points defined by the school, such as mock exams, end-of-term assessments, or any other internal evaluation.
### 3.4  Grade Entry & Management

## Phase 4: Reporting 

### 4.1  Report Generation

### 4.2  Report Management & Distribution

