# The Student Setup Guide

## Student Registration Process

```mermaid
graph TD
    A[Add Student] --> B[Edit Profile]
    B --> C[Personal Data]
    B --> D[Guardians: + Add Guardian]
    B --> E[Permanent Group Tags]
    B --> F[Academic Year: + Enrol]
    F --> G[Academic Enrolments: + Add Programme]
    G --> H[+ Add Subject]
```
### Add student

Register a new student by entering their First Name and Last Name. You may also provide their Gender, Date of Birth, and Email Address as optional fields.

### Edit profile
*   **Personal data**: This section allows you to review and update the student's core information previously entered during registration.
*   **Guardians**: This section allows you to register one or multiple guardians by providing their Full Name and Email Address.
!!! note "Assign a guardian to the student to enable progress report sharing"
*   **Permanent group tags**: Assign one or multiple permanent tags to the student. Tags assigned here are permanent and will apply across all enrolment years. Their use enables student group analysis for insights based on demographics or specific cohorts.
!!! note "Tags must be previously created in `Setup > Students > Tags`, clicking the ´Group tags` button"

#### Enrolment Process
![Setup Students](../assets/images/Setup_Students.png){ width="710" }
/// caption
Enrolment Process Flow
///
1.  **Academic Years**: Click on `+ Enrol` to associate the student with a specific Academic Year. This step is required to activate the student's record for the current cycle and enables their inclusion in specific year groups.
!!! success "Student must be enrolled in an Academic Year before assigning a Programme"
!!! warning "Review before saving"
    Please ensure the **Academic Year** and **Year Group** are correct. **These fields cannot be modified** once the enrolment is created.
2.  **Academic Enrolments**: Select `+ Add programme` to assign the student to a programme and enable subject enrolment.
3.  **Subjects**: To add subjects, open the Programme view and click the `+ Add subject button. The following form will appear:
![Setup Students](../assets/images/Setup_Students_Add_Subject.png){ width="450" }
/// caption
Adding Subject
///

Use the form to select the desired subject from the chosen programme's dropdown list, and then specify the academic year for the enrolment.
!!! note "Multiple academic years can be assigned to a single subject. This is useful when a subject spans two years or if a student requires additional time to complete the course."


!!! info "Finalizing Updates"
    To ensure all modifications in **Edit Profile** are successfully synchronized, you must click the **Done** button before navigating away.




