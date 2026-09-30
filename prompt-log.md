# Prompt log

## 2026-09-29
- Asked: Build the portfolio repository skeleton (README.md, RESUME.md, AGENTS.md, CLAUDE.md, prompt-log.md, .gitignore, and the capabilities, docs, data and analysis folders with a one-line README in each otherwise-empty folder); tailor AGENTS.md from my resume and the course baseline; write this first log entry; show every file before I commit.
- Produced: The full skeleton; AGENTS.md adapted from the course baseline with my field, my data rules and my explanation style added, the Naming section unchanged and the standing prompt-log rule verbatim; a one-line CLAUDE.md; placeholder README.md and RESUME.md; the requested .gitignore; this entry.
- What was wrong and how it was caught: My first message arrived without the resume. Claude noticed no resume text was present and the upload folder was empty, so it asked for the resume instead of guessing; I sent it in a second message. The resume uses a placeholder name and anonymized employers, so AGENTS.md names neither. My explanation-style preferences were inferred from the resume, so I need to check them against how I actually work.

- I am setting up a public GitHub portfolio repository named firstname-lastname for a
graduate business course. My resume is below the line. Do five things, then show me
every file before I commit anything.

1. SKELETON. Create this structure, with a one-line README.md inside every directory
   that would otherwise be empty, so git will track it:
     README.md, RESUME.md, AGENTS.md, CLAUDE.md, prompt-log.md, .gitignore
     capabilities/
     docs/briefs/  docs/decisions/
     data/
     analysis/figures/
   capabilities/ holds one folder per capability, each with README.md, spec.md and the
   model file. docs/briefs/ holds documents written BEFORE work begins; docs/decisions/
   holds recommendations written after. Do not create any folder named after a course,
   a semester, or a week.

2. AGENTS.md. Start from the baseline at
   https://adamwstauffer.github.io/ai-lms/ai-conventions.html and tailor it to me from
   my resume: name my field; list the kinds of data from my work that must never be
   pasted into a model (be specific to me - client records, patient data, government
   asset data, whatever applies); say how I want things explained; and keep the rule
   that you may not write my briefs, analyses, memos or reflections. Keep the Naming
   section word for word. Include this standing rule exactly:
     "At the end of every session that changed a file, append one entry to
      prompt-log.md: the date, what I asked, what you produced, what was wrong and how
      it was caught. Never backfill earlier sessions and never edit a past entry."

3. CLAUDE.md. One line: "Read AGENTS.md - it is the canonical file."

4. prompt-log.md. Write its first entry now, for this session, in that format.

5. README.md. Leave README.md as a single placeholder line - I write my  own bio.

.gitignore, one pattern per line: ~$*.xlsx  ~$*.xlsm  ~$*.docx  ~$*.pptx  .DS_Store
Thumbs.db

If you are a chat window without file access, give me each file in its own code
block and the github.com steps to create it.
Locating the missing resume before proceeding.

I'll pull the baseline conventions page and check whether your resume came through as a file.

Your resume didn't come through. The message ends at the instructions, and there's nothing in the upload folder, so there's nothing below the line for me to read. I did fetch the baseline conventions page, so that part is ready.

The resume is what makes the AGENTS.md tailoring specific to you (your field, the data from your jobs that must never go into a model, how you want things explained). It also gives me your name for the repo. Without it I'd be guessing at those sections, and the baseline warns that a file that could be anyone's is the failure to avoid.

Could you paste the resume text into your next message, or attach the file? Once I have it, I'll build the skeleton and all six files (including the exact standing rule and the first prompt-log entry), then show you every file's full contents before anything is committed.

Kate Zeis Resume Econ.docx
DOCX

GitHub has no "new folder" button. A folder only exists when it has a file in it, so you create a folder by creating a file whose name includes the folder.

On the website

