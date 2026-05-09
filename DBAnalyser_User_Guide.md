# DBAnalyser User Guide & Getting Started Document

**Version:** 1.0  
**Last Updated:** May 9, 2026  
**Audience:** End Users, Database Teams, Developers  

---

## Table of Contents

1. What is DBAnalyser?
2. Installation & Initial Setup
3. Login & First Time Setup
4. Dashboard Overview
5. Understanding Database Findings
6. Working with Findings
7. Using the Optimizer
8. Managing Change Requests
9. Reports & Analytics
10. Help Center & Support
11. Quick Reference Guide
12. Glossary of Terms

---

## 1. What is DBAnalyser?

### Purpose

DBAnalyser is an intelligent database analysis and optimization platform designed to:

- **Automatically detect** problems in your SQL code and database structure
- **Intelligently suggest** improvements using AI technology
- **Safely test** all changes before they go live
- **Manage approvals** for database changes through a formal workflow
- **Track changes** for complete audit and compliance purposes

### Who Should Use It?

- Database Administrators (DBAs)
- SQL Developers and Engineers
- Data Architects
- Technical Leads
- Anyone responsible for database performance and quality

### Key Benefits

| Benefit | What You Get |
|---------|------------|
| **Faster Databases** | Optimize slow queries automatically |
| **Safer Changes** | Test before deploying to production |
| **Better Teamwork** | Collaborate with comments and assignments |
| **Complete Tracking** | See who did what and when |
| **Less Risk** | Formal approval process prevents mistakes |
| **Time Savings** | AI suggestions save hours of manual analysis |

### Problems It Finds

- Slow or inefficient SQL queries
- Missing database indexes
- Poorly optimized stored procedures
- Database schema issues
- Performance bottlenecks
- Best practice violations
- Security concerns

---

## 2. Installation & Initial Setup

### System Requirements

**Minimum:**
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- No software installation needed on your computer

**For Full Features (Optimizer):**
- Python 3.9+ (backend server)
- Node.js 16+ (if hosting frontend yourself)
- PostgreSQL database
- 4GB RAM minimum
- Ollama AI engine (for AI suggestions)

### Accessing the Application

**Cloud Version:**
```
1. Go to: https://dbanalyser.yourcompany.com
2. Bookmark this page
3. Keep the URL safe
```

**Local Version:**
```
1. Ask your IT team for the server URL
2. Typical format: http://localhost:5173
3. Bookmark for easy access
```

### Required Access Credentials

You need:
- **Username** - Your email or user ID
- **Password** - Provided by your manager or IT

**Don't have access yet?**
1. Email your manager or DBA
2. Request access to DBAnalyser
3. You'll receive login credentials within 1-2 business days

---

## 3. Login & First Time Setup

### Step-by-Step Login

**Step 1: Open Application**
```
1. Open your web browser
2. Navigate to your company's DBAnalyser URL
3. You should see the login page
```

**Step 2: Enter Credentials**
```
1. Username field: Enter your email or username
2. Password field: Enter your password
3. Check "Remember me" (optional - for your device only)
```

**Step 3: Login**
```
1. Click "Login" button
2. Wait for page to load (usually 2-3 seconds)
3. You should see the dashboard
```

**Step 4: Welcome Screen**
```
You'll see:
- Your name (top right)
- Main dashboard
- Navigation menu (left side)
- Quick action buttons
```

### First Time Configuration

**Accessing Settings:**
1. Click your **profile icon** (top right corner)
2. Select **"Settings"** from dropdown menu
3. You're now in preferences section

**Basic Settings to Configure:**

**Setting 1: Email Notifications**
```
Location: Settings → Notifications

Options:
☐ Email when someone assigns me a task
☐ Email when change request needs my approval
☐ Email daily summary
☐ Email when scan completes

Recommendation: 
Enable at least task assignment notifications
```

**Setting 2: Display Preferences**
```
Location: Settings → Display

Options:
☐ Light mode / Dark mode (choose one)
☐ Items per page (10, 25, 50, 100)
☐ Default date format (MM/DD/YYYY or DD/MM/YYYY)

Recommendation:
Choose mode based on preference, 50 items per page works well
```

**Setting 3: Default Database**
```
Location: Settings → Defaults

Action:
1. Click "Select Default Database"
2. Choose the database you work with most
3. This appears first when you open app

Benefit:
Saves time - your main database loads automatically
```

**Setting 4: Timezone**
```
Location: Settings → Regional

Action:
1. Select your timezone from dropdown
2. All dates/times display in your timezone

Why it matters:
Ensures you see correct times for approvals and deadlines
```

**Save Your Changes:**
```
1. After configuring settings
2. Click "Save Preferences" button (bottom right)
3. See green checkmark: "Settings saved successfully"
4. Done!
```

---

## 4. Dashboard Overview

### What is the Dashboard?

The Dashboard is your **main control center**. It shows:
- All database problems found
- Their severity and current status
- Who is working on them
- Quick actions available

### Dashboard Layout

**Top Section:**
```
┌─────────────────────────────────────┐
│ Welcome, John!           🔔 ⚙️ 👤   │  Notifications, Settings, Profile
└─────────────────────────────────────┘
```

**Left Navigation Menu:**
```
📊 Dashboard (home)
🔍 New Assessment
🐢 Findings (all problems)
⚙️ Optimizer (AI suggestions)
📋 Change Requests
📈 Reports
❓ Help
```

**Main Content Area:**
```
┌──────────────────────────────────────────┐
│ Filter Options:                          │
│ [Severity ▼] [Status ▼] [Database ▼]   │
│                                          │
│ Your Recent Findings:                    │
│ ┌────────────────────────────────────┐  │
│ │ Problem | Severity | Status | View │  │
│ ├────────────────────────────────────┤  │
│ │ Slow query | High | Pending| [✓]  │  │
│ │ Missing index | Medium | In Progress │
│ │ ... more rows ...                  │  │
│ └────────────────────────────────────┘  │
└──────────────────────────────────────────┘
```

