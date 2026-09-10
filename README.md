# Painting Company AI Morning Report

AI-powered operations automation built with n8n.

## What it does

This workflow analyzes daily painting crew updates and produces a structured morning operations report.

It automatically:

- Detects completed job progress
- Identifies stalled jobs with 24+ hours of inactivity
- Flags customer, weather, material, and scheduling issues
- Detects safety and major scope-change escalations
- Prevents duplicate job classifications
- Routes escalation cases separately
- Validates and formats AI output
- Produces an auditable final report

## Workflow

```text
Schedule / Webhook
        ↓
Crew Updates
        ↓
Normalize & Filter
        ↓
AI Operations Agent
        ↓
Validate & Format Report
        ↓
Escalation Check
     ↙       ↘
Escalation   Normal
     ↘       ↙
      Audit Log
          ↓
Final Portfolio Output
