# The Data Manager’s Operational Roadmap


## Phase 1: Initial Setup
Initial setup tasks required before the start of the academic cycle.
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

!!! success "User & Teacher linkage"
    Each User account should be linked to a unique Teacher record to ensure proper access and responsibility for academic data. Deleting a Teacher record will not deactivate the linked User account, and vice versa.


!!! danger "Data Manager accounts"
    Data Manager access should be granted only to a limited number of trusted staff members. Users with this permission have **full editing and deletion access** to all data within the system.

## Phase 3: Grading

### 3.1  Examination Results 

### 3.2  Expected Grades 

### 3.3  Internal Grading Moments & Gradebooks

### 3.4  Grade Entry & Management

## Phase 4: Reporting 

### 4.1  Report Generation

### 4.2  Report Management & Distribution

