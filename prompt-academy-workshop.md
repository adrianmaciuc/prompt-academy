# Prompt Academy: Practical AI workshop for beginners

✅ Two-Day AI Training Workshop Plan

**Audience:**
Beginners with no prior AI experience.
**Goal:** Learn to use AI practically across any field.

✅ Structure

**Day 1 & Day 2**

- Session 1: 1 hrs
- Break: 60 min
- Session 2: 1.5 hrs

✅ Day 1 Agenda

### Session 1: Hands-On Prompt Techniques (50 min)

Start with The Grandfather riddle:
 `when I was 6 years old my grandfather was 10 times my age. now I am 10. two years ago he died. how old was he last year ? answer in one token.`
 follow up with 
 `now explain step by step`

- Basic Prompt: Ask a simple question. (The `Task`) (e.g., “Explain search engines”). 
    alternatives:
        - car engines
        - how planes fly
        - how apis work
        - what does cleaning data mean
        - what is prompt engineering
        - what is context window in ai
        - what is an mcp

- Add `Persona`: “Act as a kindergarden teacher, explain search engines” 
    alternatives:
        - university professor
        - a lawyer
        - a quality assurance engineer
        - a human resources manager
        - a senior developer

- Add Output Style (The `Format`): “Act as a kindergarden teacher, explain search engines, be short and concise”
    alternatives:
        - with as many details as possible 
        - in bullet points
        - as a short story
        - as a table
        - as a step by step guide
        - as a humorous explanation

- Add `Scope`: “Act as a kindergarden teacher, explain search engines for beginners in the tech industry, be short and concise”
    alternatives:
        - for people who already know a bit about tech
        - for high school students
        - for non-technical adults
        - for an architect in software development
        - for business executives

- `Few-Shot` Prompting: “Act as a kindergarden teacher, explain search engines for beginners in the tech industry
, be short and concise. here are some examples of good and bad analogies to help you:
  Examples:
  - Good: “A search engine is like a warehouse worker who helps you find and bring items quickly.”
  - Bad: “A search engine is a tool that retrieves indexed data from the internet.”

- `Negative Prompting`: “Act as a kindergarden teacher, explain search engines for beginners in the tech industry
, be short and concise. here are some examples of good and bad analogies to help you:
  Examples:
  - Good: “A search engine is like a warehouse worker who helps you find and bring items quickly.”
  - Bad: “A search engine is a tool that retrieves data from the internet.”
  . Do not use technical jargon or librarians analogies.”

- `step by step` chain of thought prompting: “Act as a kindergarden teacher, explain search engines for beginners in the tech industry
, be short and concise. here are some examples of good and bad analogies to help you:
  Examples:
  - Good: “A search engine is like a warehouse worker who helps you find and bring items quickly.”
  - Bad: “A search engine is a tool that retrieves data from the internet.”
  . Do not use technical jargon or librarians analogies. Explain step by step each of your ideas so I would understand better how a search engine works”


**Summary & Theory (10 min):**

- Why prompts matter.
- Key elements: `task`, `persona`, `format`, `scope`, `few-shot`, `negative`, `chain-of-thought`.
- Best practices for prompting.


### Session 2: Data Generation & Cleaning (30 min)

**Step 1: Generate Messy CSV**

AI Chat : Local, chatgpt.com or m365 copilot
Prompt:

Generate a CSV file with 200 rows of fictional customer data. Columns: Name, Email, Purchase Amount, Date, and Website Link. I need half of it to be accurate and half to be messy:

- Incomplete emails
- Missing values
- 5 or more words in name
- Numbers > 999 in Purchase Amount
- American and european date formats mixed
- Website Link column should have broken or incomplete URLs

**Step 2: Ask the AI to simply clean up the data**

**Step 3: Define “Clean” in Markdown**

Possible answer if no definition provided:
"The data cleaning process is complete. Note: After applying strict cleaning rules, the resulting file contains 0 rows. This means all rows in your original file had at least one critical issue according to the criteria set. If you want to relax the cleaning rules or review the issues found, let me know "

Participants create a `.md` file or just a prompt with custom cleaning rules. Example:

### Data Cleaning Instructions

- email format should be similar to eve.wilson@mailservice.com
- Remove rows where Purchase Amount > 999
- a name should be made out of one or two words
- only date format accepted 31/12/2024
- only link format accepted is with https

Examples of names

good name:
- Adrian Maciuc

bad name:
- AdriAN MaccIUC Rodriguez
- Ad@rian Maciuc
- Adrian

example of links:
good link:
https://example.com

bad link:
- link@site
- http://brokenlink


Then prompt AI:

Clean this CSV according to the rules in the markdown file.



## Session 3: Vibe Coding - Build your own tools (60 min)

Discuss briefly about the Planning Pattern

### Planning and agentic approach on executing tasks
- "help me develop a plan to build this app"
- "I need you to create a markdown file for instructions for an agent to build this app"
- "based on this plan, start writing the code for this app, try to be as simple as possible, if you can have it in one single file, do it. use javascript" 

Step 1: Create an app on chatgpt.com or on copilot. Choose an example from below. 

Step 2: Use the above planning steps to create a plan and then generate the code.

Step 3: Only I create an account on loveable.dev (free plan is enough) 

## ✅ Home assignment after Day 1:
- Choose any app from below, and build an app on loveable.dev


Example of tool to build:
### JSON Formatter & Diff Checker
(worked well in chatgpt - chatgpt hosted - react app)
Paste version A and version B. It formats both and highlights structural differences. A simple tree comparison engine, perfect for spotting sneaky API changes.

### Date/Time Globe Calculator
(worked well in chatgpt - chatgpt hosted - only js and html)
You pick a locale and a time zone and you pick a second locale . Entering a certain date and time in the past present or future and it provides the exact equivalent in the other locale and timezone, accounting for daylight savings and locale-specific formats.

### Create a daily to-do app for yourself where:
(worked well in chatgpt - chatgpt hosted - only js and html)
you can add tasks, remove tasks, mark tasks as done
you can add notes to tasks if needed
you can mark them partially done
you can generate at the end of the day a summary of all tasks done  

### Test Data Generator (Mini Edition)
(worked in vscode - copilot - local)
You choose a data type—email, phone number, username, date range, numeric bounds—and it spits out valid, invalid, and borderline values. It’s like a vending machine for edge cases.

### Tiny State Machine Visualizer
(worked in vscode - multiple inputs to fix - local)
You define states and transitions via quick text input, and it produces a diagram plus transition validation. Handy for spotting impossible or missing flows in UI logic.

### File Size Simulator
(worked in vscode - local only)
Purpose: Creates dummy files of specified size for upload tests.
Inputs: File size (KB/MB), file type.
Output: Generated file.
You can also create a dummy file as a csv file with x number of rows and y number of columns with random data inside

Other examples:

to TEST

### Data Anonymizer: Replace PII in CSVs with realistic but fake values or with encrypted values.

### Localization QA Tool: Side-by-side string comparison for locales with length warnings and missing keys.

### Voice Note Transcriber: Record short audio in-browser → transcribe to text

### Dependency Visualizer: Visual graph of package.json dependencies and quick risks.

### text extractor from images: upload images, it extracts all text from them and provides a structured output




### Network traffic analyzer
You enter an url, it fetches all the network calls provided and saves them in a structured way, for you to copy paste and compare with a second url 


### Duplicate Finder
Detects and lists duplicate entries in pasted data or CSV files.



✅ Day 2 Agenda

## Session 2:


