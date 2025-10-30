# Session 4 — Automators, Prompts, and Recipes

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

## Concepts
- Automators run modelled tasks at save/bulk time (e.g., rewrite, tag, translate).
- Recipes are reusable, named prompts plus model settings.
- Prompt engineering: be specific, provide context tokens, and constrain output format.

## Hands-on pattern: Simplified Text
- Add Simplified Title and Simplified Body fields.
- Attach Automators with prompts that:
  - Rewrite title to about 6th-grade level and wrap in <h2>
  - Rewrite body using limited tags and emit strict JSON for multi-field updates

## Good practice
- Test prompts manually first via the sidebar.
- Write to separate fields to protect human edits.
- Use low temperature for deterministic output.
- Document each automator’s purpose and scope.
