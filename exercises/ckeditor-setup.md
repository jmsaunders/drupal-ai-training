# Exercise — CKEditor AI setup (Content format only)

Audience: Beginning Drupal users  
Admin theme: Gin  
Environment: Drupal.org AI Demo (Advanced Drupal Skills)

## Goal
Enable the AI buttons in the **Content** text format only, then verify them inside a real node.

---

## Part 1 — Enable AI buttons in the Content format

1) Go to **Configuration → Content authoring → Text formats and editors**  
   `/admin/config/content/formats`

2) Click **Configure** for the **Content** format.

3) **Editor appearance → Toolbar configuration**  
   - Add the **AI Assistant** group to the **Active toolbar**.  
   - If the AI actions appear as individual buttons, add the items listed in the table below.

4) **AI Tools** section  
   - Ensure **AI tools are enabled** for this format.

5) Click **Save configuration**.

### Buttons to enable

| Button | Required | Notes |
|---|---|---|
| Summarise | Yes | Produces a concise summary of selected text |
| Rephrase | Yes | Alternate wording while keeping meaning |
| Tone | Yes | Uses your **Tone** vocabulary if mapped in this format |
| Improve clarity | Recommended | Simplifies and tightens prose |
| Fix spelling and grammar | Recommended | Quick quality pass |
| Change length (shorter/longer) | Optional | Useful for teaser copy limits |

> Keep the set small for beginners. You can add more later.

---

## Part 2 — Sanity-check AI defaults (read-only)

1) Go to **Configuration → AI → Settings**  
   `/admin/config/ai/settings`  
   - Confirm there is a **Default provider/model** selected  
   - Keep **temperature** low for predictable outputs (eg. `0.2–0.4`)

> If fields are read-only in the demo, that’s fine; you only need to confirm a default is present.

---

## Part 3 — Test in a real node

1) Go to **Content → Add content → Basic page**  
2) Title: `CKEditor AI test`  
3) Body: paste a few paragraphs of any public article text (for practice)  
4) Select a paragraph, click **AI Assistant → Summarise**  
   - Review the output and keep or undo as you prefer  
5) Select a sentence, click **AI Assistant → Tone**, choose a tone, apply  
6) Save as **Draft**

### What good looks like
- The AI buttons appear for the **Content** format only  
- Summarise and Tone produce reasonable, readable results  
- You can reverse or edit AI changes as needed

---

## Checklist
- [ ] **Content** format shows AI buttons in the toolbar  
- [ ] Summarise and Rephrase work on selected text  
- [ ] Tone applies using your Tone vocabulary (if mapped)  
- [ ] Changes saved as **Draft** for human review

---

## Troubleshooting
- **No buttons:** Re-open the **Content** format and re-add the AI Assistant group to the toolbar.  
- **Buttons greyed out:** Ensure you are using the **Content** text format on the node form.  
- **No output:** The demo may be cold-starting. Retry the action after a few seconds.  
- **Tone list empty:** Map the Tone vocabulary in the **Content** format (AI Tools → Tone → Taxonomy vocabulary = Tone).

