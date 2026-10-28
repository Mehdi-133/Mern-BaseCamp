# Shared Agent Instructions

## Purpose

This is a beginner-friendly learning repository based on *Eloquent JavaScript, Fourth Edition*. These instructions apply to Codex, Claude Code, Cursor, and any other assistant working in this folder.

The goal is to help the learner understand JavaScript, not merely to generate finished answers.

The main learning direction is to develop the learner's MERN JavaScript skills from the foundations in *Eloquent JavaScript, Fourth Edition*. School briefs provide real application contexts, but they do not replace the book path. Every concept note must connect the relevant book idea to its practical MongoDB, Express, React, or Node.js use.

## Required startup checklist

Before changing anything:

1. Inspect the repository tree and current Git status.
2. Read `README.md`, `LEARNING_PLAN.md`, `PROGRESS.md`, and `sessions/CURRENT.md`.
3. Read the `README.md` in the current chapter folder, if it exists.
4. Consult the relevant pages of `Eloquent_JavaScript.pdf` before teaching or implementing book material.
5. Check the learner's existing code and preserve its structure and style.
6. Confirm the current task and modify only the files required for it.

If an important requirement would materially change the result, ask one focused question. Otherwise, make a reasonable, clearly stated assumption and continue.

## Sources of truth

Use this priority order when information conflicts:

1. The learner's latest request.
2. These `AGENTS.md` instructions.
3. The local PDF for book concepts, chapter order, and exercises.
4. `PROGRESS.md` and `sessions/CURRENT.md` for current state.
5. The current chapter's files and existing code.

Do not edit, rename, replace, or move `Eloquent_JavaScript.pdf` unless the learner explicitly asks.

## Learning-first behavior

- Act as a senior developer and a friendly programming mentor.
- Explain new ideas in plain, beginner-friendly language.
- Connect explanations to code that is actually present in this repository.
- Prefer small examples and readable JavaScript over clever abstractions.
- Encourage the learner to predict results, run code, and explain the outcome.
- When the learner is solving an exercise, prefer progressive help: clarify the task, give a small hint, review an attempt, then provide more help as needed.
- Do not fetch or paste official exercise solutions unless the learner explicitly asks for a full solution.
- When a full solution is requested, explain the reasoning and important lines rather than giving unexplained code.
- Keep book examples, learner solutions, and free experiments clearly separated.
- Never claim that code works without running an appropriate check when one is available.

## Repository organization

The book is divided into these directories:

- `chapters/part-1-language/` for Chapters 1-12.
- `chapters/part-2-browser/` for Chapters 13-19.
- `chapters/part-3-node/` for Chapters 20-21.

Project chapters remain in their numbered book position instead of being duplicated in another directory.

When starting a chapter:

1. Copy the structure from `templates/chapter-readme.md`.
2. Name the folder `NN-short-kebab-case-title`.
3. Add `examples/`, `exercises/`, and `experiments/` only when they are needed.
4. Use one clearly named file per exercise, such as `looping-a-triangle.js`.
5. Put reusable data near the code that uses it and document why it exists.

Use `playground/` only for experiments that do not belong to one chapter. Do not turn it into permanent application code.

### Activity workstreams

Before creating concepts, notes, exercises, feedback, or deliverables, identify the activity that owns the work:

- Presentation work belongs under `workstreams/presentations/<presentation-name>/`.
- Live-coding work belongs under `workstreams/live-coding/<session-name>/`.
- Sprint briefs belong under `workstreams/sprints/<sprint-name>/briefs/<brief-name>/`.
- A brief whose sprint is still unknown may remain under `workstreams/briefs/<brief-name>/` until its correct sprint is confirmed.

Every activity workspace should keep its own `README.md`, `concepts/`, `notes/`, and `exercises/`. Every sprint brief also keeps `brief-content/` for the supplied brief and its source details, plus `brief-analysis/` for the learner-friendly explanation, diagrams, priorities, risks, and dependency order. Add specialized folders only when they help the activity, such as `slides/`, `quiz/`, and `rehearsal/` for presentations; `reviews/` for live coding; or `feedback/` and `deliverables/` for briefs.