### Reading the Dashboard Table

**Column 1: Problem Name**
```
Shows: "Slow query in order_processing"
What it means: Brief description of the issue
Action: Click to view full details
```

**Column 2: Severity**
```
Shows: Color-coded badge
🔴 Critical - Fix immediately (within hours)
🟠 High - Fix this week
🟡 Medium - Fix this month
🟢 Low - Fix when convenient

Click to filter by severity
```

**Column 3: Status**
```
Shows: Current stage
Pending - Just found
In Progress - Someone working on it
Testing - Changes being tested
Approved - Ready to deploy
Deployed - Already fixed
Closed - Complete

Click to filter by status
```

**Column 4: Assigned To**
```
Shows: Person's name or "Unassigned"
Your Name: You're responsible
Someone Else: They're working on it
Unassigned: No one has taken it yet

Click to assign if unassigned
```

**Column 5: Actions**
```
Shows: Button options
[View] - See full details
[Assign] - If unassigned
[Edit] - Modify details
[More...] - Additional options
```

### Using Dashboard Filters

**Filter by Severity:**
```
1. Click "Severity" dropdown (top of list)
2. Choose:
   ☐ Critical only
   ☐ High and above
   ☐ All severities
3. List updates instantly
4. To clear: Click "Reset Filters"
```

**Filter by Status:**
```
1. Click "Status" dropdown
2. Choose:
   ☐ Pending (not started)
   ☐ In Progress (being worked on)
   ☐ Approved (ready to deploy)
   ☐ Deployed (completed)
3. List updates instantly
```

**Filter by Database:**
```
1. Click "Database" dropdown
2. Choose your database:
   ☐ Production_DB
   ☐ Staging_DB
   ☐ Dev_DB
   ☐ All databases
3. List updates instantly
```

**Filter by Assigned To:**
```
1. Click "Assigned To" filter
2. Choose:
   ☐ My Tasks (assigned to you)
   ☐ [Person Name]
   ☐ Unassigned
3. List updates instantly
```

### Dashboard Actions

**Search for Specific Problem:**
```
1. Look for search box (usually top right)
2. Type part of problem name
3. Example: type "query" → shows all query-related problems
4. Press Enter or wait (auto-searches)
```

**Sort the List:**
```
1. Click any column header to sort
2. Click again to reverse sort (A→Z or Z→A)
3. Arrow shows sort direction (↑ or ↓)

Popular sorts:
- By Severity (Critical first)
- By Date Added (Newest first)
- By Status (Pending first)
```

**Pagination (Page Navigation):**
```
At bottom of table:
← [1] [2] [3] [4] →

Actions:
- Click page number to jump to it
- Click ← for previous page
- Click → for next page
- Or select items per page (25, 50, 100)
```

---

## 5. Understanding Database Findings

### What is a "Finding"?

A **Finding** is a single database problem that was detected.

**Example Finding:**
```
Name: "Slow SELECT query in customer_orders view"
Type: Performance issue
Severity: High (red)
Found: April 8, 2026 at 2:45 PM
Status: Pending
Rule: PERF-001
```

### How Are Findings Created?

**Automatically:**
1. System scans your database
2. Compares against best practices
3. Finds problems
4. Creates finding records

**Time taken:** 5-15 minutes per database

**Manually:**
1. Click "Report Issue"
2. Describe problem
3. System creates finding
4. You add details

### Finding Details Page

**Opening a Finding:**
```
1. Go to Dashboard
2. Click [View] button next to finding
3. Detailed popup window opens
4. Shows all information about this problem
```

**Top Section:**
```
┌────────────────────────────────────────┐
│ Problem Name: "Slow query in orders"  │
│ ID: FIND-2026-001234                  │
│ Created: April 8, 2026 by: Scan       │
│ Status: ⚫ Pending                     │
│ Severity: 🔴 High                     │
│ Assigned To: [Unassigned ▼]           │
└────────────────────────────────────────┘
```

**Tab Navigation (5 Tabs):**
```
[Problem] [Solution] [Help] [Comments] [History]
```

---

## 6. Working with Findings

### Tab 1: Problem - Understanding the Issue

**What You See:**
```
✓ Description of the problem
✓ The SQL code causing the issue
✓ Which rule flagged it
✓ Why it's a problem
✓ Impact assessment
```

**Example Screen:**

```
PROBLEM DESCRIPTION
────────────────────────────────────────

Issue Type: Query Performance

Description:
The SELECT query in the customer_orders view performs a full table scan
on a table with 5 million rows. No index on the customer_id column means
every query must check all rows, taking approximately 3 seconds per request.

Original SQL Code:
────────────────────────────────────────
CREATE VIEW v_customer_orders AS
SELECT * 
FROM orders 
WHERE customer_id = 5

Why This is a Problem:
────────────────────────────────────────
- Full table scan instead of indexed lookup
- Takes 3 seconds per query
- With 1000 users, that's 1000 seconds of waiting per second
- High database CPU usage (85%)
- Users see timeout errors

Impact:
────────────────────────────────────────
- Performance: Very Slow (3000ms per query)
- CPU Usage: 85% (very high)
- Memory: 2GB per 1000 queries
- Users Affected: All who access orders
- Risk If Not Fixed: System outages possible
```

**How to Read It:**
1. Start with "Description"
2. Read the SQL code carefully
3. Check "Why This is a Problem"
4. Understand the impact

### Tab 2: Solution - Recommended Fix

**What You See:**
```
✓ What the fix is
✓ Why this fixes it
✓ Expected improvement
✓ Risk assessment
✓ Alternative solutions (if available)
```

**Example Screen:**

