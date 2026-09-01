# Employee-Request-Management-System
An automated internal workflow that receives, classifies, and routes employee requests — from Google Forms to organized Google Sheets tabs.

## The Problem

Companies with multiple internal request types (leave, expenses, equipment) often end up with messy, unsorted spreadsheets where HR or ops has to manually categorize every submission.

## What This Does

1. **Triggers** when a new employee request is submitted via Google Forms
2. **Cleans** the incoming data (trims whitespace, normalizes values)
3. **Classifies** the request into one of three types
4. **Assigns** an initial status
5. **Routes** it to the correct tab in Google Sheets

## Request Types

| Type | Tab | Example |
|------|-----|---------|
| Leave | `Leave Requests` | "Annual leave, 5 days" |
| Expense | `Expense Requests` | "Client dinner, $85" |
| Equipment | `Equipment Requests` | "Need a new monitor" |

## Workflow

 Google Sheets Trigger → Clean Data → Switch ├── Leave → IF → Add Status → Leave Requests tab ├── Expense → IF → Add Status → Expense Requests tab └── Equipment → Add Status → Equipment Requests tab

 ## Tech Stack
 
- [n8n](https://n8n.io) — workflow automation
- Google Forms — request intake
- Google Sheets — data storage & tracking
