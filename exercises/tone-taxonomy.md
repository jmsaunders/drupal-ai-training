# Exercise — Tone Taxonomy + CKEditor AI “Tone”

> Audience: **Beginning Drupal users**  
> Admin theme: **Gin**  
> Environment: **Drupal.org AI Demo environment (Drupal AI Demo)** — then "Drupal AI Demo" as shorthand

## Goal
Create a **Tone** vocabulary and wire it into **CKEditor AI → Tone**, then try it on a page.

---

## Part 1 — Map “Tone” into your text format

1) Go to **Configuration → Content authoring → Text formats and editors**.  
2) Click **Configure** for the **Content** format.  
3) In the **AI Tools** section, open **Tone** and set **Taxonomy vocabulary** to **Tone**.  
4) Tick **Use term description for tone description**.  
5) Click **Save**.  

> If your site doesn’t have a **Tone** vocabulary yet, add it under **Structure → Taxonomy → Add vocabulary**, then add a few tone terms (eg. “David Attenborough”, “Formal”, “Friendly”) with helpful descriptions.

---

## Part 2 — Try it in CKEditor

1) Go to **Content → Add content → Basic page**.  
2) Title: `Make this like David Attenborough`.  
3) In the Body, paste sample text. You can use this Forbes article as source content:  
   https://www.forbes.com/sites/nelsongranados/2024/05/31/how-artificial-intelligence-is-shaping-the-new-media-and-entertainment-economy/  
4) Select the text, open **AI Assistant → Tone**, choose **David Attenborough**, then click **Change the tone** and review the result.  
5) Save the page.  

### What good looks like
- The **Tone** dropdown appears in the editor.  
- The rewritten text reflects the selected tone and remains factual, readable, and accessible.  
- Editors can reference the tone **descriptions** you added to the vocabulary.

---

## Checklist
- [ ] **Tone** vocabulary exists with 3–5 clear options and helpful descriptions  
- [ ] **Content** text format has **AI Tools → Tone** mapped to **Tone** vocabulary  
- [ ] AI Assistant → Tone works on a Basic page

---

## Notes
- Keep temperature low in **AI Settings** for predictable tone changes.  
- Use Tone sparingly; always human-review before publishing.