```
RECOMMENDED SOLUTION
────────────────────────────────────────

Solution: Create an index on customer_id column

Recommended SQL:
────────────────────────────────────────
CREATE INDEX idx_orders_customer_id 
ON orders(customer_id);

Why This Fixes It:
────────────────────────────────────────
An index is like a phone book. Instead of reading every name in a book,
you can look up the letter and jump directly to names starting with that
letter. Similarly, this index lets the database jump directly to rows with
specific customer_id values, avoiding the full table scan.

Expected Improvements:
────────────────────────────────────────
- Response Time: 3 seconds → 150 milliseconds (95% faster)
- CPU Usage: 85% → 10% (much lower)
- Memory: 2GB → 100MB (20x less)
- Concurrent Users: 10 → 500 (50x more capacity)

Risk Assessment:
────────────────────────────────────────
Risk Level: LOW ✓

Why it's low risk:
- Creating indexes doesn't change data
- Query results stay exactly the same
- Can be rolled back instantly if needed
- Only affects performance, not functionality

Implementation Time: 2 minutes

Alternative Solutions (if available):
────────────────────────────────────────
1. Partition the table by customer_id
   Pros: Very effective
   Cons: Complex, time-consuming
   Risk: Medium

2. Archive old data
   Pros: Smaller table
   Cons: Need to maintain archives
   Risk: Low
```

**How to Use It:**
1. Read the recommended solution
2. Check expected improvements
3. Review risk assessment
4. Decide if you want to proceed
5. Next: Go to "Optimizer" tab to test it

### Tab 3: Help - Learn More

**What You See:**
```
✓ Educational content about this type of issue
✓ Best practices
✓ Related links
✓ Examples
✓ When to use different approaches
```

**Example Screen:**

```
HELP & EDUCATION
────────────────────────────────────────

What are Database Indexes?

An index is a data structure that allows the database to find data
without scanning all rows in a table. Like a book index at the back
that tells you which pages to read for specific topics.

When Should You Create an Index?

✓ Column frequently used in WHERE clause
✓ Column used in JOIN conditions
✓ Column has high cardinality (many unique values)
✓ Table has >10,000 rows

When NOT to Create an Index?

✗ Column has very few unique values
✗ Table is very small (<1,000 rows)
✗ Column is rarely queried
✗ Index would take too much space

Best Practices:

1. Index columns in WHERE clauses
   WHERE customer_id = 5  → Index customer_id

2. Index columns in JOIN conditions
   ON orders.customer_id = customers.id  → Index both

3. Don't over-index
   Too many indexes slows down INSERT/UPDATE

4. Monitor index usage
   Remove unused indexes

5. Rebuild indexes periodically
   Keeps them efficient

Related Topics:
────────────────────────────────────────
→ Types of Indexes (Single, Composite, Full-Text)
→ Index Performance Tuning
→ Query Optimization Best Practices
→ Database Schema Design

Examples of Good Indexes:
────────────────────────────────────────
CREATE INDEX idx_orders_customer_id ON orders(customer_id);
CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_products_category ON products(category_id);

Examples of Poor Indexes:
────────────────────────────────────────
CREATE INDEX idx_orders_id ON orders(id);
-- Bad: Primary key already indexed

CREATE INDEX idx_long_text ON descriptions(full_description);
-- Bad: Indexing text column too large
```

**How to Use It:**
1. Read if you want to learn more
2. Not required for fixing the problem
3. Great for professional development
4. Share with team members to teach them

### Tab 4: Comments - Collaborate with Team

**What You See:**
```
✓ Thread of all comments
✓ Who said what
✓ When they said it
✓ Ability to reply
```

**Viewing Comments:**

```
DISCUSSION THREAD
────────────────────────────────────────

John Smith - 2026-04-08 at 10:30 AM
"I found this issue. The customer_orders view is timing out.
I think adding an index would help, but I want team input first."

Sarah Johnson - 2026-04-08 at 11:15 AM
"Good catch! I've seen this before. Yes, the index will definitely help.
I tested similar changes on another table last month and saw 90% improvement."

Michael Chen - 2026-04-08 at 2:45 PM
"Confirmed. I ran a test query - takes 3 seconds. Let's move forward with the index.
I'll create the change request."

You - Now
[Type your message here...]
[Post Comment]
```

**Adding a Comment:**

**Step 1: Click Comment Box**
```
Look for text field at bottom that says "Type your message here..."
Click on it
```

**Step 2: Type Your Message**
```
Keep it professional:

Good:
"I tested this on my local database. Query time improved from 3 seconds 
to 150ms. I'm ready to create a change request."

Bad:
"k this looks fine"
"👍👍👍"

Better:
"Looks good! Let's proceed."
```

**Step 3: Send Your Comment**
```
1. After typing, click [Post Comment] button
2. Your comment appears immediately
3. Others see it within seconds
4. They can reply with [Reply] button
```

**Best Practices for Comments:**

```
✓ BE SPECIFIC
  "Tested query, improvement confirmed" ← Good
  
✓ PROVIDE DETAILS
  "Ran test: 3000ms → 150ms (95% faster)" ← Good
  
✓ ASK QUESTIONS IF UNSURE
  "Should we also index the date column?" ← Good
  
✓ SHARE KNOWLEDGE
  "Based on similar case last month..." ← Good
  
✗ DON'T USE PERSONAL INFO
  "My password is xxxxxxx" ← Bad! Never!
  
✗ DON'T COMPLAIN
  "This database is a mess" ← Unprofessional
  
✗ DON'T BE VAGUE
  "Something's wrong" ← Not helpful
```

### Tab 5: History - Timeline of Changes

**What You See:**
```
✓ Complete timeline of everything that happened
✓ Who did what
✓ When they did it
✓ What changed
✓ Why they changed it
```

**Example Timeline:**

