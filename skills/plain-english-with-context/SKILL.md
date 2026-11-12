---
name: plain-english-with-context
description: Use when explaining findings, technical concepts, plans, reviews, status, or recommendations, or drafting comments and tickets in plain English with enough context.
---

# Plain English with Context

Write for an informed reader who may not know the specific system. Make the answer understandable on its first read.

## Structure and context

- **Lead with the answer.** Start with the direct answer or main finding. Skip introductory filler such as "Here is an explanation of..." Answer each question the user asked.
- **Supply the background the reader needs.** Explain what the relevant thing is, why it exists, and how it relates to the question before using it in a technical explanation. Adjust the detail to what the reader already knows.
- **Explain cause and effect.** Connect the finding to its reason and practical consequence: what happens, why, and what it means for the user's goal or decision.
- **Use concrete examples when they help.** Choose a small example that makes the explanation easier to understand. State any assumptions; do not invent system behavior to make an example work.
- **Stay concise but complete.** Preserve necessary context, reasoning, and material caveats. Prefer short, connected paragraphs. Use lists for distinct items or steps and tables for comparisons.
- **Choose a structure that explains the relationship.** Use a form that helps the reader understand what happens and why. Tables help when comparing items against shared criteria; a sequence, worked example, or before-and-after explanation may make a process or change clearer. Check whether the structure reveals the relationship or merely organizes category names and descriptions. Avoid imposing one repeated format on different kinds of explanation.
- **Keep the focus on the question.** Include implementation details when they help understanding or a decision. Use these principles to shape the answer, without imposing these headings or a fixed template on every response.

## Clarity and vocabulary

- **Use familiar words and direct verbs.** Define unavoidable technical terms when first introduced, including terms used inside definitions. Use the same term for the same thing throughout the answer.
- **Replace vague shorthand with its meaning.** For words such as "bounded," "boundary," and "gate," say what is limited and by how much when known, which components or responsibilities are separate, or which check must pass before which action. If a relevant limit is unknown, say so.
- **Make labels refer to something the reader can identify.** Distinguish a category or field name from its contents. “Available options and selected result” does not say what the options are or whether a choice has been made. Supply a relevant instance, value, or short explanation, and state the point in the process when it matters. Distinguish an input, proposal, confirmed choice, and final output as needed. Short labels are fine when the surrounding material makes them clear; do not expand every familiar noun or invent values merely to sound concrete.
- **Explain dense technical phrases.** Replace strings of technical nouns with a short explanation of what the components do and how they relate. Preserve exact names, versions, numbers, code, and quotations when they matter, and explain them in the surrounding prose.
- **Keep sentences and paragraphs focused.** Aim for one main idea per sentence and one topic per paragraph. Prefer active voice, naming who or what performs the action. Keep the language natural rather than splitting every thought into fragments.
- **Make instructions easy to follow.** Put necessary conditions before the action and separate distinct actions into steps.

These vocabulary and sentence principles draw on selected ASD-STE100 ideas. Apply them flexibly, preserving technical accuracy and necessary context. This is adapted guidance, not a claim of ASD-STE100 compliance. See the [official ASD-STE100 FAQ](https://www.asd-ste100.org/STE_faq.html) for its scope.

## Evidence and conclusions

- **Separate evidence from interpretation.** Distinguish verified behavior, assumptions, inferences, proposed changes, and things not yet checked. Cite supporting evidence close to the claim when assessing factual findings.
- **Match the conclusion to the evidence.** State where and under what conditions an outcome was verified. A passing staging test supports a claim about staging; it does not by itself establish a production fix or prove the cause of a failure.
- **Test the explanation, not just the wording.** For a potentially ambiguous phrase, answer “What exactly does this refer to here?” and, when relevant, “What exists or has happened at this point?” using the material available to the reader. If the answer relies on your intended meaning, replace or explain the phrase. A label that sounds relevant, a matching quotation, or a completed checklist does not establish understanding.
- **Name remaining gaps.** When assessing a solution, state whether it addresses the whole requirement and explain what remains. Describe a partial fix as partial and an unverified outcome as unverified. Explain what the uncertainty means for the user's decision.
- **Connect status to the goal.** Explain what is complete, what remains, and any established blockers. For assigned actions, name the owner and action when known. Identify the user's actions only if actually assigned or required; label suggested actions as suggestions.

## Hypothetical examples

**Vocabulary and complexity**

Dense: "Worker replica scaling necessitates MCP initialization budget reconfiguration."

Clear: "Each worker (a process that handles requests) needs service connections before it can accept requests. In this example, a fixed limit controls how many connections can be set up at once. Each worker gets an equal share. Adding workers reduces that share, so new workers may take longer to become ready. Increasing the limit may help them connect sooner."

**Evidence and conclusions**

Vague: "The new update should fix the memory leak, so we can close the ticket."

Clear: "Version 2.1 passed the staging test that previously reproduced the memory leak. This suggests the update addresses the leak, but its effect on production crashes is unverified. Suggestion: monitor production memory use and crash logs for 24 hours before deciding whether to close the ticket."

## Final check

Before sending, silently check: does the answer address every question, and can the reader understand the answer, its reason, its practical effect, and any material uncertainty on the first read? Remove filler and repetition without removing context or overstating the evidence.
