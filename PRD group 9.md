## Product Requirements Document: ExamPass

## 1. Product Overview

ExamPass is an exam check-in and queue-management system designed for universities. Students receive assigned check-in windows and a digital e-tag (QR code and a printable digital pass) that speeds up exam hall entry and drastically cuts waiting times from hours down to minutes.

## 2. Problem Statement

Students often arrive hours early for exams, leading to long, chaotic lines because

check-ins are handled manually at the door without staggered arrival times. Specifically at Babcock University, students wait at the amphitheatre for hours just to write a 15 or 20 minutes exam. This issue wastes valuable study time, creates congestion and crowds at exam venues, and raises student stress levels before exams.

## 3. Business Objectives & Success Metrics

## Objectives

- Reduce average student check-in wait times by at least 75%.

- Maintain organized, controlled entry into exam halls and CBT centres.

- Show invigilators and exam staff who and when they are expected to arrive in real time.

## Success Metrics

- Average Student Wait Time: Target of under 10 minutes before check-in.

- Window Compliance: Percentage of students checking in within their assigned time window.

- Adoption Rate: Total number of active exam sessions managed by ExamPass.

- Scan Throughput: Average check-in scan speed per student at hall entrances.


## 4. Target Users & Stakeholders

- Target Users:

- Students: Taking exams and using e-tags to enter venues.

- Invigilators / Check-in Staff: Scanning student e-tags at hall entrances.

- Stakeholders: University Exams Office, Campus IT Department, University Academic department, Student Association, and Campus Security.

## 5. Scope & Priorities (MoSCoW)

- Must Have (MVP):

- Student login and authentication.

- Automatic or manual check-in window assignment.

- Unique digital e-tag generation (QR code).

- Invigilator e-tag scanner interface.

- Live check-in status dashboard.

## Should Have:

- Automated push/SMS reminder notifications prior to window opening.

- Late-arrival flagging and tagging.

## Could Have:

- Exam hall capacity system showing remaining available spaces.

- Exportable attendance logs and analytical reports.

## Won't Have (This Release):

- Biometric hardware integration.

- AI-driven seat assignment.

- Automated grading system integration.

## 6. User Stories & Acceptance Criteria

## User Story 1 (Getting an E-Tag)

As a student, I want to view my assigned check-in window and digital e-tag before my exam so that I don't show up hours early and waste time waiting in line.

## Acceptance Criteria:

- Student must be logged in with a verified student account.

- Assigned check-in window and scannable e-tag display clearly for each upcoming exam.


- E-tag explicitly displays student name, student ID, target exam hall, and designated check-in window.

- Invalid or expired sessions block access and present a clear user message.

## User Story 2 (Scanning at the Door)

As an invigilator, I want to scan a student's e-tag at the hall entrance so that I can verify their identity quickly and keep the line moving efficiently.

- Acceptance Criteria:

- Invigilators must also login and be authenticated with valid staff permissions.

- Scanning a valid e-tag marks the student as checked in and logs an accurate timestamp.

- Duplicate scans or e-tags scanned for the wrong exam trigger an immediate, alert on screen.

## User Story 3 (Configuring Exam Windows)

As an exam administrator, I want to set check-in window timeframes and capacity limits per exam session so that students arrive in manageable batches without crowding the entrance.

- Acceptance Criteria:

- Admin must be logged in with explicit exam-admin permissions.

- Window start/end times and batch limits must validate successfully before saving.

- System evenly distributes assigned students across available windows up to set limits.

- Setting changes auto-update student e-tags and send alerts when schedules shift.


## 7. Functional Requirements

| Requirement ID | Category | Description |
| --- | --- | --- |
| FR-01 | Student Portal | Students can log in and view |
|   |   | all scheduled exams. |
| FR-02 | Queue Engine | The system assigns |
|   |   | alternating check-in windows |
|   |   | based on total exam time and |
|   |   | target batch sizes. |
| FR-03 | E-Tag Engine | The system generates a |
|   |   | unique, adaptable e-tag for |
|   |   | each student per assigned |
|   |   | exam window. |
| FR-04 | Scanner Interface | Invigilators can scan e-tags |
|   |   | using a mobile camera or |
|   |   | web-based scanner interface |
|   |   | to record entry. |
| FR-05 | Administration | Exam administrators can set |
|   |   | up exam sessions, Set |
|   |   | window sizes, and monitor |
|   |   | real-time check-in numbers. |

## 8. Non-Functional Requirements

- Performance: E-tag scan verification must process and display results within 5 seconds under normal peak usage.

- Security: E-tags must use unique, secure tokens that can't be guessed, and all student data access must strictly follow role-based permissions.

- Reliability: Occasional network issues during scanning must not result in duplicate check-in records or lost scan data (offline sync required).

- Availability: The platform must ensure 99.9% functioning time throughout active university exam weeks.


## 9. Assumptions & Open Questions

## Assumptions

- Device Access: Students possess a personal smartphone or tablet capable of displaying their e-tag.

- Staff Equipment: Invigilators have access to a mobile device or tablet equipped with a working camera and internet connection.

## Open Questions

- 1. Out-of-Window Arrivals: How should the system handle students who arrive significantly outside their assigned check-in window?

- 2. Alternative Authentication: Should we support printed passes or a manual ID lookup in case a student's phone dies or they don't have a smart device?

- 3. Missed Window Policy: What happens if a student completely misses their assigned check-in window—should they be automatically reassigned to the next available slot, or directed to a separate backup queue?

*questions to be answered by team members
