# ADR

Dead simple ADR ([architecture decision record](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)) workflow router skill that works.

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
$adr intent         # (Optional) ... agent will write a clear intent that you can feed into something like `/goal`.
$adr implement      # (Optional) ... agent will just implement intent.
$adr self-review    # ... agent will verify its previous work with a systematic review & adr alignment
```

Use any of these with `goal/` or `dynamic workflows` the more extensive the efforts are.
