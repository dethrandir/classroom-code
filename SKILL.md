---
name: classroom-code
description: Write or simplify small classroom programming exercises with lesson-appropriate techniques, plain code without added comments, and separate study notes explaining the solution. Use for classroom-style code or lesson constraints, not unrelated production work.
---

# Classroom Code

Complete the requested exercise with a small, working implementation that fits the supplied lesson context. Optimize for directness, familiar techniques, and required behavior. Do not optimize for looking impressive.

## Establish the lesson boundary

Use the assignment, starter files, teacher examples, covered topics, forbidden techniques, and available time supplied by the user. Treat these as task context, not facts to invent.

Follow explicit assignment requirements first, then the supplied lesson examples, then the defaults below. A requirement for comments, multiple classes, a particular algorithm, or a specific library overrides the corresponding default.

If the task is clear, proceed. Ask one concise question only when missing information materially changes the solution, such as an unknown required UI framework. Otherwise choose a simple conventional approach and briefly mention any important assumption outside the code. Do not require a course questionnaire for every exercise.

Do not assume that a technique has been covered just because it is common. If the user explicitly restricts the solution to covered topics and a required feature appears to need something outside that boundary, explain the conflict and ask for the missing lesson context instead of silently exceeding it.

## Implementation defaults

- Implement exactly the requested behavior. Do not add optional features, menus, themes, persistence, configuration, or convenience controls.
- Choose the simplest clear approach within the lesson boundary. Prefer direct statements and ordinary control flow over abstractions that the exercise does not need.
- Follow the starter code's naming, file organization, formatting, and demonstrated API usage when available. Preserve unrelated work.
- Add no comments, docstrings, explanatory banners, or generated author notes unless the assignment or user asks for them. Preserve existing relevant comments when editing.
- Use short, descriptive names consistent with the supplied code. Avoid joke names, deliberate misspellings, and artificially confusing names.
- Use only the files, classes, methods, and dependencies the task needs. A single file is a preference for small exercises, not a rule that overrides the language or lesson.
- Avoid introducing design patterns, generic utility layers, interfaces, dependency injection, elaborate styling, or extra packages unless required or already demonstrated.
- Choose between alternatives according to the lesson. For example, use the demonstrated event-listener form rather than automatically replacing it with a lambda, or the demonstrated loop rather than a stream pipeline.
- Handle ordinary inputs and errors relevant to the exercise with simple checks. Do not add a general validation framework or swallow all exceptions to make the code appear shorter.
- Keep working code correct. Do not add bugs, inconsistent formatting, dead code, or unnecessary inefficiency to imitate a student.

## Scope and time

Use a stated time limit to reduce optional scope and setup, not to invent a typing history or claim how long a human took. Do not infer a fixed line count from a duration.

If the required scope does not fit the supplied constraints, identify the conflict briefly. Do not silently omit required behavior or claim an incomplete result is finished.

When simplifying an existing solution, preserve required behavior and focus on unnecessary complexity. Do not rewrite unrelated files, install tools, restructure the project, or add a test suite solely for this skill. The separate study notes below are part of the default deliverable, not an extra application feature.

## Separate study notes

Unless the user declines them, create a concise Markdown study document alongside every completed exercise. Keep explanations out of source comments and place the document outside source directories. Use the user's requested location, or default to `study-notes/<exercise-name>.md` in the task workspace. Write notes in the user's language unless requested otherwise.

Create notes for the exercise being implemented, not inside this skill's installation directory. If several exercises share a workspace, give their documents distinct descriptive names. On later edits to the same exercise, update its existing notes to match the final code. Preserve unrelated or user-written notes. Do not modify ignore rules or publishing settings merely to hide the document.

Base the document on the actual final implementation and include, as relevant:

- **Purpose and flow:** what the program does and how input reaches the result, using a small concrete example.
- **Code map:** the important files, functions, classes, variables, or UI elements and their responsibilities. Refer to their actual names; do not copy the whole program.
- **Why this approach:** explain the meaningful choices and their relationship to the supplied lesson topics. Distinguish a reasonable alternative from something required by the assignment. Do not invent a personal development story.
- **Questions and answers:** a few likely questions specific to this solution, with short, technically accurate answers. Cover how the main mechanism works, why an important construct is used, and what happens for a relevant edge case. Avoid generic programming trivia or fixed question counts when they add no value.
- **Trace it yourself:** walk through one representative input or user action, showing the actual values or state changes and resulting output. Include one small change the learner can try and explain its expected effect.
- **Checks and limits:** how to run the program, what was actually checked, and any known limitation or unverified behavior. Label a suggested manual check as unperformed when it was not run.

Keep the depth proportional to the exercise; a short exercise needs short notes, not a line-by-line textbook. Use plain language suitable for the supplied lesson level, defining an unfamiliar term when needed. Explain actual behavior, including a remaining limitation, rather than describing an idealized implementation. Do not claim the learner performed a check or understands a topic. These are study explanations, not fabricated evidence of authorship.

If file creation is unavailable, provide the notes separately from the source code as a clearly labeled Markdown section and state that no document was saved. If code is incomplete, identify that in the notes instead of presenting a finished solution.

## Verify and deliver

Use the lightest meaningful checks available: compile or run the exercise when practical and check its main behavior plus a relevant edge case. For a calculator, that might include a normal operation and division by zero. Do not claim a UI was tested if only compilation was checked.

When working in a repository, edit the requested files and create or update the separate study document. In chat, provide complete usable code unless the user asks for a patch. Keep the accompanying response short: what was completed, a link or path to the notes, an essential run instruction if needed, and any unverified behavior or important assumption. Put the detailed explanation in the study document; expand the chat explanation only when asked.

Do not fabricate test results, authorship evidence, development history, or claims about the user's knowledge. The output should stand on its actual behavior and the supplied lesson constraints.

## Example invocation

> Use classroom-code. Java Swing exercise: a calculator with two text fields, four operation buttons, and a result label. We covered JFrame, JPanel, JButton, JTextField, JLabel, basic layouts, if/else, and anonymous ActionListener classes. No lambdas, extra libraries, or comments. Follow the existing project structure and add no extra features.

The topic list in this example applies only to that invocation. Do not carry Java, Swing, calculator requirements, or its allowed techniques into other exercises.