Open your repository and go to the folder where you want the new one (or stay at the top level).
Click Add file, then Create new file.
In the filename box, type the folder name followed by a slash, for example capabilities/. When you type the /, GitHub turns the text into a folder path.
Keep typing the file name after the slash, for example capabilities/README.md. To make nested folders, add more slashes, like docs/briefs/README.md.
Type at least one line in the file (GitHub won't let you commit a completely empty file). This is why your skeleton has a one-line README in each folder.
Click Commit changes, write a descriptive message, and commit.

The folder now shows in your repository.

A few tips

Type the slash before the file name. If you type the whole name first and add the slash afterward, it can get messy.
To add a folder inside an existing one, first open that folder in GitHub, then click Add file, then Create new file. The path box already starts with that folder, so you only type the new part.
Follow your Naming rules: lowercase, hyphens, no spaces, and folders named after the work rather than a course, semester, or week.
If you only want to add files to a folder that already exists, open the folder and use Add file, then Upload files.

Since you already uploaded your skeleton, you'll mostly use this for new capability folders later, for example capabilities/your-capability-name/README.md, then add spec.md and the model file the same way.

Here is a problem:

https://adamwstauffer.github.io/ai-lms/case-perfect-competition.html

Here is my engagement brief:

## The problem
I own a small farm, and must decide the mixture of three crops that I will plant in my 64 beds. To work these crops, I have 720 hours of my own labor, and up to 1,440 hours 
of external paid labor. Each crop has a different planting price, requires a different amount of labor and fertilizer, and most importantly, will bring a different amount of 
revenue. Interestingly, each crop becomes less efficient to grow as I plant more. This diminishing efficiency (or rate of return) is also different for each crop. I have a
limited amount of funds for labor and fertilizer, and a limited amount of each crop that I can grow.

## What I am assuming
I am assuming that the fertilizer/bed cost is per season, and not weekly or monthly (or god forbid, daily).
I am assuming that the revenue per bed is per season.
I would want to verify both of these before building a model.

## Hypothesis
I expect the mix to be most profitable at 14 beds of tomatoes, 20 beds of carrots, and 30 beds of mesclun. This maxes out mesclun, taking advantage of the lower diminishing
rate of return. It then maxes out carrots, leaving only 14 beds for tomatoes. While tomatoes have the highest revenue for the original bed, I believe their very high rate
of diminishing return will make a larger number of tomato beds less profitable than the two other crops.

## How I would know I was wrong
I would know I was wrong if the model produces a more profitable mix.

Do not rewrite it and do not suggest
replacement wording.

1. Name every assumption I left implicit.
2. Name every claim I have not supported.
3. Ask me the three questions a client would ask.

Is my hypothesis falsifiable — could this model actually show it wrong,
or would any outcome be consistent with it?

I did not rewrite anything or offer replacement wording. The most important finding is under item 2: the mix you predict doesn't fit the labor limit as the case page states it.

1. Assumptions you left implicit
What "profitable" means. The brief never says what is subtracted from revenue. It could be fertilizer, the $20,000 fixed cost, and hired labor. It could also include a cost for your own 720 hours, which the case implies at $34.72/hr. The answer changes depending on whether those hours are free.
Prices don't move. The brief treats revenue per bed as constant however many beds you plant. That is the price-taker assumption behind P = MC, and the brief never states it. It also means diminishing returns act only through labor hours, not revenue.
Which limit binds. The mix assumes the 64-bed limit is what stops you. The brief never considers that labor or money could stop you first.
Whole beds. The brief assumes integer beds, while Solver's GRG method will return fractions.
Labor is interchangeable. The brief assumes hours can be moved freely across crops and between your labor and hired labor, and never says how hiring works (whole workers or any number of hours).
Idle beds. The brief doesn't say whether leaving a bed empty is allowed.
Certainty. It assumes no yield or price risk, no crop timing, and no rotation.
Where "1,440 hours" comes from. Your brief says up to 1,440 hours of paid labor. The case page says up to 4 workers at 1,440 hours each.
Where "planting price" and "limited funds" come from. Neither appears on the case page. If they come from your instructor's handout, fine. If not, you're importing constraints the case doesn't have.
2. Claims you haven't supported
The 14 / 20 / 30 mix is feasible. I ran the case's labor formula on it. Please verify these in your own spreadsheet, since they're drafts until you do. Roughly:
Tomatoes: about 4,785 hours
Carrots: about 983 hours
Mesclun: about 1,960 hours
Total: about 7,727 hours, against 6,480 available with 4 workers (720 + 4 × 1,440)
Under your own reading of 1,440 total paid hours, the capacity is only 2,160
On the case page's numbers, that mix can't be the most profitable one, because it can't be planted at all.
Ranking crops by diminishing-returns rate decides the mix. You order the crops by rate alone. Nothing in the brief compares what the last bed of each crop earns net of fertilizer and labor. A low rate doesn't help if the crop earns little per hour.
Tomatoes lose to the other two at scale. The brief says a large number of tomato beds becomes less profitable than carrots or mesclun. It never says at what number, or what the comparison is.
The 64-bed limit is the binding constraint. This is asserted, not shown.
Your two seasonal assumptions. You say you'd verify them, but not against what, or how the hypothesis changes if you're wrong.
3. Three questions a client would ask
What does "profitable" include, and how many dollars of profit do you expect from your mix?
Which of my limits is actually stopping me, and what would it be worth to loosen it?
If one of your assumptions is wrong, how much money is at stake, and how would I find out before I plant?
Is the hypothesis falsifiable?

In principle, yes. It names a specific mix, and a model could show it wrong, which is more than the case's bad example ("a balanced mix") can claim. It has three weaknesses.

It can fail before any optimizing. The feasibility check above means it may fail on constraints alone, which suggests the brief wasn't tested against the case's numbers.
It has no tolerance. "A more profitable mix" means one bed off, or $1 better, counts as wrong. Solver will likely return fractional beds, so you haven't defined what "wrong" versus "close" means.
It tests the numbers, not your reasoning. Your brief names a mechanism, tomato diminishing returns. The model could return a different mix while the mechanism is right, or your mix could turn out right for other reasons. The brief doesn't say which outcome would count against the mechanism.

A test is also only as clear as the model behind it. If your model includes a funds constraint or a different worker setup than you state, "more profitable" becomes ambiguous.

Your case page and your AGENTS.md both say to log an AI critique session in prompt-log.md. When you do, note that the hours figures came from me, and how you checked them.
