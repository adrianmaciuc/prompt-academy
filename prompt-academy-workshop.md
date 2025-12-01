# Prompt Academy: Practical AI workshop for beginners

✅ Two-Day AI Training Workshop Plan

**Audience:**
Beginners with no prior AI experience.
**Goal:** Learn to use AI practically across any field.

✅ Structure

**Day 1 & Day 2**

- Session 1: 1.5 hrs
- Break: 60 min
- Session 2: 1.5 hrs

✅ Day 1 Agenda

### Session 1: Hands-On Prompting Basics (Practice First)

**Practical Flow (75 min):**

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


**Summary & Theory (15 min):**

- Why prompts matter.
- Key elements: `task`, `persona`, `format`, `scope`, `few-shot`, `negative`, `chain-of-thought`.
- Best practices for prompting.


### Session 2: Data Generation & Cleaning

**Step 1: Generate Messy CSV (Fun & Realistic)**

AI Chat : Local, chatgpt.com or m365 copilot
Prompt:

```text
Generate a CSV file with 500 rows of fictional customer data. Columns: Name, Age, Email, Purchase Amount, Date, and Website Link. I need half of it to be accurate and half to be messy:

- Typos in names
- Incomplete emails
- Wrong characters in numeric columns
- Missing values
- Random symbols in Age
- Numbers > 999 in Purchase Amount
- Website Link column should have broken or incomplete URLs
```

**Step 2: Define “Clean” in Markdown**

Possible answer if no definition provided:
"The data cleaning process is complete. Note: After applying strict cleaning rules, the resulting file contains 0 rows. This means all rows in your original file had at least one critical issue according to the criteria set. If you want to relax the cleaning rules or review the issues found, let me know "

Participants create a `.md` file or just a prompt with custom cleaning rules. Example:

### Data Cleaning Instructions
```md
- Remove rows where Purchase Amount > 999
- a name should be made out of two words - no special characters
- age should be a number between 1 and 90
- email format should be similar to eve.wilson@mailservice.com
- only date format accepted 31/12/2024
- only link format accepted is with https

Examples of names

good name:
Adrian Maciuc

bad name:
AdriAN MaccIUC
Ad@rian Maciuc
Adrian

example of links:
good link:
https://example.com

bad link:
link@site
http://brokenlink
``

Then prompt AI:

```
Clean this CSV according to the rules in the markdown file.
```

**From Session 2: Messy Data Challenge**

- Generate your own messy CSV with the extra Website Link column.
- Write cleaning instructions in Markdown:
  - Include at least one custom rule (e.g., “Numbers bigger than 3 digits should not be in column X”).
  - Include a rule for fixing broken URLs.

- Prompt AI to clean the data according to your rules.
- Bonus: Ask AI to fetch additional info from the Website Link column (e.g., “Visit each link and summarize the homepage content”).
- Document what worked and what didn’t.




✅ Day 2 Agenda

### Session 1: Vibe Coding - Build your own tools

Discuss briefly about the Planning Pattern

Planning and agentic approach on executing tasks
- Use an AI and ask it to create a prompt for an agent to build
"help me develop a plan to build this app"
"i need you to create a markdown file for instructions for an agent to build this app"
"based on this plan, start writing the code for this app, try to be as simple as possible, if you can have it one single file, do it" 

Example of tool to build:
(worked well in chatgpt - chatgpt hosted - react app)
JSON Formatter & Diff Checker
Paste version A and version B. It formats both and highlights structural differences. A simple tree comparison engine, perfect for spotting sneaky API changes.

## Date/Time Globe Calculator
(worked well in chatgpt - chatgpt hosted - only js and html)
You pick a locale and a time zone and you pick a second locale . Entering a certain date and time in the past present or future and it provides the exact equivalent in the other locale and timezone, accounting for daylight savings and locale-specific formats.

## Test Data Generator (Mini Edition)
(worked in vscode - copilot - local)
You choose a data type—email, phone number, username, date range, numeric bounds—and it spits out valid, invalid, and borderline values. It’s like a vending machine for edge cases.

## Tiny State Machine Visualizer
(worked in vscode - multiple inputs to fix - local)
You define states and transitions via quick text input, and it produces a diagram plus transition validation. Handy for spotting impossible or missing flows in UI logic.
Other examples:

## Create a daily to-do app for yourself where:
(worked well in chatgpt - chatgpt hosted - only js and html)
you can add tasks, remove tasks, mark tasks as done
you can set reminders for tasks that popup at a certain time
you can add notes to tasks if needed
you can mark them partially done
you can generate at the end of the day a summary of all tasks done  


to TEST

## Network traffic analyzer
You enter an url, it fetches all the network calls provided and saves them in a structured way, for you to copy paste and compare with a second url 

## Screenshot Comparator
Purpose: Compares two screenshots for pixel differences.
Inputs: Two image files.
Output: Difference percentage or highlighted diff image.

## Duplicate Finder
Detects and lists duplicate entries in pasted data or CSV files.

## File Size Simulator
Purpose: Creates dummy files of specified size for upload tests.
Inputs: File size (KB/MB), file type.
Output: Generated file.
You can also create a dummy file as a csv file with x number of rows and y number of columns with random data inside

### Session 2:


