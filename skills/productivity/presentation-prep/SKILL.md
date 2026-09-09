---
name: presentation-prep
description: Check whether you can explain a product or topic before presenting it by answering likely audience questions.
disable-model-invocation: true
argument-hint: "What are you going to explain, and to whom?"
---

Rehearse the questions an audience is likely to ask after hearing the user's explanation. This is a comprehension check, not a presentation-writing exercise.

Conduct the session in the user's language. Translate the UI labels below while preserving their meaning.

## 1. Establish the explanation

If the invocation already names the topic, use it. Otherwise ask:

> What are you planning to explain, and who will hear it? Paste the explanation, outline, or product description you plan to use.

Use one free-text field. The answer should give enough detail to identify the audience's likely assumptions, objections, and knowledge gaps. Ask one short follow-up only when the audience or explanation is too unclear to generate useful questions.

## 2. Build the audience-question queue

Extract the questions a real listener would probably ask. Prioritise questions that test whether the user understands what they are presenting, not trivia or presentation style.

Cover only the dimensions relevant to the material:

- the core claim and audience value
- how it works
- evidence and examples
- limitations, tradeoffs, and failure cases
- alternatives and differentiation
- adoption, cost, risk, and next steps

Keep a queue of three to seven questions, ordered by audience importance. Tell the user how many questions you found and show their short titles, but do not reveal expected answers.

Base expected answers on the user's material and trustworthy sources available in the current context. When correctness depends on a fact not established by those sources, verify it with available tools. If it still cannot be established, do not guess.

## 3. Ask the questions

Use the harness's structured question UI to present each audience question one at a time. For every question, provide:

- one explicit choice: **I can't answer**
- a free-text custom answer field

Do not provide candidate answers. The user should retrieve and formulate the answer, not recognise it from a list.

Record the user's answer and continue through the queue until all three to seven questions have been answered. Do not evaluate or explain an answer while the queue is still open.

## 4. Evaluate and explain all answers

After the user answers the final question, evaluate every answer. Present one result for each question using this shape:

```
### <question title>

**Verdict:** Correct | Partly correct | Incorrect | Not verifiable | Could not answer

**Why:** <what was accurate, missing, mistaken, or unverifiable>

**A strong answer:** <a concise answer the user could give to the audience>

**Presentation gap:** <optional: what the original explanation should make clearer>
```

Judge substance rather than wording. Accept different answers when they are accurate and answer the audience's concern. Never turn uncertainty into a confident correction:

- **Correct:** accurate and sufficient for the likely audience.
- **Partly correct:** the core is right, but an important condition, mechanism, or limitation is missing.
- **Incorrect:** a material claim conflicts with the explanation or a verified source.
- **Not verifiable:** the available material cannot establish the answer. Name the source or evidence needed.
- **Could not answer:** the user selected **I can't answer**. Explain the answer without treating the choice as a failure.

## Readiness summary

End with a brief readiness summary:

- what the user could explain accurately
- which gaps should be resolved before presenting
- the highest-risk audience question, if any

End the skill after the summary.
