---
name: adr
description: Explicit-only router for ADR workflow commands. A dead simple engineering skill framework that works reliably.
disable-model-invocation: true
---

# ADR

Use this as one router skill. Follow the command the user invoked.

If the user invokes only `adr`, `$adr`, or `ADR`, run `adr adr` by default. Choose another route only when the request clearly asks for research, synthesis, a spec, intent, implementation, self-review, or recap.

Keep writing brief, direct, and human. No jargon, filler, or extra process.

Write all artifacts under project-local `./adr`. If `./adr` or the needed subdirectory does not exist, create it.

Use timestamp format `YYYYMMDD-HHMMSS`.

## `adr research`

Conduct a code-based research spike.

Only use web search if the codebase cannot answer the question.

Be systematic. Search with breadth and depth. Be diligent and unbiased.

Document the research in:

```text
./adr/research/SPIKE-{appropriate-name}-{timestamp}.md
```

If the research is large enough, or the user directs it, use multiple sub-agents. If the research requires multiple spikes, create multiple spike documents.

## `adr synthesize`

Review recent research that relates to the idea or discussion with the user.

Document the synthesis in:

```text
./adr/research/synthesis-{appropriate-name}-{timestamp}.md
```

## `adr spec`

Describe and declare a rough spec so the user can iterate toward a final decision.

Document the spec in:

```text
./adr/specs/{appropriate-name}-{timestamp}.md
```

Update the spec as the user iterates.

## `adr adr`

Create the formal ADR once the user says they are ready.

Use the current research, synthesis, spec, and discussion. Generate the ADR directly.

Document the ADR in:

```text
./adr/decisions/{number}-{appropriate-name}-{timestamp}.md
```

Write it in this shape:

```markdown
# {number}. {title}

Date: {YYYY-MM-DD}

## Status

Accepted

## Context

{What led to this decision.}

## Decision

{What was decided.}

## Consequences

{What changes because of this decision.}
```

## `adr intent`

State the intent of what was specified.

Write the what, why, and how in paragraph format. Start the intent with an action verb.
If there was any form of research, spike, synthesis or spec documentation, as well as an adr, append those paths to the end of the intent.

## `adr implement`

Use the previously stated intent. If there is no clear intent, state the intent first.

Then implement.

## `adr review`

Conduct a self-review of your code. Actively look for issues: bugs, duplications, oversights, edge cases, and anything that feels off. Trace through the logic systematically and flag anything that needs to be fixed or improved before moving on.

Assess reusability. Look for duplicated logic that should be shared or abstracted, unless there is a good reason not to.

Compare the implementation against the ADR. Look for clear divergences or issues.

## `adr recap`

Create a recap document that describes the full process: what was implemented, how it was implemented, and the reference files that were created.

Write the recap under:

```text
./adr/
```
