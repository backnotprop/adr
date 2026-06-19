# ADR

Dead simple ADR ([architecture decision record](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)) workflow router skill that works.

## Install

```bash
npx skills add backnotprop/adr
```

## Skill
In your own personal workflow, <br/>
when all you want is an ADR for whatever you've decided:
```bash
$adr                # adr doc gets created
```

### In a more streamlined approach:
_Use any of these with `goal/` or `dynamic workflows` the more extensive the efforts are._

```bash
$adr research       $USER{this new idea against the code}
$adr synthesize     # ... agent will orient towards implementation.
$adr spec           # ... agent will craft into plan.
$adr                # ... agent will write formal decision record.
                    # ... tell the agent to implement it after
                    # or:
$adr intent         # ... agent will output a clear intent
                    # ... that you can feed into something like `/goal`.
                    # ... or prompt into a dynamic workflow,
$adr self-review    # ... agent will verify its previous work
                    # ... with a systematic review & adr alignment
```

### There are no rules. You can skip, hop, merge, and do whatever:<br/>

```bash
$adr synthesize/spec Together to shape an implementation for us.
```

### You will end up with a directory shape like:

```
 adr/
  ├── README.md
  ├── decisions/
  │   ├── 0001-record-architecture-decisions.md
  │   ├── 0002-build-a-focused-coding-orchestrator-agent.md
  │   ├── ...
  │   ├── 0023-build-multi-agent-operations-view-from-task-state-20260618-145801.md
  │   └── 0024-run-parent-agent-as-managed-background-task-20260618-193203.md
  ├── research/
  │   ├── SPIKE-claude-monitor-capabilities-20260618-012732.md
  │   ├── SPIKE-event-streams-and-renderers-20260618-110007.md
  │   └── SPIKE-parent-tool-call-tracing-20260618-084045.md
  └── specs/
      ├── multi-agent-operations-view-20260618-145355.md
      ├── parent-agent-wait-and-durable-run-20260618-074619.md
      └── run-event-stream-contract-20260618-110147.md

  Mental model:

  adr/
  ├── README.md              # index of accepted decisions
  ├── decisions/             # final accepted ADRs, numbered forever
  ├── research/              # investigation notes before decisions
  └── specs/                 # draft plans/specs before decisions
```