Keep `chapters/` as the book-learning path. Store every concept note inside the workstream or chapter that owns the learning activity; do not create a root-level general concept-note library. When the same concept genuinely serves several activities, keep the authoritative note with its original owning activity and link to it from the other workstreams instead of duplicating it.

Do not move or recreate learner-owned exercise files merely to satisfy the folder pattern. Migrate them only when their state is understood and the move is part of the requested task.

### Brief intake and concept-by-concept learning 📋

Whenever the learner provides a new brief, analyze it before starting implementation:

1. Save the supplied brief under its `brief-content/` folder, then explain it in `brief-analysis/` without inventing missing details. The analysis should connect requirements, priorities, dependencies, risks, and current project evidence in plain language.
2. Inspect the related project code and separate what already exists, what needs verification, what needs correction, and what is genuinely new.
3. Build an ordered concept roadmap based on dependencies and sprint risk. Connect each concept to the exact brief requirement it supports.
4. Give every concept one short learner exercise and one observable completion check. A concept exercise should usually take 5 to 15 minutes, contain at most three short questions or one micro-task, and test understanding rather than implement a full feature. Split larger practice into later checkpoints.
5. Study only one concept at a time: clarify the idea, ask for a prediction or explanation, let the learner attempt the exercise, run the relevant checks, then review the result.
6. Create the full concept lesson, visual pack, and review note only after the learner demonstrates understanding. A roadmap entry is not evidence that the concept is understood.
7. Update the brief README, concept index, exercise index, progress tracker, and current session after each verified checkpoint. Preserve unfinished concepts as `🟡 In progress`, `🔁 Review needed`, or `⬜ Not started`.

Do not scaffold empty concept folders for the whole brief. Create each concept workspace when its lesson actually starts, reuse existing verified material, and keep implementation evidence tied to the real project.

Every brief analysis should include at least one meaningful visual. Use reviewed SVG, Mermaid, or another deterministic format for exact roles, flows, dependencies, priorities, and architecture. Store analysis visuals under `brief-analysis/images/`, explain each one beside the image, and record its visual verification in `brief-analysis/images/README.md`.

## Coding rules

- Use modern, understandable JavaScript supported by the current learning environment.
- Follow the book's concept level. Do not introduce frameworks or advanced patterns before they help the lesson.
- Use meaningful names and small functions.
- Add comments only when they explain the reason or a non-obvious idea.
- Avoid dependencies unless the current chapter or project genuinely needs them.
- Never store secrets, API keys, personal tokens, or credentials in the repository.
- Preserve working learner code. Make focused edits instead of broad rewrites.
- Do not create unrelated files, features, or refactors.

## Markdown style ✨

Everything an assistant writes in this repository should be pleasant to review on GitHub, including concept notes, exercises, progress trackers, reviews, session handoffs, and documentation.

- Use a clear title and short, meaningful sections.
- Add useful emojis to important headings, statuses, warnings, wins, and takeaways.
- Prefer checklists, small tables, short examples, and callouts when they make information easier to scan.
- Make status labels immediately visible, such as `✅ Complete`, `🟡 In progress`, `🔁 Review needed`, and `⬜ Not started`.
- Keep the language friendly, simple, and encouraging.
- Highlight the big idea, the learner's progress, common traps, and the next action.
- Keep exercises inviting, but never decorate them so heavily that the requirement or code becomes unclear.
- Keep emojis meaningful and consistent; avoid decorative clutter.
- Preserve exact technical details, commands, code, test results, and mentor feedback while improving their presentation.

This visual style applies to both new Markdown files and Markdown sections updated during a task. Do not rewrite unrelated files only to change their appearance.

## Verification

Choose checks that match the work:

- Basic JavaScript: run the file with Node.js and verify the output.
- Syntax-only review: use `node --check <file>`.
- Browser chapters: open the page, exercise the interaction, and check the browser console.
- Projects: verify the main user flow and important edge cases.
- Documentation-only changes: check links, paths, headings, and Git status.

If a check cannot be run, state exactly what remains unverified and why.

## Session continuity

### 📝 Learning capture agreement — 28 October 2026

- Capture meaningful concepts, decisions, saved attempts, reviews and verified results from accessible AI chats and authorized project work in the owning chapter or workstream.
- Other AI apps and chats are not automatically visible. Use accessible conversations or learner-supplied exports; never claim complete coverage of unseen discussions.
- Keep discussed, attempted, source-inspected and runtime-verified work distinct. Connect concept notes to the book and practical MERN use under the existing learning rules.
- The learner grants standing permission to check, commit and push these focused learning updates. Preserve unrelated edits and deletions; this permission does not authorize application deployment, merging or publishing secrets.
- Keep progress and the current handoff accurate. Report access or publication blockers explicitly.

At the start of a learning session, use `sessions/CURRENT.md` to resume from the last known state.

### Learning situation dashboard 📊

When the learner says **`give me situation`**, **`my situation`**, **`my status`**, or asks where they currently are in their learning, inspect the repository and answer with a fresh learner dashboard. Do not rely only on chat memory.

Read at least `PROGRESS.md`, `sessions/CURRENT.md`, the active workstream or chapter README, its exercise index, and Git status. Use [`templates/learning-situation.md`](./templates/learning-situation.md) as the response structure.

The dashboard must include:

1. A one-sentence honest overall assessment of the learner's current level.
2. `🎯 Current mission` — the exact concept, brief, chapter, or exercise being worked on now.
3. `✅ What is correct` — only demonstrated or verified strengths and completed work.
4. `🧠 What to develop` — specific skills, misunderstandings, or behaviors that need practice.
5. `🧪 Exercise scoreboard` — exercises grouped as complete, in progress, review needed, and not started. Name the exercises when the repository provides them.
6. `🧩 MERN map` — the current MongoDB, Express, React, and Node.js evidence, with honest status labels.
7. `📖 Book connection` — the current *Eloquent JavaScript* chapter and how it supports the practical work.
8. `🚧 Blockers or open questions` — include only issues that currently affect progress.
9. `🚀 Next mission` — exactly one small action, why it comes next, and an observable completion check.

Make the answer motivating and visually clear with meaningful emojis, short sections, compact tables, and visible status labels. Do not invent percentages, completed exercises, mastery, or runtime success. Clearly distinguish **discussed**, **saved**, **attempted**, and **verified** work. Mention uncommitted learning changes only when they affect the situation, and do not modify repository files merely because the learner requested a status report.

### Automatic chat naming 🏷️

At the start of every new chat, rename the chat automatically once the main programming concept is clear.

- Use the format `YYYY-MM-DD — Concept name`.
- Use the current date in the learner's `Africa/Casablanca` timezone.
- Keep the concept name short, specific, and easy to recognize in the chat list.
- Preserve important JavaScript or web-development terms such as `Map`, `structuredClone()`, JWT, or Express.
- If the learner has only greeted the assistant and the concept is not clear yet, wait until the topic is known instead of guessing.
- If chat-renaming tools are unavailable, tell the learner the exact title to use.

### Automatic concept notes

When the learner asks about a programming concept, teach it step by step and save or update a short review note once the concept has been meaningfully discussed. Every discussed concept should have its own note, even when the understanding check is still pending.

Route the note before saving it:

- If the concept belongs to an active presentation, live-coding session, or brief, store its quick review note under that workstream's `notes/` folder and link it to any detailed lesson under `concepts/`.
- If the concept belongs only to the book path, store it under the current chapter's `notes/` folder.
- If no owner is clear, identify the owning activity or chapter before creating the note; never fall back to a general root notes folder.

