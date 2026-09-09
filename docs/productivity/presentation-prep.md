## What it does

`presentation-prep` checks whether you can explain a product, proposal, or topic before you present it. It turns your planned explanation into the questions a real audience is likely to ask, then has you answer them one at a time and gives immediate feedback.

It tests **recall**, not recognition. The question form offers only an `I can't answer` choice and a free-text answer field. It never supplies candidate answers that let you guess from their wording or shape. One invocation covers one explanation, and feedback comes after all of its questions are answered.

## When to reach for it

You invoke this by typing `/presentation-prep`, and the [agent](https://www.aihero.dev/ai-coding-dictionary/agent) won't reach for it on its own.

Reach for it before a product demo, sales call, design review, stakeholder presentation, or any explanation where follow-up questions will expose whether you understand the material. Paste the explanation or outline you plan to use and name the audience.

| What you need | Reach for |
| --- | --- |
| Rehearse likely audience questions before presenting | `presentation-prep` |
| Sharpen a plan or decision before you commit to it | [grill-me](https://aihero.dev/skills-grill-me) |
| Learn a topic over several sessions | [teach](https://aihero.dev/skills-teach) |
| Collect answers from someone else | [to-questionnaire](https://aihero.dev/skills-to-questionnaire) |

## The audience-question queue

The leading idea is the **audience-question queue**. The skill extracts three to seven likely questions from your explanation and orders them by audience importance. The queue can cover value, mechanism, evidence, limitations, alternatives, cost, risk, or next steps, but it uses only the dimensions that fit the material.

Each answer gets one of five verdicts: correct, partly correct, incorrect, not verifiable, or could not answer. Once the queue is complete, feedback includes a concise answer you could give the audience and, where useful, the gap in the original explanation that made the question hard. The invocation then ends with a short readiness summary.

## Common questions

**Is this a multiple-choice quiz?**

No. `I can't answer` is the only supplied choice. Every substantive answer is free text, so the check measures whether you can retrieve and explain the answer yourself. This also avoids option-shape clues, such as the correct answer always being longer or more specific.

**How does it know whether my answer is correct?**

It uses your supplied material and trustworthy sources available in the conversation. If a claim needs evidence that is not available, the verdict is `Not verifiable`, with the missing source named. It should not turn the model's memory into a confident correction.

**Does it rewrite my presentation?**

No. It may identify a presentation gap when your explanation leaves an important audience concern unanswered, but its job is to test your understanding. Rewrite the presentation after the rehearsal, using the gaps it found.

**What happens if I choose `I can't answer`?**

You get the expected answer and an explanation without the choice being treated as a failure. The point is to expose the gap before the audience does.

**Can I move on to another explanation in the same invocation?**

No. Each invocation checks one explanation. Start another invocation when you are ready to rehearse a different explanation.

## It's working if

- The questions sound like your actual audience, not a generic trivia quiz.
- You have to formulate answers rather than spot them among distractors.
- Feedback separates factual errors from missing detail and unverifiable claims.
- Choosing `I can't answer` turns an unknown into a specific item to learn before presenting.
- The ending names both your strongest area and the highest-risk audience question.

## Where it fits

`presentation-prep` is a reach-for-it-anytime standalone used immediately before you explain something to other people. It follows preparation and precedes the real presentation; it does not create a lasting workspace or write files.

Its nearest neighbours are [grill-me](https://aihero.dev/skills-grill-me), which stress-tests the idea itself, and [teach](https://aihero.dev/skills-teach), which builds knowledge over multiple sessions. When you are unsure which skill fits, [ask-matt](https://aihero.dev/skills-ask-matt) routes you.