```
CHANGE HISTORY
────────────────────────────────────────

📌 April 8, 2026 - 3:45 PM
Status Changed to: "In Progress"
Changed By: Michael Chen
Reason: "Starting work on this. Will test tomorrow."

📌 April 8, 2026 - 2:15 PM
Status Changed to: "Pending"
Changed By: System
Reason: "Initial creation - awaiting assignment"

📌 April 8, 2026 - 10:30 AM
Finding Created
Found By: Automated Scan
Reason: "Database scan identified performance issue"


DECISION TRACKING
────────────────────────────────────────

Who Needs to Decide Next?
- You haven't assigned this yet
- Consider assigning to most experienced team member
- Or work on it yourself

Timeline for this finding:
- Found: April 8
- Started: Today
- Target Fix: April 15
- Deployment: April 20
```

**Why History Matters:**

```
✓ Accountability: See who did what
✓ Learning: Review how past similar issues were handled
✓ Compliance: Prove actions taken (for audits)
✓ Troubleshooting: Understand what was tried before
✓ Training: Show new team members how you work
```

---

## 7. Using the Optimizer

### What is the Optimizer?

The Optimizer is an **AI-powered assistant** that:
- Analyzes your database problems
- Suggests improvements
- Tests them for you
- Compares performance

**Powered by:** Ollama (local AI, not cloud-based)

### When to Use the Optimizer

**Use it when:**
```
✓ You have a slow query
✓ You want AI suggestions for improvement
✓ You want to test changes safely
✓ You need performance comparisons
✓ You want to download optimized code
```

**Don't use it when:**
```
✗ The database is down (no queries possible)
✗ You're in the middle of a major deployment
✗ You already know the fix
✗ Changes are purely structural (new columns, tables)
```

### Accessing the Optimizer

**From Dashboard:**
```
1. Go to Dashboard
2. Find your problem
3. Click [View]
4. Find "Optimizer" tab
5. Click it
```

**OR Direct Menu:**
```
1. Left navigation → Optimizer
2. Select finding from list
3. Scroll to optimization section
```

### Step 1: Get Optimization Suggestion

**What Happens:**
1. You provide SQL code with problem description
2. AI analyzes it
3. AI suggests better version
4. You review the suggestion

**How to Use:**

**Screen 1: Input Section**

```
OPTIMIZATION REQUEST
────────────────────────────────────────

Finding: "Slow query in customer_orders view"
Rule: PERF-001

Original SQL Code:
[Box showing original SQL code]

Issue Description:
"Full table scan on large table - no index"

Confidence Level to Accept:
○ High (80%+) - Very confident suggestions only
○ Medium (60%+) - Balanced - default
○ Low (40%+) - All suggestions (experimental)

[Get Suggestion Button]
```

**Step 2: Click "Get Suggestion"**

```
1. Review your input is correct
2. Click large blue button: [Get Optimization Suggestion]
3. System connects to AI
4. Shows: "Analyzing your query... (this takes 10-15 seconds)"
5. Wait for response
```

**Step 3: Review AI Response**

```
AI OPTIMIZATION RESULT
────────────────────────────────────────

Confidence Score: 85%
🟢 High confidence suggestion

Estimated Improvement: 75%
Performance should improve by 75%

Risk Level: 🟢 LOW
Safe to implement

Suggested SQL Code:
────────────────────────────────────────
CREATE INDEX idx_orders_customer_id 
ON orders(customer_id);

AI Explanation:
"This query performs a full table scan on a table with 5 million rows.
Adding an index on the customer_id column will allow the database to
directly locate the required rows instead of scanning the entire table,
resulting in a 75% performance improvement."

Next Steps:
1. [Test on UAT] - Verify the suggestion
2. [Download] - Save the SQL code
3. [Try Again] - Get different suggestion
```

**Interpreting Scores:**

```
CONFIDENCE SCORE (0-100%)
────────────────────────────────────────
90-100% = Excellent (Deploy with confidence)
70-89%  = Good (Likely to work, test first)
50-69%  = Medium (Test thoroughly before deploying)
<50%    = Low (Get second opinion, don't rely on this)

IMPROVEMENT ESTIMATE (0-100%)
────────────────────────────────────────
75-100% = Major improvement (excellent)
50-74%  = Significant (good)
25-49%  = Moderate (helps but not game-changing)
<25%    = Minor (small benefit)

RISK LEVEL
────────────────────────────────────────
🟢 LOW      = Safe, low chance of problems
🟡 MEDIUM   = Moderate risk, needs testing
🔴 HIGH     = Significant risk, careful review needed
```

### Step 2: Test on UAT

**What is UAT?**
```
UAT = User Acceptance Testing

Safe copy of your production database
where tests don't affect real users
```

**Why Test First?**
```
✓ Verify the fix actually works
✓ Check for unexpected problems
✓ See real performance improvement
✓ Prove data integrity (same results)
✓ All before touching production database
```

**How to Test:**

**Click "Test on UAT" Button**

```
Testing in progress...
━━━━━━━━━━━━━━━━━━━ 50%
Running original query...
Running optimized query...
Comparing results...
```

**Test Results Display:**

```
TEST RESULTS
════════════════════════════════════════

Test Database: UAT (Safe Copy)
Test Time: 2026-04-08 14:30

PERFORMANCE COMPARISON
────────────────────────────────────────

Original Query:
├─ Execution Time: 3,200 milliseconds (3.2 seconds)
├─ CPU Usage: 85%
├─ Memory Used: 2.1 GB
└─ Rows Returned: 1,247

Optimized Query:
├─ Execution Time: 215 milliseconds (0.215 seconds)
├─ CPU Usage: 8%
├─ Memory Used: 125 MB
└─ Rows Returned: 1,247

IMPROVEMENT METRICS
────────────────────────────────────────
Speed Improvement: 93% faster ✓
CPU Reduction: 91% less ✓
Memory Reduction: 94% less ✓
Data Integrity: ✓ VERIFIED (same 1,247 rows)

VERDICT: ✓ PASS - Safe to deploy

Status after UAT:
Your optimization passed all tests!

Next Steps:
1. [Download] - Get the SQL code
2. [Submit for Approval] - Start CR process
3. [Try Different] - Get another suggestion
```

