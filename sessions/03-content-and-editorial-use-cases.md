# Session 3 — Content and Editorial Use Cases

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

> Audience: **Beginning Drupal users**  
> Admin theme: **Gin**  
> Environment: **Drupal.org AI Demo environment (Drupal AI Demo)** — then "Drupal AI Demo" as shorthand

## Session goals
By the end you will:
- Use CKEditor AI to summarise and rephrase with confidence
- Configure a Tone vocabulary and wire it into the editor
- Enable Content Suggestions for titles and readability
- Keep changes in draft so editors stay in control

---

## Part A — CKEditor AI: quick wins you can repeat

**Step 1. Open a page for editing**
1) Go to **Content → Content** (`/admin/content`).  
2) Pick a Basic page and click **Edit**.
   - *TODO: screenshot — Content list with a page selected*

**Step 2. Summarise a paragraph**
1) Select 5–8 sentences in the Body field.  
2) Click **AI** in the toolbar → **Summarise**.  
3) Insert the result **below** your selection to compare.  
   - *TODO: screenshot — CKEditor AI menu with Summarise*

**Expected result:** A concise 1–2 sentence summary that preserves facts.  
**Validation:** Read both versions aloud. The meaning should match.

**Step 3. Rephrase for clarity**
1) Select the same text.  
2) AI → **Rephrase** → choose **Plain language** or **Simpler**.  
3) Insert and evaluate.  
   - *TODO: screenshot — Rephrase variants*

**Guardrail:** Do not publish yet. Keep the page in draft.

---

## Part B — Tone with taxonomy (editor-friendly control)

We will create a **Tone** vocabulary so editors can steer voice consistently.

**Step 4. Create a “Tone” vocabulary**
1) **Structure → Taxonomy** (`/admin/structure/taxonomy`).  
2) **Add vocabulary** → Name: `Tone`. Save.  
   - *TODO: screenshot — New vocabulary form*

**Step 5. Add tone terms with guidance**
Add at least four terms. In each **Description**, write guidance for the model. Examples:

- **Plain language**  
  “Use short, clear sentences. Avoid jargon. Target Grade 6 reading level.”
- **Friendly**  
  “Warm, helpful, encouraging. Use ‘you’ and active voice. Keep it concise.”
- **Formal**  
  “Professional and neutral. No contractions. Avoid colloquial phrasing.”
- **My voice**  
  “Match Matthew’s direct style. No emojis. Rarely use em dashes. Canadian spelling.”

Add more as needed for your organisation’s style.  
- *TODO: screenshot — Term edit with description guidance*

**Step 6. Wire Tone to your text format**
1) **Configuration → Content authoring → Text formats and editors** (`/admin/config/content/formats`).  
2) Edit the format used by Basic page (e.g., Basic HTML).  
3) In the AI settings for the format, select **Tone vocabulary: Tone**.  
4) Ensure the **AI** toolbar group is present.  
5) Save.  
- *TODO: screenshot — Text format wired to Tone vocabulary*

**Expected result:** CKEditor AI → Tone now shows your Tone terms.

**Step 7. Apply tone in the editor**
1) Reopen your page if closed.  
2) Select text. AI → **Tone** → choose **Plain language** or **Friendly**.  
3) Apply and compare with the original.  
- *TODO: screenshot — Tone dropdown showing your terms*

**Validation:** The message stays the same, voice changes to match the term description.

---

## Part C — Content Suggestions for titles and readability

**Step 8. Enable Content Suggestions**
1) Same text format screen as Step 6.  
2) Enable **Content Suggestions**:  
   - **Readability**  
   - **Summarise Text**  
   - **Suggest Title**  
3) Save.  
- *TODO: screenshot — Content Suggestions toggled on*

**Step 9. Use Suggestions**
1) In the editor sidebar, open **Suggestions**.  
2) Click **Readability** on a paragraph.  
3) Click **Suggest Title** for the whole page.  
- *TODO: screenshot — Suggestions panel*

**Expected result:** Practical hints that an editor can accept or ignore, always under control.

---

## Part D — Keep humans in the loop

**Step 10. Save as draft**
1) **Publishing options** → **Published** unchecked.  
2) **Save**.  

**Policy tip:** Use separate **review fields** or a workflow state so generated text is reviewed before publishing. This keeps accountability with your editorial team.

---

## Troubleshooting

- **AI buttons not visible:** Ensure the correct **text format** is assigned to the content type and the AI group is added to the toolbar.  
- **Tone list empty:** Make sure the **Tone** vocabulary is selected in the text format and at least one term exists.  
- **Suggestions not appearing:** Confirm the Content Suggestions checkboxes are enabled in the text format.  
- **Provider test fails:** Re-run the test under **Configuration → AI → Providers**. Cold starts are common in demo environments.

---

## What’s next (Session 4 preview)
You will attach **Automators** to run structured tasks at save time:
- Simplified Title
- Simplified Body
- Strict output formats for reliable updates

---

## Attribution and licence
Copyright © 2025 James Matthew Saunders and Rod Martin.  
Created with support from amazee.io and Promet Source.  
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).
