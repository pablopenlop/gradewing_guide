# The Student Setup Guide

## Student Registration Process


```mermaid
graph LR
    A([Add Student]) --> B[Edit Profile]
    
    subgraph Setup [Profile Details]
        B -.-> C(Personal Data)
        B -.-> D(Guardians)
        B -.-> E(Permanent Tags)
    end

    subgraph Enrolment [Enrolment Process]
        B --> F(Academic Year)
        F --> G(Programme)
        G --> H(Subjects)
    end

    C & D & E & H --- Z((Done))
    
    style Z fill:#fafafa,stroke:#bbb,stroke-width:1px,stroke-dasharray: 5 5
    style Setup fill:#f9f9f9,stroke:#eee,stroke-dasharray: 2 2
    style Enrolment fill:#fff,stroke:#eee
```
### Add student

![Setup Students](../assets/images/Setup_Students.png){ width="700" }


Click the `Add student` button to begin the registration process. Enter the student's First Name and Last Name into the corresponding form to create the record. You may also provide their Gender, Date of Birth, and Email Address as optional fields.

### Edit profile
*   **Personal data**: This section allows you to review and update the student's core information previously entered during registration.
*   **Guardians**: This section allows you to register one or multiple guardians by providing their Full Name and Email Address.
!!! note "Assign a guardian to the student to enable progress report sharing"
*   **Permanent group tags**: Assign one or multiple permanent group tags to the student. Tags assigned here are permanent and will apply across all enrolment years. Their use enables student group analysis for insights based on demographics or specific cohorts.
!!! note "Group tags must be previously created in `Setup > Students > Tags`, clicking the `Group tags` button"

#### Enrolment Process
![Setup Students](../assets/images/Setup_Students_Enrolment.png){ width="700" }

1.  **Academic Years**: Click on `+ Enrol` to associate the student with a specific Academic Year. This step is required to activate the student's record for the current cycle and enables their inclusion in specific year groups.

    !!! note "Student must be enrolled in an Academic Year before assigning a Programme"

    !!! warning "Review before saving"
        Please ensure the **Academic Year** and **Year Group** are correct. **These fields cannot be modified** once the enrolment is created.
    
    !!! info "Annual Group Tags"
        You can assign one or multiple tags to a student for a specific academic year. Unlike permanent tags, these are used to group students for academic purposes that may change from year to year.

    !!! info "Learner Statuses (Flags)"
        Assign one or multiple specific educational profiles to the student. These "flags" allow teachers and Data Managers to immediately identify and support specific student needs:

        *   **SEN (Special Educational Needs)**: The student has a learning difficulty or disability that requires special educational provision.
        *   **EAL (English as an Additional Language)**: The student's first language is not English and they may need support to access the curriculum.
        *   **LA (Low Attainer)**: The student is currently struggling to achieve the minimum expected academic standards for their level.
        *   **G&T (Gifted & Talented)**: The student demonstrates high ability in one or more academic, creative, or practical areas.
        *   **MP (Mobile Pupil)**: The student has joined the school outside the standard admission cycle or intake times.
        *   **OAGC (Out of Age Group Cohort)**: The student is not in the expected year group based on their chronological age.     

2.  **Academic Enrolments**: Select `+ Add programme` to assign the student to a programme and enable subject enrolment.

    !!! info "Add Programme"
        Within the form, you can select the most appropriate program for each student from the following options, organized by educational level:

        **Final Secondary (KS5)**

        *   **IB Diploma Programme**
        *   **GCE AS & A levels**
        *   **Level 3 Extended Project Qualifications**
        *   **International AS & A levels**
        *   **International Project Qualifications**
        *   **Other Pre-university (KS5) Programmes**

        **Upper Secondary (KS4)**

        *   **IB Middle Years Programme (Years 4–5)**
        *   **GCSEs**
        *   **Level 1 & 2 Project Qualifications**
        *   **International GCSEs**
        *   **O Levels**

        **Lower Secondary (KS3)**

        *   **International Lower Secondary Programme**


3.  **Subjects**: Locate the specific Programme section and click its corresponding `+ Add subject` button.

<table style="border: none; border-collapse: collapse; width: 100%; table-layout: fixed;">
  <tr style="border: none;">
    <td style="border: none; width: 50%; padding: 10px; text-align: center; vertical-align: top;">
      <img src="../../assets/images/Setup_Students_Add_Subject.png" class="glightbox" style="width: 100%; border-radius: 4px; border: 1px solid #eee;" alt="Subject Selection">
    </td>
    <td style="border: none; width: 50%; padding: 10px; text-align: center; vertical-align: top;">
      <img src="../../assets/images/Setup_Students_Add_Subject_Conf.png" class="glightbox" style="width: 100%; border-radius: 4px; border: 1px solid #eee;" alt="Enrolment Details">
    </td>
  </tr>