**Understanding Test Results:**

```
What Each Metric Means:

Execution Time:
- How long the query takes
- Lower is better
- Example: 3,200ms → 215ms = 93% faster

CPU Usage:
- How much processing power used
- Lower is better
- Example: 85% → 8% = much easier on server

Memory Used:
- RAM consumed during query
- Lower is better
- Example: 2.1GB → 125MB = saves memory

Rows Returned:
- Number of results
- Should be same for both queries
- If different: ❌ Data integrity problem

Data Integrity: VERIFIED
- Means both queries returned identical data
- Important! If different, optimization changed results
- In that case: ❌ Don't use this optimization
```

**If Test Fails:**

```
❌ TEST FAILED

What went wrong:
Original query returned: 1,247 rows
Optimized query returned: 1,224 rows

The optimized query changed the results!
This could be a bug in the suggestion.

What to do:
1. Click [Review] to see the difference
2. Check the suggested SQL carefully
3. Click [Try Another Suggestion] for new AI suggestion
4. Or click [Manual Fix] to write your own
```

### Step 3: Download Optimized SQL

**Why Download?**

```
✓ Have a backup copy of the code
✓ Share with team before deployment
✓ Include in change request documentation
✓ Reference for similar issues
✓ Version control / Git
```

**How to Download:**

```
DOWNLOAD OPTIMIZED SQL
────────────────────────────────────────

1. After successful test, click [Download] button

2. Choose format (select one):
   ☐ SQL File (.sql) - Recommended
   ☐ Text File (.txt)
   ☐ PDF Report
   ☐ Copy to Clipboard

3. If you chose .sql or .txt:
   - File downloads to your computer
   - Default location: Downloads folder
   - Filename: "optimization_2026_04_08.sql"

4. What's in the file:

   -- Original Query (CURRENT)
   -- ================================================
   SELECT * FROM orders WHERE customer_id = 5;

   -- Optimized Query (SUGGESTED)
   -- ================================================
   CREATE INDEX idx_orders_customer_id 
   ON orders(customer_id);

   -- Performance Comparison
   -- ================================================
   -- Original: 3,200ms, 85% CPU
   -- Optimized: 215ms, 8% CPU
   -- Improvement: 93% faster

   -- Confidence: 85%
   -- Risk Level: LOW
   -- Date: 2026-04-08
   -- Downloaded by: John Smith
```

**After Download:**

```
1. Review the file carefully
2. Save in a safe location
3. Add to your documentation
4. Ready to proceed to change request
5. Or share with team for review first
```

---

## 8. Managing Change Requests

### What is a Change Request (CR)?

A **Change Request** is a **formal, tracked request to change the database**.

**Why are they needed?**

```
✓ Prevents accidents
✓ Gets approval from responsible people
✓ Tracks who made what change
✓ Creates audit trail for compliance
✓ Allows rollback if problems occur
✓ Ensures safety through reviews
```

### Creating a Change Request

**From Optimizer:**

```
1. After testing optimization:
   - Click [Submit Change Request] button
   - Form appears automatically
   - Pre-filled with optimization details
```

**Manually:**

```
1. Go to "Change Requests" in left menu
2. Click [Create New CR] button
3. Fill out form (details below)
```

### CR Form - Fields to Fill

**Field 1: Title**

```
What it is: Short name for this change

Good examples:
"Add index to orders.customer_id"
"Optimize customer_orders view"
"Remove unused stored procedure"

Bad examples:
"Fix stuff"
"Database change"
"Urgent"

Tips:
- Keep it 5-15 words
- Be specific
- Start with action verb (Add, Remove, Optimize, etc.)
```

**Field 2: Description**

```
What it is: Detailed explanation of the change

What to include:
- What are you changing?
- Why do you need to change it?
- What problem does it solve?
- Any risks?
- Expected benefits?

Example:
"Adding an index to orders(customer_id) will solve
the performance issue where queries take 3+ seconds.
Test on UAT shows 93% improvement with no data issues.
Risk is low as this is purely performance optimization.
Benefits: Better user experience, reduced server load."

Tips:
- Use 3-5 sentences
- Be clear and professional
- Provide context
- Don't use jargon if avoidable
```

**Field 3: Priority**

```
Options:
🔴 Critical - Change needed immediately (within hours)
🟠 High - Change needed urgently (within 24 hours)
🟡 Medium - Normal priority (within 1 week)
🟢 Low - Can wait (within 1 month)

How to choose:
- System is broken? → Critical
- Users can't work? → Critical
- Performance is bad? → High
- Nice to have? → Low

Default: High (unless you specify)
```

**Field 4: Expected Impact**

```
Options:
○ No downtime needed
○ <1 minute downtime
○ 1-5 minutes downtime
○ 5-30 minutes downtime
○ >30 minutes downtime

What it means:
Will users notice? Will the database be offline?

For most optimizations: "No downtime needed"
For schema changes: May need downtime

Tips:
- Be honest about impact
- Affects scheduling of deployment
```

**Field 5: Attachments (Optional)**

```
You can upload:
- SQL script file
- Test results screenshot
- Performance comparison chart
- Documentation
- Word doc with details

Steps:
1. Click [Choose File] button
2. Find file on your computer
3. Click it
4. File shows as attached

Tip:
Always attach the optimized SQL file
```

**Field 6: Assign Reviewer (Optional)**

```
If you know who should review:
1. Click "Select Reviewer"
2. Choose from dropdown
3. That person gets notified

If you don't know:
- Leave blank
- System assigns automatically
- Usually assigns to tech lead

Tip:
Assign to most senior person you know
if you want faster approval
```

**Final Step: Submit**

```
1. Review all information one more time
2. Verify attachments uploaded
3. Click large [SUBMIT CHANGE REQUEST] button
4. See confirmation: "Change Request CR-2026-001234 Created"
5. You're done! Now it's in review process
```

### CR Review Process (4 Stages)

**What is it?**

