# 1\. Project Overview

The Student Expense Tracker is a web application that helps students understand where their money goes. Users upload statements from mobile money (e.g. M-Pesa) and banks (e.g. Co-op Bank), and the app turns those long, hard-to-read transaction lists into clear summaries, charts and comparisons.

## 2\. Problem Statement

Students often receive money in small, frequent amounts and spend it just as quickly on airtime, transport, food, data and withdrawals. Statements record every transaction but explain nothing. 

**Core problem:** Students lack a simple, visual way to track and understand their spending across multiple accounts.

## 3\. Goals and Objectives

Make past spending understandable at a glance.

Combine multiple accounts (mobile money and banks) into one view.

Show month-to-month change so users can see whether they are improving.

Keep the experience simple enough for a first-time user to understand with no training.

## 4\. Target Users

**Primary:** University and college students who use mobile money daily and hold at least one bank account.

**Persona: "Lionel", 21, third-year student**

* Receives an allowance monthly plus occasional income from side jobs.
* Uses M-Pesa for almost everything; has a Co-op Bank account for school fees and savings.
* Wants to know why money runs out before month-end.
* Comfortable with a phone, impatient with spreadsheets.

## 5\. Screens and Features

### Dashboard

Summary cards: last month's total income, last month's total expenses, and current balance.

Comparison with the month before (e.g. "Spending up 12% vs. September") with a clear up/down indicator.

Short list of recent transactions.

Quick link to import a new statement.

### Import

Where statements enter the system.

Large drag-and-drop zone plus a "Choose file" button.

Supported formats noted clearly (e.g. PDF, CSV).

Two-stage progress bar: **Uploading** and **Extracting transactions**.

Success state showing a summary (e.g. "248 transactions found") and a button to view the dashboard.

Error state for unsupported or unreadable files.

### Analytics

Where patterns become visible.

Pie or donut chart of spending by category

Bar or line chart comparing income and expenses across previous months.

Month selector and optional account filter.

### Accounts

Where the user sees what is connected.

Card for each account: bank, mpesa

"Add account" card.

Per-account import shortcut.

### Settings

Where users can switch themes(light and dark)

User determines how long their data is kept

## 6\. User Flow

1. Open the app and land on the **Dashboard** (empty state prompts import).
2. Go to **Import**, drop a statement, watch progress.
3. Return to the **Dashboard** to see the summary populate.
4. Open **Analytics** to explore categories and month comparisons.
5. Open **Accounts** to manage or add accounts.

## 7\. Technical Approach

* **HTML5** for structure, one file per screen (dashboard.html, import.html, analytics.html, accounts.html).
* **Tailwind CSS** for styling, with a shared custom theme (colours, fonts) so all screens stay consistent.
* **Charts:** static placeholders (SVG or images) or a lightweight chart library purely for visuals.
* **Sample data:** hard-coded, realistic figures so the prototype looks believable.