</table>

**Step 1: Selection**  
Use the dropdown in the first form to select the required subject. Each option in the list is a **unique entry** that already includes its specific **Examination Board** and **Curriculum System** (e.g., **Cambridge**, **Pearson/Edexcel**, **Oxford/AQA**, or **International Baccalaureate**). Click `Next` to proceed.

**Step 2: Configuration**  
In the final form, select the **Academic Year** and the **Enrolment Type**:

!!! info "Enrolment Types"
    *   **Standard Enrolment**: For students following the regular internal course.
    *   **Exam Only**: This option allows exam results to be recorded ***without creating an internal enrolment record***. It is an efficient way to manage subject qualifications earned outside the institution by incoming students.

!!! note "Multi-Year Enrolment"
    Multiple academic years can be assigned to a single subject. This is useful when a subject spans two years or if a student requires additional time to complete the course.

!!! warning "Finalizing the Profile"
    After completing all sections—including **Personal Data**, **Guardians**, **Group Tags**, and **Enrolments**—you must click the `Done` button to save and synchronize the entire student record.

### Group tags

![Setup Students](../assets/images/Setup_Students.png){ width="700" }


Click the `Group tags` button to create the specific tags required for your school. You can select one or multiple tags from the provided list or add your own custom labels. The standard categories include:

**Educational Needs**

*   **EAL**: English as an Additional Language.
*   **G&T / GIFTED**: Gifted and Talented students.
*   **IEP**: Individualized Education Program.
*   **SEN**: Special Educational Needs.

**Other Demographics**

*   **MOBILE**: Mobile Pupil (students joining outside the standard admission cycle).
*   **OAGC**: Out of Age Group Cohort.

!!! tip "Global Tags Setup"
    Setting up these **Group Tags** in `Setup > Students > Tags` ensures they are available as dropdown options when editing individual student profiles later.

---

## Practical Case Studies

Accurate student enrollment is the cornerstone of effective data management. Ensuring each student is correctly registered in the system is essential not only for assigning them to the appropriate **Teaching Groups** but also for:

1. **Academic Tracking:** Enabling the generation of **Expected Grades** and the scheduling of **Internal Grades**, including **Predicted**, **Attainment**, and **Target** grades.
2. **Examinations:** Managing the formal registration and recording of **Official Exam Results** once they are released by the awarding bodies.

The consistent effort of maintaining accurate student data—both personal details and enrollment—combined with the regular input of internal and external grades, empowers the school to:

*   **Deliver high-quality Progress Reports:** Generate automated and professional reports for students and parents.
*   **Track Individual Performance:** Analyze the current status and progress of every student in real-time.
*   **Monitor Subject & Cohort Trends:** Evaluate the evolution and academic health of specific subjects, year groups, or key stages.
*   **Measure Value-Added:** Analyze the progress made by students relative to their starting points and benchmark the school's performance against national or program averages.

---

### Case Study 1: Standard GCE AS & A-Level Pathway
*“Integrating linear subject tracking with a completed AS-Level and independent research certification.”*

#### **Profile Overview**
This case represents a high-standard academic profile in the UK curriculum. It demonstrates how the application manages a core set of **Linear A-Levels** (concluding in Year 13) alongside specific qualifications that follow different timelines.

*   **Core Academic Load:** 3 Linear GCE A-Levels (Physics, Maths, Computer Science) tracking progress over a 24-month cycle.
*   **Completed AS Level:** 1 Standalone GCE AS-Level (Further Maths) concluded and achieved at the end of Year 12.
*   **Independent Research:** 1 Extended Project Qualification (EPQ) used to enhance the student's academic profile for university entry.
*   **Native Language Accreditation:** 1 GCE A-Level (Spanish) managed as "Exam Only" to certify existing language proficiency without instructional overhead.

#### **Application Enrollment View**

| Subject title | Enrolled in |
| :--- | :--- |
| **GCE AS & A levels** | |
| AQA Level 3 Advanced GCE in Physics (7408) | 2025/26 – Year 13 <br> 2024/25 – Year 12 |
| AQA Level 3 Advanced GCE in Spanish (7692) | **Exam only** |
| OCR Level 3 Advanced GCE in Computer Science (H446) | 2025/26 – Year 13 <br> 2024/25 – Year 12 |
| Pearson Edexcel Level 3 Advanced GCE in Mathematics (9MA0) | 2025/26 – Year 13 <br> 2024/25 – Year 12 |
| Pearson Edexcel Level 3 Advanced Subsidiary GCE in Further Mathematics (8FM0) | 2024/25 – Year 12 |
| | |
| **Level 3 Extended Project Qualifications** | |
| Pearson Edexcel Level 3 Extended Project Qualification | 2025/26 – Year 13 |

