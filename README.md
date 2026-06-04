# AI News Summarizer Workflow (Advanced)

## Overview

This n8n workflow automatically collects AI-related news and technology updates, summarizes the most important items using Google Gemini, and sends a clean digest by email.

It is designed for people who want a quick daily briefing without manually reading multiple news sources.

---

## Problem Statement

Keeping up with AI and technology news every day takes time. Important updates are often scattered across multiple sources, and it is difficult to read everything and summarize it manually.

This workflow solves that problem by automating the collection, summarization, and delivery of daily news updates.

---

## Solution

The workflow:

1. Runs automatically on a schedule.
2. Fetches news from RSS feeds.
3. Collects technology updates and AI-related items.
4. Pulls AI event information through an HTTP request.
5. Merges and aggregates all the collected data.
6. Sends the content to Google Gemini for summarization.
7. Generates a readable daily briefing.
8. Emails the final summary to the user.

---

## Workflow Architecture

Schedule Trigger  
↓  
AI News Feed  
↓  
Tech Updates Feed  
↓  
Fetch Events  
↓  
Data Merger / Aggregator  
↓  
Google Gemini Summarization  
↓  
Gmail  
↓  
Final Daily Email

---

## Technologies Used

- n8n
- RSS Feeds
- Google Gemini
- Gmail
- HTTP Request
- Data Aggregation

---

## How It Works

### Step 1: Scheduled Execution
The workflow starts automatically at a fixed time every day.

### Step 2: News Collection
It reads news from RSS sources and fetches event-related data through an API request.

### Step 3: Data Preparation
All incoming items are merged and aggregated so that the AI model receives one combined dataset.

### Step 4: AI Summarization
Google Gemini converts the raw news items into a well-organized briefing with:
- AI news highlights
- broader technology updates
- upcoming AI events

### Step 5: Email Delivery
The final summary is sent to Gmail as a daily news report.

---

## Output

The final email contains:
- important AI news
- technology updates
- event listings
- short summaries
- article links

---

## Setup Instructions

1. Import the JSON file into n8n.
2. Configure the RSS feed URLs if needed.
3. Connect Google Gemini credentials.
4. Connect Gmail credentials.
5. Activate the workflow.
6. Verify that the schedule time is correct.

---

## Demo

A screencast is included in the repository demo folder.

---

## Future Improvements

- Add more news sources
- Add topic-based filtering
- Save summaries to Google Sheets or Notion
- Create separate emails for different categories
- Add a Telegram or Slack delivery option

---

## Author

Pranav Mahesh Palled
