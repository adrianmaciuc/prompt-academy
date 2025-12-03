# Prompt Academy — Practical AI Workshop for Beginners

✅ Two-Day Hands-on Workshop

**Audience:** Beginners with no prior AI experience

**Goal:** Learn practical ways to use AI across workflows and small tools

## Day 1 — Agenda (overview)

- Session 1: 🧠 Hands-On Prompt Techniques (≈50 min)
- Break: ☕ 60 min
- Session 2: 🛠️ Data Generation & Cleaning (≈30 min)
- Session 3: 💡 Vibe Coding — Build your own tools (60 min)

### Session 1 — Hands-On Prompt Techniques (50 min)

Start with a warm-up puzzle to surface reasoning style:

> Puzzle: when I was 6 years old my grandfather was 10 times my age. now I am 10. two years ago he died. how old was he last year ? (answer in one token)

Follow up: `now explain step by step`

Learning objectives

- Understand prompt building blocks: Task, Persona, Format, Scope
- Practice few-shot and negative prompting
- Try chain-of-thought styles safely (step-by-step explanations)

Practical exercises (examples to run in class)

- Basic Prompt (The `Task`): Ask a simple question (e.g., “Explain search engines”). Alternatives:
  - car engines, how planes fly, how APIs work, what does data cleaning mean, what is prompt engineering, what is context window in AI, what is an MCP

- Add `Persona` (change tone): e.g., “Act as a kindergarten teacher, explain search engines”. Alternatives: university professor, lawyer, QA engineer, HR manager, senior developer

- Add `Format` (output style): short & concise, long detailed, bullet points, short story, table, step-by-step guide, humorous

- Add `Scope`: eg. “for beginners in the tech industry” or tailor for high-school students, non-technical adults, architects, or executives

- `Few-Shot` prompting: give 1–2 examples of good/bad outputs to steer style

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


**Summary & Theory (10 min)**

- Why prompts matter
- Key elements: `task`, `persona`, `format`, `scope`, `few-shot`, `negative`, `chain-of-thought`
- Best practices and common pitfalls

### Session 2 — Data Generation & Cleaning (30 min)

Goal: generate messy data, define cleaning rules, and ask AI to clean it.

Step 1 — Generate Messy CSV (class prompt)

Prompt idea (AI Chat: local, chatgpt.com, or M365 Copilot):

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

- Email should look like `eve.wilson@mailservice.com`
- Remove rows where Purchase Amount > 999
- Names must be 1–2 words and contain no special chars
- Accept only date format `31/12/2024`
- Website link must use `https`

If no rules provided, prompt the class to discuss what “clean” should mean (and show the example fallback message about 0 rows after strict cleaning).

Examples (for class discussion):

- Good name: Adrian Maciuc
- Bad names: AdriAN MaccIUC Rodriguez, Ad@rian Maciuc, Adrian
- Good link: https://example.com
- Bad link: link@site, http://brokenlink

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


