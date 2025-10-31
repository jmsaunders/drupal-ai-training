# Session 1 — Introduction to AI in Drupal

Copyright © 2025 James Matthew Saunders and Rod Martin.  
Created with support from amazee.io and Promet Source.  
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

> Audience: **Beginning Drupal users**  
> Admin theme: **Gin**  
> Environment: **Drupal.org AI Demo environment (Drupal AI Demo)** — then “Drupal AI Demo” as shorthand

---

## Session goals
By the end of Session 1 you will:
- Understand how Drupal integrates AI in a human-in-the-loop way (no black boxes).
- Launch the **Drupal AI Demo** using **Advanced Drupal Skills**.
- Confirm an AI provider is active and responding.
- Use CKEditor AI to summarise and change tone in a page.
- Know where configuration lives so you can repeat this on your own.

---

## Part A — Quick orientation (5–10 minutes)

**Key idea:** Drupal treats AI as a set of services you configure and govern. Editors stay in control; AI assists.

**Concepts in one minute each:**
1. **AI Core** — shared UX and APIs that surface AI features.
2. **Providers** — where the model inference runs. Multiple providers supported.
3. **Recipes / Prompts** — repeatable instructions and settings for consistent output.
4. **Automators** — run tasks at save/bulk time, write into fields under editorial control.
5. **Agents** — guided actions that help editors or builders accomplish multi-step tasks.

> Principle: **People over prompts.** Define your workflow, then fit the model and recipe to it.

---

## Part B — Start the environment (Drupal AI Demo)

**Step 1. Open the demo site**
1. Visit: `https://drupal.org/ai/demo`
2. Choose **Advanced Drupal Skills**.
3. Click **Launch**. Wait for the site to open in your browser tab.
   - *TODO: screenshot — demo launcher page*

**Expected result:** You land on a Drupal CMS site with AI features preconfigured for evaluation.

**Troubleshooting:**
- If the site does not load, retry the launcher. Use a private window if you have stale cookies.

---

## Part C — Confirm the admin theme and navigation

**Step 2. Confirm Gin is enabled**
1. From the admin bar, go to **Appearance**.
2. Verify **Gin** is the default **Administration theme**.
   - *TODO: screenshot — Appearance showing Gin as admin theme*

**Expected result:** Admin pages have the Gin look and layout.

---

## Part D — Verify the AI provider responds

**Step 3. Check provider status**
1. Go to **Configuration → AI → Providers**.  
   Path: `/admin/config/ai/providers`
2. Locate the active provider card. Click **Test connection** (or equivalent).
   - *TODO: screenshot — Providers screen with “Test” control highlighted*

**Expected result:** A success message indicates the provider is reachable.

**If it fails:**
- Wait 10–15 seconds and test again. Demo backends can be cold-started.
- If still failing, switch provider (if available in the demo) and test again.

---

## Part E — First hands-on win in CKEditor (Summarise + Tone)

We will edit a page and use CKEditor AI actions. Keep changes in draft to preserve the demo content.

**Step 4. Open an existing page**
1. Go to **Content → Content**. Path: `/admin/content`
2. Find a **Basic page** with a few paragraphs. Click **Edit**.
   - *TODO: screenshot — Content listing with a page selected*

**Step 5. Summarise a paragraph**
1. In the body field, select a paragraph of 5–8 sentences.
2. In the CKEditor toolbar, click the **AI** icon and choose **Summarise**.
3. When the summary appears, choose **Insert** to replace the selection or **Insert below** to compare.
   - *TODO: screenshot — CKEditor AI menu open; Summarise highlighted*

**Expected result:** The selected paragraph is reduced to 1–2 concise sentences.  
**Validation:** Read for factual preservation and clear phrasing.

**Step 6. Change tone using taxonomy-backed Tone**
1. Keep the summarised text selected.
2. Click **AI → Tone**, then choose a tone (for example, *Plain language* or *Friendly*).
3. Apply the change and review the result.
   - *TODO: screenshot — AI → Tone menu*

**Expected result:** Wording shifts to the selected tone while preserving meaning.

> Note: Tone options and behaviour can be driven by a **Tone** taxonomy. We will set that up properly in a later session; for now, use the defaults provided by the demo.

**Step 7. Keep the page as draft**
1. Scroll to **Publishing options**.
2. Ensure **Published** is unchecked.
3. Click **Save**.

**Expected result:** Your edits are saved but not publicly visible. Editors maintain control.

---

## Part F — Where things live (so you can repeat this)

Use these paths to locate and adjust AI features on your own sites:

- **Providers:**  
  `Configuration → AI → Providers`  
  `/admin/config/ai/providers`  
  Test connections, select defaults, and review capabilities (chat, vision, embeddings, JSON).

- **Global AI settings:**  
  `Configuration → AI → Settings`  
  `/admin/config/ai/settings`  
  Confirm default models, temperature, and feature toggles.

- **CKEditor AI tools:**  
  `Configuration → Content authoring → Text formats and editors`  
  `/admin/config/content/formats`  
  Edit your format, then enable **AI** buttons in the toolbar and sidebar.

- **Permissions:**  
  `People → Permissions`  
  `/admin/people/permissions`  
  Grant AI actions only to roles that need them.

> Governance practice: enable AI features in **roles** used by trained staff; use drafts or review fields to keep humans in the loop.

---

## Part G — Quick wins checklist (2 minutes)

- [ ] Provider tests successful  
- [ ] CKEditor AI buttons visible in the toolbar  
- [ ] You produced one summary and one tone-adjusted paragraph  
- [ ] Your page was saved as **draft** (not published)

If any box is unchecked, flag it now. We fix blockers before moving on.

---

## What’s next (Session 2 preview)
In Session 2 we will:
- Review the modules behind these features.
- Confirm provider capabilities and defaults.
- Prepare the groundwork for **Automators** and **Recipes** so that structured, repeatable tasks write into fields editors can review.

---

## Attribution and licence
Copyright © 2025 James Matthew Saunders and Rod Martin.  
Created with support from amazee.io and Promet Source.  
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).
