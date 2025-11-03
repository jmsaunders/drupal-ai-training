# Exercise — Summarise selected text in CKEditor

Audience: Beginning Drupal users  
Admin theme: Gin  
Environment: Drupal.org AI Demo (Advanced Drupal Skills)

## Goal
Use **AI Assistant → Summarise** to condense selected body text on a Basic page, then review and save as a draft.

---

## Prerequisites
- The **Content** text format has AI buttons enabled (see “CKEditor AI setup” exercise).
- A default AI provider/model is present (read-only is fine in the demo).

---

## Part 1 — Prepare a Basic page
1) Go to **Content → Add content → Basic page**.  
2) Title: `Summarise test`.  
3) In **Body**, paste a few paragraphs from a public source you’re allowed to use for practice.

Tip: For best results, paste at least 3–5 paragraphs of coherent prose.

---

## Part 2 — Summarise selected text
1) Select a paragraph (or multiple paragraphs) in the editor.  
2) Click **AI Assistant → Summarise**.  
3) Wait for the response, then review what changed:
   - Key points preserved
   - Shorter and clearer
   - No invented facts (“hallucinations”)

4) If needed, undo and try again on a smaller or larger selection.  
5) Optionally apply **Rephrase** or **Improve clarity** to polish the result.

---

## Part 3 — Save for human review
1) Set **Moderation state** to **Draft** (if moderation is enabled).  
2) Click **Save**.

What good looks like:
- The summary is materially shorter and easier to read.  
- Meaning and facts are preserved.  
- No accessibility regressions (eg. headings remain headings).

---

## Optional — Content Suggestions panel
If **Content Suggestions** are enabled in your site:
- Open **Suggestions** and try **Readability** and **Suggest title**.
- Compare the suggested title against your original and pick the clearest.

---

## Checklist
- [ ] AI Assistant → Summarise is available in the **Content** format  
- [ ] Summaries are concise and accurate  
- [ ] Draft is saved for human review  
- [ ] (Optional) Suggestions used to improve readability/title

---

## Troubleshooting
- **No AI buttons:** Re-check **Configuration → Content authoring → Text formats and editors → Content** and add the AI Assistant group to the toolbar.  
- **No output:** The demo may be cold-starting; try again after a few seconds.  
- **Over-compressed result:** Summarise smaller selections or run **Improve clarity** instead of another summary.
