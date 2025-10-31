# Session 4 — Automators, Prompts, and Recipes

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

Audience: Beginning Drupal users  
Admin theme: Gin  
Environment: Drupal.org AI Demo environment (Drupal AI Demo)

---

## Session goals

By the end of this session you will:

- Understand **what Automators** do in Drupal’s editorial pipeline
- Understand **what Recipes** are and why they matter
- See how Drupal saves AI-assisted work into fields that humans control
- Learn where to manage Automator behaviour in your own sites

This session is **conceptual with demonstration**, because the AI Demo environment has limited access to Automator configuration.

---

## Part A — What Automators do

**Automators** allow AI to run **automatically** when content is saved, based on:
- Which fields are modified
- What transformations are configured
- Which model is set
- What rules are defined by the editor or site builder

Editor remains in control:
- Output goes into **specific fields**
- Editors review AI-generated changes before publishing
- Nothing is overwritten silently

---

## Part B — Where Automators live

Explore the configuration:

1. Go to  
   **Configuration → AI → Automators**  
   `/admin/config/ai/automators`

   *TODO: screenshot — Automators overview*

2. Look for automators enabled in the demo.

Expected:
- You see a list of automators already present in the demo environment

If none appear:
- The demo provider may be cold-started
- Refresh and revisit after 20–30 seconds

---

## Part C — Understand Automator execution

Open a Basic Page:

1. Go to  
   **Content** → click **Edit** on any existing page  
   `/admin/content`

2. Make a simple editorial change:
   - Add a sentence
   - Fix some punctuation
   - Adjust structure manually

3. Save **as draft**  
   (ensures human-in-the-loop control)

Expected result:
- If an Automator is active, Drupal may suggest or apply changes to a **separate field**, for example:
  - Suggest Title
  - Summarise Text
  - Simplify body language

*TODO: screenshot — Field showing automated output (if present)*

If nothing fires:
- Demo environment might not currently include active Automators
- Not a failure: helps illustrate variability of AI integration

---

## Part D — What Recipes are and why they matter

You tried tone changes and summarisation manually using CKEditor AI.

Those are:
- **Prompts**
- That editors must select each time

A **Recipe** is a reusable prompt with:
- Consistent output expectations
- Controlled tone, structure, and formatting
- Model and temperature settings locked in
- Optional Automator attachment

Example (conceptual):

> *When saving a press release, create a short teaser with a limit of 120 characters in a separate field, plain language.*  

Recipes reduce variability and avoid prompt drift.

Recipes enable:
✅ Repeatable outcomes  
✅ Governance  
✅ Editorial efficiency  
✅ Role-based control  

---

## Part E — Putting it together (in the real world)

In production Drupal sites:

| Who | Role |
|-----|-----|
| Editors | Use CKEditor AI actions |
| Content Designers | Define tone taxonomy and review AI outputs |
| Site Builders | Configure Automators and Recipes |
| Governance leads | Approve rules for AI changes |

AI helps at scale **without removing human accountability**.

---

## Troubleshooting

If automators are missing:
- Cold start: retry after a few seconds
- Provider limitation in demo environment

If outputs don’t appear:
- It’s expected that **not all** automators are enabled in this demo build

Message to trainees:
> The demo proves the concept. Actual production builds unlock the real workflow power.

---

## What’s next (Session 5 preview)

We will:
- Explore ethics and bias considerations  
- Ensure proper oversight of AI-assisted content  
- Align with accessibility best practices  

This strengthens the **human governance layer** before automation is expanded.

---

## Attribution and licence

Copyright © 2025 James Matthew Saunders and Rod Martin.  
Created with support from amazee.io and Promet Source.  
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).
