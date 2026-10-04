# NovaCRM Meeting-Notes Q&A Assistant

## Project Overview

The **NovaCRM Meeting-Notes Q&A Assistant** is an AI-assisted project management solution that uses meeting transcripts to answer questions about project owners, decisions, deadlines, risks, and project progress.

The project uses **Google NotebookLM** to analyze a dataset of 15 fictional NovaCRM project meeting transcripts and provide source-grounded answers.

## Problem Statement

Project information is often distributed across multiple meeting notes, making it difficult to quickly identify:

- Who is responsible for a task
- Important project decisions
- Deadlines and revised dates
- Current and resolved risks
- Migration and testing outcomes
- Post-launch status

This project demonstrates how an AI-powered meeting-notes assistant can make this information easier to retrieve and verify.

## Objectives

1. Create a structured dataset of 15 project meeting transcripts.
2. Load the transcripts into Google NotebookLM.
3. Design 15 questions related to project management information.
4. Verify NotebookLM's answers against the original meeting transcripts.
5. Generate a consolidated project-status summary.
6. Identify potential owner/date inconsistencies and determine whether they are genuine errors or documented changes.

## Dataset

The dataset contains **15 fictional NovaCRM project meetings** covering the complete project lifecycle from kickoff to pilot launch.

The meetings include topics such as:

- Project kickoff
- Requirements and security
- API contract freeze
- SSO integration
- Compliance
- Data migration
- Defect resolution
- Regression testing
- Launch readiness
- Pilot launch

The dataset is available in:

`data/meeting_transcripts.csv`

## Methodology

The project workflow was:

15 Meeting Transcripts  
↓  
CSV Dataset  
↓  
Google NotebookLM  
↓  
15 Project Questions  
↓  
Answer Verification  
↓  
Project Status Summary  
↓  
Owner/Date Consistency Analysis

## AI Tool Used

**Google NotebookLM**

NotebookLM was used as the AI-powered retrieval and question-answering tool. The meeting transcripts were provided as source material, and questions were asked about project owners, dates, decisions, risks, and outcomes.

This project does **not** involve training a new machine-learning model. It demonstrates the use of an existing AI tool for grounded information retrieval and project analysis.

## Evaluation

A total of **15 questions** were evaluated.

The questions covered:

- Task ownership
- Deadlines
- Security and masking
- Compliance
- Migration results
- Defects
- Testing
- SSO certificates
- Launch decisions
- Launch-day activities
- Pilot outcomes

All 15 answers were verified against the meeting transcripts and were found to be correct.

The detailed verification is available in:

`evaluation/T35_NotebookLM_QA_Verification.xlsx`

## Owner and Date Analysis

Potential owner/date inconsistencies were reviewed across the meeting transcripts.

The analysis found **no genuine unresolved owner or date errors**. The identified differences were documented project changes, clarifications, or changes in task timing.

The detailed analysis is available in:

`evaluation/T35_Wrong_Owner_Date_Error_Log.xlsx`

## Project Status

The NovaCRM pilot was successfully launched on **30 September 2026** and entered a two-week observation phase.

Key launch outcomes included:

- Migration completed at 08:10.
- 99.83% of records were successfully loaded.
- API availability was 99.98%.
- No critical UI or compliance incidents were reported.
- Four support tickets were recorded.
- The pilot remained active for the planned observation period.

## Key Project Decisions

Some major decisions captured from the meetings include:

- Server-side role-based masking was enforced.
- CSV exports were included in masking controls.
- The API contract was frozen.
- Compliance sign-off was formally rescheduled.
- Invalid migration records were handled through a quarantine strategy.
- The project received a GO decision for the pilot launch.
- A launch-day command center was established.
- A two-week pilot observation period was planned.

## Repository Structure

```text
NovaCRM-Meeting-Notes-QA-Assistant/
│
├── README.md
│
├── data/
│   └── meeting_transcripts.csv
│
└── evaluation/
    ├── T35_NotebookLM_QA_Verification.xlsx
    └── T35_Wrong_Owner_Date_Error_Log.xlsx
