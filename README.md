# Meeting-Notes Q&A Assistant

## Project Overview

The **Meeting-Notes Q&A Assistant** is an AI-assisted project management solution that uses meeting transcripts to answer questions about project owners, decisions, deadlines, risks, budgets, testing, training, and project progress.

The project uses **Google NotebookLM** to analyze 15 fictional project meeting transcripts and provide source-grounded answers.

## Problem Statement

Project information is often distributed across multiple meeting notes, making it difficult to quickly identify:

- Who is responsible for a task
- Important project decisions
- Deadlines and follow-up dates
- Current project risks and issues
- Budget and vendor-related concerns
- Testing and implementation progress
- Training and approval requirements
- Final project status

This project demonstrates how an AI-assisted meeting-notes system can make this information easier to retrieve, organize, and verify.

## Objectives

1. Create a structured dataset of 15 fictional project meeting transcripts.
2. Load the transcripts into Google NotebookLM.
3. Design and record AI-use questions related to project management information.
4. Verify NotebookLM responses against the original meeting transcripts.
5. Generate a consolidated project-status summary.
6. Identify potential owner/date inconsistencies and determine whether they are genuine errors or documented changes.

## Dataset

The dataset contains **15 fictional project meetings**, identified as **MTG001–MTG015**, covering April–July 2025.

The meetings cover topics such as:

- Campus hiring
- CRM migration
- Q3 sales reviews
- Vendor consolidation
- Budget utilization
- Testing delays
- Training progress
- Finance approvals
- Legal and regulatory risks
- IT and implementation issues
- Pilot feedback
- Follow-up actions and deadlines

The dataset is stored in:

`data/meeting_transcripts.csv`

## Tool Used

**Google NotebookLM**

NotebookLM was used as the AI-assisted question-answering and source-grounding tool.

No separate machine-learning model was trained for this project.

## Methodology

The project workflow was:

**15 Meeting Transcripts → NotebookLM → AI-use Questions → Source Verification → Project Status Summary → Owner/Date Analysis**

### Step 1 – Dataset Preparation

A structured CSV containing 15 fictional meeting transcripts was prepared.

### Step 2 – AI Analysis

The meeting transcript dataset was uploaded to Google NotebookLM.

Questions were asked about:

- Action-item owners
- Deadlines
- Project decisions
- Budget concerns
- Vendor issues
- Risks
- Testing delays
- Training progress
- Approvals
- Project status

### Step 3 – Verification

NotebookLM's responses were checked against the original meeting transcripts.

The verified results are available in:

`evaluation/T35_T5_Meeting_Notes_QA_Final.xlsx`

### Step 4 – Status Summary

A consolidated project-status summary was prepared from the meeting information.

It is available in:

`documentation/Project_Status_Summary.md`

### Step 5 – Owner/Date Analysis

Potential owner and deadline inconsistencies were reviewed to determine whether they represented genuine AI errors or explicitly documented changes or parallel assignments.

The analysis is available in:

`evaluation/T35_Wrong_Owner_Date_Error_Log_NEW.xlsx`

## Key Findings

The meetings revealed several recurring project-management themes:

- Vendor delays affected testing and implementation timelines.
- Budget utilization increased across the meetings.
- Additional funding requirements were discussed.
- Finance, legal, and regulatory approvals were important dependencies.
- Training schedules and training materials required follow-up.
- Testing delays were linked to vendor sample delays.
- Project decisions were frequently reviewed in subsequent meetings.
- Clear ownership and deadlines were important for project follow-up.

## Final Meeting – MTG015

The final meeting reported:

- The team selected **Option B** and planned to review again the following week.
- Pilot feedback was mostly positive.
- **7 issues were logged.**
- English training material was ready, while Marathi and Hindi versions remained pending.
- Budget utilization reached **96%**, with a potential requirement for an additional **Rs 3 lakh**.
- Legal sign-off on contract changes remained pending.
- The primary risk identified was an upcoming festive-demand spike.
- Zoya Verma was assigned to call the vendor by Friday.
- Diya Singh was assigned to share the revised plan by Friday.

## Evaluation Result

The AI-use interactions were verified against the source meeting transcripts.

**Result: No confirmed wrong owner or wrong date was identified.**

Where similar or repeated assignments appeared, they were evaluated according to the information explicitly stated in the relevant meeting transcript.

## Project Files

```text
Meeting-Notes-QA-Assistant/
│
├── data/
│   └── meeting_transcripts.csv
│
├── documentation/
│   ├── Project_Status_Summary.md
│   └── T35_NovaCRM_Meeting_Notes_QA_Report.docx
│
├── evaluation/
│   ├── T35_T5_Meeting_Notes_QA_Final.xlsx
│   └── T35_Wrong_Owner_Date_Error_Log_NEW.xlsx
│
└── README.md
