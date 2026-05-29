# AI Automated Job Finder — Daily Job Discovery System

## 🚀 Overview
This project is an AI-powered job discovery automation built using n8n. It automatically fetches the latest remote job postings every morning, processes them, and sends curated job opportunities directly to email.

It helps users stay updated with relevant job openings without manually searching job boards.

---

## 🎯 Problem Statement
Job seekers spend significant time daily searching for relevant job opportunities across multiple platforms.

Challenges include:
- Manual job searching is time-consuming
- Missing new job postings
- No centralized job filtering system
- Repetitive daily browsing

---

## ⚙️ Solution
This workflow automates the entire job discovery process:

- Runs automatically every day at 7 AM
- Fetches job listings from RemoteOK RSS feed
- Parses and extracts job data
- Processes and formats job details using JavaScript
- Structures data using Set node
- Sends curated job opportunities via Gmail

---

## 🧠 Workflow Architecture

Scheduled Trigger (7 AM) → HTTP Request (RSS Feed) → RSS Read Node → JavaScript Processing → Data Formatting (Set Node) → Gmail Notification

---

## 🔧 Tech Stack
- n8n (Workflow Automation Engine)
- RemoteOK RSS Feed API
- RSS Read Node
- JavaScript (Data transformation)
- Gmail API
- Cron/Scheduled Trigger

---

## 📦 Features
- Fully automated daily job scraping
- Real-time job data extraction
- Structured job formatting
- Email-based job delivery
- No manual job searching required
- Runs every morning at 7 AM automatically

---

## 🧠 How It Works

### 1. Scheduled Trigger
The workflow runs automatically every day at 7 AM using a cron-based trigger in n8n.

---

### 2. Data Fetching
An HTTP Request node fetches job listings from:

https://remoteok.com/remote-jobs.rss

---

### 3. RSS Parsing
The RSS Read node extracts structured job data such as:
- Job title
- Company name
- Job link
- Job description

---

### 4. Data Processing (JavaScript Node)
A JavaScript function processes and filters job data for readability and formatting.

---

### 5. Data Structuring
A Set node formats the final output into clean, readable fields.

---

### 6. Email Delivery
A Gmail node sends curated job listings directly to the user’s email, including:
- Job title
- Application link
- Company information

---

## 📸 Demo

### Example Output Email
- Title: “Frontend Developer — Remote”
- Company: XYZ Tech
- Apply Link: https://remoteok.com/...

---

## 📈 Real-World Impact
- Eliminates manual job searching
- Saves 1–2 hours daily
- Provides early access to job postings
- Improves job application speed
- Centralizes job discovery process

---

## 🚀 How to Use

1. Import workflow JSON into n8n
2. Set up scheduled trigger (7 AM)
3. Configure HTTP request node
4. Add Gmail credentials
5. Activate workflow
6. Receive daily job emails automatically

---
