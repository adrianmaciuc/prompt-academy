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

**10 Engaging Exercises:**

1. Remove rows with missing values.
2. Delete rows where Age is not numeric.
3. Capitalize all names.
4. Validate emails.
5. Correct spelling mistakes.
6. Drop Purchase Amount > 999.
7. Replace empty Age with “Unknown.”
8. Convert dates to YYYY-MM-DD.
9. Add new column: Total with Tax (+10%).
10. Validate and fix Website Link column.


✅ Home Assignments for Day 1

**From Session 1: Prompt Variations**

- Create 5 variations of the same prompt by adding:
  - Persona (e.g., teacher, comedian, CEO)
  - Output style (bullet points, story, poem)
  - Scope (for kids, for experts)
  - Few-shot examples (good vs bad)

- Document how each variation changes the output.

**From Session 2: Messy Data Challenge**

- Generate your own messy CSV with the extra Website Link column.
- Write cleaning instructions in Markdown:
  - Include at least one custom rule (e.g., “Numbers bigger than 3 digits should not be in column X”).
  - Include a rule for fixing broken URLs.

- Prompt AI to clean the data according to your rules.
- Bonus: Ask AI to fetch additional info from the Website Link column (e.g., “Visit each link and summarize the homepage content”).
- Document what worked and what didn’t.

✅ Day 2 Agenda

### Session 1: AI for Different Fields

- Practice creating outputs for marketing, education, research.
- Summary: Patterns and best practices.

### Session 2: Ethics & Limitations

- Practice testing AI boundaries.
- Summary: Responsible use, bias, privacy.

✅ Resources to Share

**Beginner guides:**

- https://platform.openai.com/docs/guides
- https://learn.microsoft.com/en-us/copilot/

**Books:**

- AI Superpowers
- Human Compatible

**Free tools:**

- ChatGPT
- Bing Copilot
- Canva AI

✅ New Additions Incorporated:
- ✔ Practice-first approach
- ✔ Prompt layering exercise
- ✔ Messy CSV generation with Website Link column
- ✔ Markdown-based cleaning instructions
- ✔ Home assignments for prompt variations and data cleaning with link validation