```
Your CR goes through 4 levels of approval before deployment:

Stage 1: 👥 Peer Review
         Developer checks your work

Stage 2: 👨‍💼 Tech Lead Review
         Tech lead checks architecture

Stage 3: 👨‍💻 DBA Review
         Database admin checks impact

Stage 4: 🔒 Compliance Review
         Ensures regulatory requirements
```

**Viewing CR Status:**

```
In your CR:
You can see:

┌─────────────────────────────┐
│ CR-2026-001234              │
│ Add index to orders         │
│                             │
│ Stage 1: Peer Review        │
│ Status: ✓ Approved 04/08    │
│ Approver: Sarah Johnson     │
│                             │
│ Stage 2: Tech Lead Review   │
│ Status: ⏳ Pending          │
│ Waiting for: Michael Chen   │
│                             │
│ Stage 3: DBA Review         │
│ Status: ⭕ Not started      │
│                             │
│ Stage 4: Compliance Review  │
│ Status: ⭕ Not started      │
└─────────────────────────────┘

Current Status: "In Review (Stage 2)"
Next Step: Waiting for Tech Lead approval
```

**If You're a Reviewer:**

```
When someone submits a CR, you might get notified.

Email notification:
────────────────────────────────────────
Subject: "Change Request CR-2026-001234 Needs Your Approval"

Body: "Please review and approve/reject the following change..."

Steps to Review:
────────────────────────────────────────
1. Click email link (takes you to CR details)
2. Read description and original SQL
3. Review test results
4. Click [View Change] to see details
5. Make decision:
   - Click [Approve] if it looks good
   - Click [Request Changes] if you have concerns
   - Add comment explaining your decision
6. Click [Submit]
```

### CR Deployment (After All Approvals)

**When All 4 Stages Approved:**

```
Status shows:
✓ Stage 1: Approved
✓ Stage 2: Approved
✓ Stage 3: Approved
✓ Stage 4: Approved

CR Status: "Ready to Deploy"

Who can deploy:
- Database Administrator (DBA)
- Usually only the DBA does this

Next step:
Wait for DBA to schedule deployment
```

**Deployment Process:**

```
DBA does:

1. Run pre-deployment checks
   - Verify SQL syntax
   - Check security
   - Verify performance
   - Verify compatibility

2. Deploy to production
   - Run the SQL command
   - Monitor for errors
   - Check if successful

3. Run post-deployment validation
   - Verify database still healthy
   - Check performance improved
   - Verify no data loss
   - Check all queries still work

4. If all good:
   - Status changed to "Deployed"
   - You get notification
   - Problem marked "Resolved"

5. If problem:
   - Status changed to "Failed"
   - CR can be rolled back
   - System reverts the change
```

### Rollback (Undo Recent Changes)

**What is Rollback?**

```
Undo a recent change that caused problems

Example:
- Deployed optimization Monday at 10am
- Discovered it caused issues Monday at 3pm
- Click [Rollback] button
- Change undone (back to original)
```

**Rollback Window:**

```
When can you rollback?

✓ Within 1 hour of deployment
✓ Only if change is causing problems

❌ After 1 hour - automatic window closes
❌ If change is working fine

Why time limit?
- System snapshot only kept for 1 hour
- After that, need manual intervention
```

**How to Rollback:**

```
1. Go to your CR
2. Look for [Rollback] button
   (appears if within 1 hour)
3. Click it
4. Enter reason: "Causing query timeouts"
5. Click [Confirm Rollback]
6. System reverts change
7. Database back to previous state
8. Status shows "Rolled Back"
```

---

## 9. Reports & Analytics

### What Are Reports?

**Reports** show you:
- Summary of database problems
- Progress over time
- Trends (improving or getting worse)
- Statistics and metrics
- Who fixed what

### Accessing Reports

**From Menu:**
```
1. Left navigation → Reports
2. Shows various report options
```

**From Dashboard:**
```
1. Dashboard → [View Report] button
2. Pre-filled with current data
```

### Available Report Types

**Report 1: Executive Summary**

```
WHO SHOULD READ: Managers, Directors, Executives

WHAT YOU GET:
├─ Total problems found (this week)
├─ Critical problems (red flag)
├─ Problems resolved (progress)
├─ Average time to fix
├─ Trend (getting better/worse?)
└─ Top recommendations

EXAMPLE OUTPUT:
────────────────────────────────────────
Database Health Summary
Week of April 8-14, 2026

Total Issues: 42 (↑ from 38 last week)
Critical: 2 (need immediate attention)
Resolved: 18 (43% closure rate)
In Progress: 12
Pending: 12

Trend: IMPROVING ✓
Average Fix Time: 3 days (improving by 1 day)

Top Issue: Slow customer_orders view
Status: Fixed this week (deployed 04/12)
Impact: 500+ users affected (now resolved)

Recommendation: Continue current pace
```

**Report 2: Technical Details**

```
WHO SHOULD READ: Developers, DBAs, Technical Teams

WHAT YOU GET:
├─ Detailed issue list
├─ SQL code snippets
├─ Performance metrics
├─ Test results
├─ Before/after comparisons
└─ Deployment history

EXAMPLE OUTPUT:
────────────────────────────────────────
Detailed Technical Report
April 8-14, 2026

Issue #1: Slow customer_orders view
────────────────────────────────────────
Severity: High
Cause: Missing index on customer_id
Original Performance: 3,200ms
Optimized Performance: 215ms
Improvement: 93% faster
Status: Deployed 04/12/2026
Deployed by: Maria Garcia

[Shows SQL code]
[Shows test results table]
[Shows query plan comparison]

Issue #2: Inefficient user_reports procedure
────────────────────────────────────────
[Similar detailed breakdown]
```

**Report 3: Trend Analysis**