#### **Key Considerations**

!!! info "Linear Subject Tracking"
    For linear subjects (`7408`, `9MA0`, `H446`), all grades recorded in the application (**Internal and Expected**) refer to the **entire qualification**. Since there is only one final exam, the system compares all grades against each other and against a **single Final Exam Grade**. This allows the application to track the student's overall progress and calculate the **Value-Added** provided by the school.

---
<!-- 
### Case Study 2: Cambridge International (CIE) Pathway
*“Managing Staged Assessment (AS + A2), Mandatory Linear subjects, and Student-Choice Linear entries.”*

#### **Profile Overview**
This case demonstrates the flexibility of the Cambridge curriculum. It tracks subjects following the standard "Staged" route alongside two types of Linear entries: those forced by the syllabus and those chosen by the student to be taken in a single exam series.

*   **Core Academic Load:** 2 Cambridge International A-Levels (Maths, Chemistry) using the standard **Staged Assessment** route (AS in Y12, A2 in Y13).
*   **Mandatory Linear Pathway:** 1 International A-Level (**French 9716**) which only allows a single exam sitting at the end of the 24-month cycle.
*   **Student-Choice Linear Pathway:** 1 International A-Level (**Computer Science 9618**) where the student sits both AS and A2 components in a single series at the end of Year 13.
*   **Completed AS Level:** 1 Standalone International AS-Level (Further Maths 9231) concluded in Year 12.
*   **External Accreditation:** 1 International A-Level (Law 9084) managed as "Exam Only."

#### **Application Enrollment View**


| Subject title | Enrolled in |
| :--- | :--- |
| **International AS & A levels** | |
| Cambridge International GCE A level in Chemistry (9701) | 2025/26 – Year 13 |
| Cambridge International GCE AS level in Chemistry (9701) | 2024/25 – Year 12 |
| **Cambridge International GCE A level in Computer Science (9618)** | 2025/26 – Year 13 |
| **Cambridge International GCE AS level in Computer Science (9618)** | 2025/26 – Year 13 |
| Cambridge International GCE A level in Mathematics (9709) | 2025/26 – Year 13 |
| Cambridge International GCE AS level in Mathematics (9709) | 2024/25 – Year 12 |
| Cambridge International GCE A level in French (9716) | 2025/26 – Year 13 <br> 2024/25 – Year 12 |
| Cambridge International GCE AS level in Further Mathematics (9231) | 2024/25 – Year 12 |
| Cambridge International GCE A level in Law (9084) | **Exam only** |
| Cambridge International GCE AS level in Law (9084) | **Exam only** |

#### **Key Considerations**

!!! info "Mandatory vs. Choice Linear Tracking"
    The application handles two Linear scenarios:
    1. **Mandatory Linear (French 9716):** The student is enrolled across both years, but the system expects a single final exam grade in Year 13.
    2. **Student-Choice Linear (Computer Science 9618):** Both AS and A-Level components are enrolled in **Year 13 only**. The system treats this as a single "all-in-one" assessment event.

!!! info "Staged Tracking"
    For **Staged** subjects (`9701`, `9709`), the application tracks **Year 12** and **Year 13** as two distinct academic events. The system benchmarks Year 12 internal grades against the **AS Exam Grade**, and Year 13 internal grades against the final **A-Level Exam Grade**.

---

### Case Study 3: International Modular Pathway (Pearson & OxfordAQA)
*“Tracking modular qualifications with multiple exam windows (January/June) and cumulative certification.”*

#### **Profile Overview**
This case represents the modular academic route, offering maximum flexibility in examination scheduling. It demonstrates how the application manages the transition between AS and A Level across modular boards like Pearson Edexcel and OxfordAQA.

*   **Modular Assessment:** 4 International Advanced Levels (IAL) where exams are completed unit-by-unit.
*   **Pearson Edexcel Transition:** A clear shift from the AS "X-code" in Year 12 to the A Level "Y-code" in Year 13.
*   **OxfordAQA Continuity:** A single-code system (`9620`) where the student certifies the AS in Year 12 and the A Level in Year 13 using the same subject identifier.
*   **Student-Choice Linear Sitting:** 1 IAL (**Spanish**) where the student has chosen to sit both AS and A2 units in a single exam series (Year 13), effectively treating a modular qualification as a linear one.
*   **Completed AS Level:** 1 Standalone International AS-Level (Further Maths `XFM01`) concluded in Year 12.