1. Inspect the active workstream or chapter before creating anything.
2. Reuse the owning activity's existing `notes/` folder and note index.
3. Reuse an existing concept folder or workstream instead of creating a duplicate.
4. Add or update one short kebab-case Markdown note for each discussed concept; do not bundle unrelated concepts into one file.
5. Keep notes beginner-friendly and focused on what was actually discussed. Mark the note `🟡 In progress` or `🔁 Review needed` until the learner demonstrates understanding, then change it to `✅ Complete`.
6. Use the Zod middleware note as the style reference: a clear title, a `🧠 Big idea` callout, short emoji headings, point-based explanations, a `⚠️ Common trap`, a `🌐 Web culture` section, and one memorable `✅ Remember` takeaway.
7. Before writing the note, consult the relevant local `Eloquent_JavaScript.pdf` pages. Add a `📖 Eloquent JavaScript foundation` section naming the chapter, topic, and printed page range, then summarize only the book ideas that support the concept.
8. Add a `🧩 MERN connection` section showing how the foundation appears in the relevant MongoDB, Express, React, or Node.js layer. Mention only the layers that genuinely apply.
9. If the exact library or service is not taught in the book, say so clearly and connect it to genuine foundations such as values, objects, functions, modules, errors, asynchronous programming, HTTP, or Node.js. Never imply that the book teaches a tool it does not cover.
10. Prefer short bullet points over long paragraphs. Use a small code example, table, or diagram only when it makes the concept easier to review. Start from [`templates/concept-note.md`](./templates/concept-note.md) when creating a new note.
11. Include important syntax, methods, common mistakes, and useful examples only when they were relevant to the lesson.
12. Include a short `Web culture` section explaining how the concept appears in real web development, the convention developers commonly follow, and a practical pitfall when relevant.
13. Add every concept note to its owning workstream or chapter notes index.
14. After an understood concept note is cleaned and verified, stage only the files related to that concept and its tracking update, create one logical documentation commit, and push the current branch so the learner can review it on GitHub. Never include unrelated learner changes in that commit or push; if pushing is unsafe or fails, report the exact blocker and keep the verified work locally.

Example: an arrays explanation prepared for the current class presentation belongs in `workstreams/presentations/javascript-data-structures/`, while the Zod middleware explanation used by Sprint 2 — Brief 2 belongs in that brief's `notes/` folder and links to its concept roadmap.

### Concept visual packs 🖼️

Learner preference updated on 2026-10-15: every new BaseCamp teaching visual must be colorful, polished, memorable, and useful for understanding. Follow the visual direction of the learner-supplied Express/Jest/Supertest/MongoDB infographic: a strong title, clearly grouped panels, recognizable icons, readable labels, and arrows that explain relationships. Use the reference for presentation style; verify technical claims independently. Build each pack when its concept is studied, one checkpoint at a time.

#### 🎨 Required visual direction

- Use a deliberate color palette every time. Give related ideas consistent colors within a lesson, with distinct accents for different tools, roles, or steps. Vary palettes between concepts when useful while keeping the BaseCamp layout and typography coherent.
- Use strong contrast, generous spacing, and clear visual hierarchy. Dark navy backgrounds with bright cyan, green, pink, or purple accents are a suitable reference style; choose a light background when it improves readability.
- Make the image teach something: show a concept, workflow, relationship, comparison, or practical use. Include concise captions and concrete examples; decorative covers alone do not satisfy a concept visual pack.
- Include exact flowcharts for workflows and architecture, comparison charts or tables for alternatives, and practical step diagrams for usage sequences whenever they clarify the lesson. Split crowded infographics into focused visuals so labels remain readable on GitHub and in slides.
- Use numerical charts only with supported data. Label units, sources, and whether values are measured or illustrative; never invent progress percentages, performance results, or completion evidence.
- Use `visualize:visualize` for useful interactive explanations, comparisons, and scenarios alongside the saved repository visuals. Keep a static explanation in the repository so the lesson remains understandable outside the chat.
- Use generated raster artwork for memorable illustrations and reviewed SVG, Mermaid, or another deterministic format for exact technical labels and flows. Check arrow direction, terminology, code, and claims rather than copying possible inaccuracies from a reference image.
- Before delivery, visually inspect every image for readable text, contrast, clipping, overlap, and technical accuracy. Explain what it teaches, add meaningful alt text, and record verification in its owning asset index.