```
WHO SHOULD READ: Team Leads, Managers

WHAT YOU GET:
├─ Chart showing problem count over time
├─ Which categories are improving
├─ Which categories are getting worse
├─ Predictions for next month
└─ Recommendations

EXAMPLE OUTPUT:
────────────────────────────────────────
Database Health Trends
Last 90 Days

Chart: Problem Count Over Time
300 problems
250
200 ▲
150 ██
100 ██ ▲▲
 50 ██ ▲▲ ▲
  0 ██ ▲▲ ▲ ▼ ▼
    Mar Apr May

← Trend: IMPROVING (down from 280 to 45)
← Prediction: 20 problems by end of May

Problems by Category:
Performance: 45 (↓ from 120) - Much improved
Schema: 8 (→ stable)
Security: 0 (← Fixed all!)
Other: 5 (↓ from 8) - Improving
```

**Report 4: Team Performance**

```
WHO SHOULD READ: Team Leads, Managers

WHAT YOU GET:
├─ Number of problems each person fixed
├─ Average time each person takes
├─ Problem resolution rate
├─ Who approved the most changes
└─ Team statistics

EXAMPLE OUTPUT:
────────────────────────────────────────
Team Performance Report
April 2026

Problems Resolved by Team Member:
────────────────────────────────────────
John Smith:    15 issues (40% of team)
Sarah Johnson: 12 issues (32% of team)
Michael Chen:   8 issues (21% of team)
You:            3 issues (8% of team)

Average Resolution Time:
────────────────────────────────────────
John Smith:    3 days
Sarah Johnson: 4 days
Michael Chen:  5 days
You:           2 days ← Fastest!

Change Requests Approved:
────────────────────────────────────────
[DBA Name]:       32 approved
[Tech Lead Name]: 28 approved
[Other]:          15 approved
```

### Generating a Report

**Step 1: Open Reports**
```
1. Click "Reports" in left menu
2. See report options
```

**Step 2: Choose Report Type**
```
1. Click report you want
2. Example: "Executive Summary"
```

**Step 3: Set Parameters**

```
REPORT PARAMETERS
────────────────────────────────────────

Date Range:
○ Last 7 days (current week)
○ Last 30 days
○ Last 90 days
○ Custom date range
  From: [April 1, 2026 ▼]
  To:   [April 30, 2026 ▼]

Database (optional):
☐ All databases
☐ Production_DB only
☐ Staging_DB only

Severity Filter (optional):
☐ All
☐ Critical only
☐ Critical + High

[Generate Report]
```

**Step 4: View Report**

```
Report generates and displays on screen
Shows all data selected
Ready to view/download
```

**Step 5: Download Report**

```
After viewing, click [Download]

Choose format:
○ PDF - Best for printing/sharing
○ Excel - Best for analysis/pivot tables
○ HTML - Best for web viewing

File downloads to computer
File named: "report_20260408_ExecSummary.pdf"
```

### Sharing Reports

**Email Report:**
```
1. Click [Share] button
2. Enter email addresses (comma-separated)
3. Add message (optional)
4. Click [Send]
5. Report sent as attachment
```

**Print Report:**
```
1. Download as PDF
2. Open PDF
3. Use browser print (Ctrl+P)
4. Print to printer or PDF
```

**Include in Documentation:**
```
1. Download as PDF or Excel
2. Attach to documentation
3. Include in presentations
4. Use for meetings/reviews
```

---

## 10. Help Center & Support

### Accessing Help Center

**From Application:**
```
1. Click "Help" in left menu
2. Shows help articles
```

**Search for Help:**
```
1. Click search box (top of Help section)
2. Type your question
   Example: "How to create change request"
3. Press Enter
4. See matching articles
```

### Finding Answers

**Browse by Category:**

```
HELP CATEGORIES
────────────────────────────────────────

Getting Started
├─ Login and first-time setup
├─ Dashboard overview
├─ Running your first scan
└─ Basic navigation

Working with Findings
├─ Understanding findings
├─ Changing status
├─ Assigning tasks
└─ Adding comments

Using Optimizer
├─ Getting AI suggestions
├─ Testing on UAT
├─ Understanding metrics
└─ Downloading optimized SQL

Change Requests
├─ Creating change requests
├─ Approval process
├─ Deployment process
└─ Rollback procedures

Reports & Analytics
├─ Generating reports
├─ Report types
├─ Exporting reports
└─ Sharing reports

Troubleshooting
├─ Login issues
├─ Performance problems
├─ Error messages
└─ Contact support
```

### Getting Personal Support

**Slack Channel:**
```
#dbanalyser-help

Post your question:
- Screenshots help
- Describe what you're trying to do
- Team responds within 1 hour
```

**Email Support:**
```
support@dbanalyser.company.com

Include in email:
- Your name
- What you're trying to do
- Error message (if any)
- Screenshot (if possible)
- When you need help

Response time: Within 24 hours
```

**In-Person Help:**
```
Office hours:
- Every Tuesday 2-3pm in Meeting Room B
- DBA team available
- Bring your questions
- No appointment needed
```

**Phone Support:**
```
Critical issues only: +1-555-0199
(For when database is down)

Hours: 8am-6pm Monday-Friday
```

---

## 11. Quick Reference Guide

### Most Common Tasks

**Task 1: Find Problems in My Database**
```
1. Click "New Assessment"
2. Select your database
3. Click "Start"
4. Wait 5-15 minutes
5. See problems in dashboard
```

**Task 2: Fix a Problem**
```
1. Dashboard → Click [View]
2. Review Problem tab
3. Optimizer tab → Get Suggestion
4. Test on UAT → Review results
5. Submit Change Request
6. Get approvals
7. Deploy (DBA does this)
```

**Task 3: Assign Work to Someone**
```
1. Dashboard → Find problem
2. Click [Assign] button
3. Select person
4. Click "Assign"
5. They get notified
```

**Task 4: Check Status of My Work**
```
1. Dashboard → Filter "Assigned To: Me"
2. See all your tasks
3. Click any one to view details
4. Update status when needed
```