#### **Application Enrollment View**


| Subject title | Enrolled in |
| :--- | :--- |
| **International AS & A levels** | |
| OxfordAQA International A level in Chemistry (9620) | 2025/26 – Year 13 |
| OxfordAQA International AS level in Chemistry (9620) | 2024/25 – Year 12 |
| Pearson Edexcel International A level in Mathematics (YMA01) | 2025/26 – Year 13 |
| Pearson Edexcel International AS level in Mathematics (XMA01) | 2024/25 – Year 12 |
| Pearson Edexcel International A level in Physics (YPH11) | 2025/26 – Year 13 |
| Pearson Edexcel International AS level in Physics (XPH11) | 2024/25 – Year 12 |
| **Pearson Edexcel International A level in Spanish (YSP01)** | **2025/26 – Year 13** |
| **Pearson Edexcel International AS level in Spanish (XSP01)** | **2025/26 – Year 13** |
| Pearson Edexcel International AS level in Further Mathematics (XFM01) | 2024/25 – Year 12 |

#### **Key Considerations**

!!! info "Modular Certification (Cash-in) Tracking"
    The application treats Year 12 and Year 13 as two distinct certification events. Even if the code remains the same (**OxfordAQA**), the system expects an official **AS Exam Grade** at the end of Year 12 and an **A Level Exam Grade** at the end of Year 13 once the "cash-in" is processed.

---
-->

### Case Study 2: Advanced Multi-Board International Pathway
*“A comprehensive summary of international curricula: combining CIE, OxfordAQA, and Pearson Edexcel with accelerated and non-standard assessment routes.”*

#### **Profile Overview**
This case serves as a master reference for international centers. It demonstrates how the application unifies diverse assessment models (Staged, Modular, and Linear) into a single student record, including early certifications and independent research.

*   **Mixed Board Ecosystem:** Seamless integration of Cambridge (CIE), OxfordAQA, and Pearson Edexcel.
*   **Accelerated Completion:** 1 IAL (**Spanish**) fully completed in Year 12, providing early A-level achievement.
*   **Student-Choice Linear Sitting:** 1 A-Level (**IT 9626**) where both AS and A2 components are taken in Year 13.
*   **External Accreditation:** 1 A-Level (**Law 9084**) managed as an "Exam Only" entry for independent study.
*   **Research Certification:** 1 Cambridge International Project Qualification (**IPQ**) completed in Year 13.

#### **Application Enrollment View**


| Subject title | Enrolled in |
| :--- | :--- |
| **International AS & A levels** | |
| Cambridge International GCE A level in Media (9607) | 2025/26 – Year 13 |
| Cambridge International GCE AS level in Media (9607) | 2024/25 – Year 12 |
| OxfordAQA International A level in Economics (9640) | 2025/26 – Year 13 |
| OxfordAQA International AS level in Economics (9640) | 2024/25 – Year 12 |
| Pearson Edexcel International A level in Mathematics (YMA01) | 2025/26 – Year 13 |
| Pearson Edexcel International AS level in Mathematics (XMA01) | 2024/25 – Year 12 |
| **Pearson Edexcel International A level in Spanish (YSP01)** | **2024/25 – Year 12** |
| **Pearson Edexcel International AS level in Spanish (XSP01)** | **2024/25 – Year 12** |
| **Cambridge International GCE A level in Information Technology (9626)** | **2025/26 – Year 13** |
| **Cambridge International GCE AS level in Information Technology (9626)** | **2025/26 – Year 13** |
| Pearson Edexcel International AS level in Further Mathematics (XFM01) | 2024/25 – Year 12 |
| Cambridge International GCE A level in Law (9084) | **Exam only** |
| Cambridge International GCE AS level in Law (9084) | **Exam only** |
| | |
| **International Project Qualifications** | |
| Cambridge International Project Qualification | 2025/26 – Year 13 |

#### **Key Considerations**

!!! info "Mixed Assessment Logic"
    The application dynamically adapts to the specific board logic:
    *   **Staged (CIE/OxfordAQA):** Records the transition from Year 12 AS to Year 13 A-Level as linked exam events.
    *   **Accelerated (Spanish):** Archives final A-Level results achieved in Year 12 for ongoing reporting in Year 13.
    *   **Student-Choice Linear (IT):** Benchmarks both AS and A2 components against a single target in Year 13.

!!! info "Exam Only & Independent Projects"
    For **Law (9084)** and the **IPQ**, the system focuses on final outcome reporting. While the IPQ is a taught component, Law is excluded from internal Value-Added calculations to reflect its status as an external accreditation.

---
