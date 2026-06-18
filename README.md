# ADR

Dead simple ADR (architecture decision record) workflow router skill that works.

## Install

```bash
npx skills add backnotprop/adr
```

## Skill
```bash
$adr research       $USER{this new idea against the code}
$adr synthesize     # ... agent will orient towards implementation.
$adr spec           # ... agent will craft into plan.
$adr                # ... agent will write formal decision record.
$adr intent         # (Optional) ... agent will write a very clear intent that you can copy and feed into something like `/goal`.
$adr implement      # (Optional) ... agent will just implement intent.
$adr self-review    # ... agent will verify its previous work with a simple review.
```