**Task 5: Check If Someone Approved My Change**
```
1. Left menu → Change Requests
2. Find your CR (search if needed)
3. See approval stages
4. Check if all 4 approved
```

### Keyboard Shortcuts

```
SYSTEM SHORTCUTS
────────────────────────────────────────
Ctrl+F            Search on page
Ctrl+P            Print current page
Ctrl+S            Save page (browser saves)
Escape            Close popup/modal

DASHBOARD SHORTCUTS
────────────────────────────────────────
Ctrl+N            New Assessment
Ctrl+H            Go to Help
Ctrl+,            Go to Settings
Ctrl+Shift+L      Logout
```

### Time-Saving Tips

**Tip 1: Bookmark Common Pages**
```
Bookmark in browser:
- Dashboard
- My Tasks (Finding list with filter)
- Reports page
- Help page

Access in 1 click instead of 5 clicks
```

**Tip 2: Use Email Notifications**
```
Get notification when:
- Task assigned to you
- CR needs your approval
- Scan completes

Don't check every 5 minutes - let app notify you
```

**Tip 3: Set Default Database**
```
Settings → Defaults → Default Database

Save time loading your main database
```

**Tip 4: Save Report Templates**
```
After creating a report you like:
- Click "Save as Template"
- Name it (example: "Weekly Summary")
- Next time: Just click template
- No need to re-configure

Saves 5 minutes per report
```

**Tip 5: Batch Process**
```
Instead of: 1 finding at a time
Do this: Get 5 suggestions at once
- Open 5 problems
- Get AI suggestion for each
- Review all at same time
- Submit CRs together

More efficient use of time
```

### Phone/Tablet Tips

**Responsive Design:**
```
DBAnalyser works on phones and tablets
No special app needed - just web browser

What works well:
✓ View dashboard
✓ Read finding details
✓ Add comments
✓ View reports

What's harder on small screens:
- Comparing side-by-side SQL code
- Using optimizer (small screen)
- Reviewing complex metrics

Recommendation:
Use desktop/laptop for detailed work
Use phone for quick check-ins
```

---

## 12. Glossary of Terms

**Assessment / Scan**
```
Process of analyzing your database to find problems
Takes 5-15 minutes
Creates finding records for each problem found
```

**Confidence Score**
```
0-100% rating of how sure the AI is about a suggestion
Higher = more reliable (aim for 70%+)
Lower = might be wrong (get second opinion)
```

**Change Request (CR)**
```
Formal, tracked request to change the database
Goes through 4 approval stages
Required before deploying to production
Allows rollback if problems occur
```

**Critical Severity**
```
🔴 Highest severity level
Fix immediately (within hours)
Database is broken or users can't work
```

**Dashboard**
```
Main control center / home page
Shows list of all findings
Filter, search, sort problems
Central place to manage work
```

**Data Integrity**
```
Means the data is correct and unchanged
When testing: verify same results from both versions
"Data Integrity: Verified" = Good! Safe to use
"Data Integrity: Failed" = Bad! Don't use this suggestion
```

**Deploy / Deployment**
```
Moving changes from safe/test environment to production
Making changes live so real users see them
DBA does this (not regular developers)
```

**Finding**
```
Single database problem found by system
Examples: slow query, missing index, schema issue
Each finding can have comments, history, status
```

**High Severity**
```
🟠 Second highest severity
Fix within 24 hours
Affects users' ability to work efficiently
```

**Low Severity**
```
🟢 Lowest severity level
Fix when convenient (no deadline)
Minor issue, doesn't affect daily work
```

**Medium Severity**
```
🟡 Middle severity level
Fix within 1 week
Affects performance or quality
```

**Ollama**
```
AI engine that powers the Optimizer
Runs locally (not in cloud)
Analyzes SQL and suggests improvements
```

**Optimization**
```
Improving something (usually making it faster)
Example: Making slow query run faster
Result: Better performance, happier users
```

**Rollback**
```
Undo a recent change
Used if deployment caused problems
Can only be done within 1 hour of deployment
```

**Status**
```
Current stage of a problem
Examples: Pending, In Progress, Approved, Deployed
Shows progress of fixing the issue
```

**UAT (User Acceptance Testing)**
```
Safe copy of production database
Used for testing changes before deploying
Real data, real conditions, but safe
No impact on real users
```

**Unassigned**
```
Problem that no one has been assigned to yet
Means it's not claimed by anyone
You can click [Assign] to take responsibility
```

---

## Support & Contact Information

**Quick Support Links:**

```
Help Center: In-application (left menu)
Email: support@dbanalyser.company.com
Slack: #dbanalyser-help
Phone (critical only): +1-555-0199
Office Hours: Tuesday 2-3pm, Meeting Room B
```

**What Information to Provide When Getting Help:**

```
Always include:
1. What were you trying to do?
2. What error message did you see?
3. Screenshot (if possible)
4. When did it happen?
5. Does it keep happening?

Example good report:
"I'm trying to test an optimization on UAT.
When I click 'Test on UAT', I get error:
'Cannot connect to UAT database'
This started today at 2pm.
I've tried 5 times, same error.
Screenshot attached showing error."
```

---

## Final Checklist Before You Start

```
Before using DBAnalyser, make sure:

☐ You have login credentials (username + password)
☐ You can access the web address (bookmark it)
☐ You have tested login (successful?)
☐ You've completed First-Time Setup (settings)
☐ You understand the 5 tabs (Problem/Solution/Help/Comments/History)
☐ You know how to view a finding
☐ You've read about the Optimizer
☐ You know what a Change Request is
☐ You saved this guide for reference
☐ You know how to get help (email/Slack/phone)

If all checked: You're ready to start! 🎉
```

---

**Document Version:** 1.0  
**Last Updated:** May 9, 2026  
**Next Review:** August 9, 2026

For questions or feedback about this guide, please contact: support@dbanalyser.company.com

---

**Happy optimizing! 🚀**