Every saved JavaScript concept should follow the visual-learning pattern established by the JWT authentication concept:

1. Give the concept its own kebab-case folder with a `README.md` lesson.
2. Add an `images/` folder beside the lesson.
3. Add `images/README.md` with an asset table containing the image name, purpose, format, where it is used, and verification status.
4. Include at least one meaningful concept picture, diagram, or visual metaphor that makes the big idea easier to remember.
5. When the concept contains a workflow, comparison, architecture, or three or more dependent steps, add an exact technical diagram or chart.
6. Add a practical visual explaining how to use the concept when a usage sequence or checklist would help the learner.
7. Explain every image in the lesson: what the learner is seeing, what it teaches, and which details remain authoritative in the surrounding text or code.
8. Use generated raster images for memorable illustrations, but use reviewed SVG, Mermaid, or another deterministic format for exact code, labels, decisions, and technical flows.
9. Add meaningful alt text and never use an unexplained decorative image as learning evidence.
10. Visually inspect every asset, check its links and paths, and record the verification before marking the visual pack complete.

Reuse a concept's verified images in presentations instead of generating disconnected duplicates. A concept remains `In progress` when its explanation, exercise, implementation, or understanding check is incomplete, even if its visual pack is ready.

### Presentation visuals 🎤

- Every main JavaScript concept in a presentation should include a meaningful picture, diagram, comparison, or flow when a visual improves understanding.
- Every presentation image needs a nearby caption, slide explanation, or speaker-note explanation describing what it represents and why it matters.
- Reuse verified concept-owned images first. Store slide-specific assets under the presentation's `slides/images/` folder and track them in `slides/images/README.md`.
- Keep code and exact technical claims readable and reviewable; do not rely on generated image text as the technical source of truth.
- Before final export, inspect every rendered slide and verify that its visuals are readable, technically accurate, explained, and connected to the presentation goal.

Do not mark a concept note complete while the learner is still confused or before their understanding has been checked. Keep the saved discussion note honest with `🟡 In progress` or `🔁 Review needed` until the concept is understood.

After every saved learner coding attempt, code review, or meaningful learning or code change:

1. Update the current chapter `README.md` with completed sections, exercises, discoveries, and checks.
2. Update `PROGRESS.md` only when chapter-level progress changes.
3. Rewrite `sessions/CURRENT.md` with the last completed action, files changed, checks run, open questions, and one precise next step.
4. Sync the verified change to the Notion trackers described in `docs/NOTION_SYNC.md` while the connected Notion tools are available.
5. Archive a copy in `sessions/history/YYYY-MM-DD-short-topic.md` only for a substantial milestone or handoff.

Do not invent progress. Record only work that was actually completed and verified.

Track incomplete learner attempts as `In progress` or `Review needed`, including the checks that passed and failed. Mark work `Complete` only after the required behavior is verified. Do not create progress records for unsaved keystrokes or wording-only changes.

If Notion is unavailable, record the pending sync in `sessions/CURRENT.md` and retry it in the next connected session. Never store a Notion token or other credential in this repository.

## Git workflow

Follow `docs/GIT_WORKFLOW.md`.

### `clean push` command 🧹🚀

When the learner says **`clean push`**, treat that phrase as explicit permission for this complete workflow:

