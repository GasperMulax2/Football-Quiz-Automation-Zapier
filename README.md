# Football Quiz Auto-Grading Workflow

## Project Overview

This project demonstrates workflow automation using Zapier, Google Forms, Google Sheets, and JavaScript. The workflow automatically grades a football quiz, stores participant results, and sends personalized email feedback without requiring any manual intervention.

The goal of this project was to showcase automation, data processing, and workflow integration skills while creating a scalable solution for quiz management.

---

## Business Problem

Grading quiz responses manually can be time-consuming and inefficient, especially when dealing with multiple participants. This workflow automates the entire process from quiz submission to result delivery, reducing manual effort and improving response time.

---

## Workflow Architecture

```plaintext
Google Forms
      ↓
Zapier Trigger
      ↓
Code by Zapier (JavaScript)
      ↓
Google Sheets
      ↓
Personalized Email Notification
```

---

## Technologies Used

* Zapier
* Google Forms
* Google Sheets
* JavaScript (Code by Zapier)

---

## Workflow Process

### Step 1: Quiz Submission

Participants complete a General Football Quiz using Google Forms. The form collects:

* First Name
* Last Name
* Email Address
* Six football knowledge questions

---

### Step 2: Automated Grading Logic

A JavaScript code step inside Zapier grades each submission automatically.

The grading logic:

* Stores the correct answers for all six questions
* Converts user responses to lowercase
* Removes extra spaces using string trimming
* Compares responses against the answer key
* Counts correct and incorrect answers
* Calculates the final grade percentage

Grade Calculation:

```plaintext
Grade = (Correct Answers / Total Questions) × 100
```

---

### Step 3: Data Recording

After grading is complete, the results are automatically recorded in Google Sheets.

| Column     | Data                        |
| ---------- | --------------------------- |
| First Name | Participant First Name      |
| Last Name  | Participant Last Name       |
| Email      | Participant Email           |
| # Correct  | Number of Correct Answers   |
| # Wrong    | Number of Incorrect Answers |
| Grade %    | Final Score Percentage      |

This creates a structured dataset that can be used for reporting and analysis.

---

### Step 4: Personalized Email Notifications

Once the results are recorded, Zapier automatically sends a personalized email to each participant containing:

* Personalized greeting
* Correct answers count
* Incorrect answers count
* Final grade percentage
* Encouragement message

---

## Key Features

* Automated grading with no manual review required
* Case-insensitive answer matching
* Whitespace trimming to improve accuracy
* Instant score calculation
* Real-time email notifications
* Centralized data storage in Google Sheets
* Easily scalable for additional questions

---

## Example Results

| Correct Answers | Wrong Answers | Grade |
| --------------- | ------------- | ----- |
| 6               | 0             | 100%  |
| 5               | 1             | 83.3% |
| 3               | 3             | 50.0% |

---

## Sample Email Output

```plaintext
Hi Gasper,

Thank you for taking the General Football Quiz!

Quiz Score Report
--------------------------------

Correct Answers: 6/6
Wrong Answers: 0/6
Your Grade: 100%

We appreciate your participation. Keep practicing and try again to improve your score!

Best regards,
The Quiz Team
```

---

## Skills Demonstrated

* Workflow Automation
* Process Optimization
* Data Collection
* Data Validation
* JavaScript Logic
* Spreadsheet Automation
* Zapier Integrations
* Business Process Improvement

---

## Future Improvements

* AI-generated quiz feedback
* Interactive performance dashboard
* Additional quiz categories
* Automated reporting and analytics
* Enhanced answer validation