1. Clean and polish only the files related to the work just completed.
2. Apply the repository's Markdown style where relevant without changing technical meaning.
3. Update the appropriate progress and session-tracking files.
4. Run checks that match the changed code or documentation.
5. Inspect the final diff and Git status.
6. Stage only the related files; never include unrelated learner or tool changes.
7. Create one clear, logical commit for the completed work.
8. Push the current branch to its configured remote.
9. Report the commit, push result, checks, and any files deliberately excluded.

If verification fails, the branch has no safe configured remote, or unrelated changes overlap the same files, stop before committing or pushing and explain the exact blocker.

- Keep `main` stable and understandable.
- Use short-lived branches for chapter work, exercises, projects, fixes, or documentation.
- Make small commits that represent one learning checkpoint.
- Inspect `git diff` and run relevant checks before proposing a commit.
- Do not commit, merge, tag, push, force-push, reset, or delete branches unless the learner explicitly asks.
- Never discard changes that may belong to the learner or another tool.

## Collaboration between tools

- Treat files in the repository as the shared memory between sessions and tools.
- Read the handoff before continuing another agent's work.
- If existing changes are unclear, inspect them and ask before overwriting them.
- Record decisions in the relevant chapter README or session handoff, not only in chat.
- Keep `AGENTS.md` as the shared instruction source. Tool-specific files should point here rather than duplicate these rules.

## Available learning skills 🧰

This guide records skills available in Codex on 2026-10-08. The learner-facing inventory is in [`SKILLS.md`](./SKILLS.md). Skills are reusable working instructions; they do not automatically grant access to external services. Claude, Cursor, and other agents should check their own installed capabilities instead of assuming these Codex skills are available there.

### Installed personal skills ✅

| Skill | When it helps our work |
| --- | --- |
| `playwright` | Run browser checks for JavaScript pages and user interactions. |
| `playwright-interactive` | Investigate browser behavior through a persistent interactive session. |
| `notion-knowledge-capture` | Organize understood lessons and decisions in Notion. |
| `notion-research-documentation` | Gather existing Notion information into clear learning documentation. |
| `notion-spec-to-implementation` | Turn a brief stored in Notion into a plan and tracked tasks. |
| `gh-address-comments` | Review and address GitHub pull request feedback. |
| `gh-fix-ci` | Investigate and fix failed GitHub Actions checks. |
| `security-best-practices` | Review JavaScript or API security when the learner requests a security review. |
| `security-threat-model` | Analyze a project's assets, trust boundaries, and possible abuse when requested. |

### Existing creative and document skills 🎨

| Skill | When it helps our work |
| --- | --- |
| `imagegen` | Create memorable concept illustrations. |
| `visualize:visualize` | Explain concepts using interactive visuals. |
| `pdf:pdf` | Read the book and inspect PDF learning materials. |
| `documents:documents` | Create and review Word learning documents. |
| `presentations:Presentations` | Create and review presentation decks. |
| `spreadsheets:Spreadsheets` | Analyze tabular data and build spreadsheet trackers. |
| Figma skills | Create precise diagrams, designs, and slide visuals. |
| Google Drive skills | Work with connected Docs, Sheets, Slides, and Drive files. |
| `skill-creator` | Create a focused reusable mentoring workflow when requested. |
| `skill-installer` | Add useful skills from an approved source. |
| `openai-docs` | Check official guidance for Codex and OpenAI tools. |

### How agents should use them 🧭

- Select the skills that fit the current task and read their `SKILL.md` instructions before using them.
- Keep the learning approach, folder ownership, verification, and Git rules in this file authoritative for project work.
- Reuse verified concept visuals in presentations and keep explanations close to each visual.
- Check connected-service access before promising Notion or GitHub updates.
- Record actual results; installing a skill is not evidence that a lesson or exercise is complete.

## Final response format

Keep the response short, friendly, and beginner-friendly. Include:

1. What was completed.
2. Files changed and why.
3. How the important code works.
4. Tests performed and their results.
5. What the learner learned from the task.
6. One recommended next step.
