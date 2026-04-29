# Session 5 — Ethics, Bias, and Accessibility

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

> Audience: **Beginning Drupal users**  
> Admin theme: **Gin**  
> Environment: **Drupal.org AI Demo environment (Drupal AI Demo)** — then "Drupal AI Demo" as shorthand

---

## Session goals

By the end you will:
- Recognise where bias can appear in AI-assisted content
- Apply review techniques to maintain factual integrity
- Ensure text generated through AI meets accessibility expectations
- Understand Drupal’s governance controls for responsible use

---

## Part A — Bias in output and how to detect it

AI models **predict** text based on training data. They do not:
- Understand truth
- Know your organisation’s values
- Automatically represent people fairly

**Common risks in editorial use:**
- Overconfident inaccuracies
- Culturally loaded assumptions or stereotypes
- Unexplained technical terms
- Excessive reading levels

**Exercise:**  
Take a paragraph you summarised earlier. Ask:
- Is the meaning still correct?
- Is any group over-generalised?
- Is anything oversimplified in a harmful way?

If yes:
- Edit manually
- Mark for review
- Do not publish until corrected

---

## Part B — Accessibility is not optional

AI may:
- Remove headings
- Flatten lists
- Introduce dense phrasing
- Produce long sentences

Tools to validate accessibility:

1) **Enable Content Suggestions**
   - Check **Readability**
   - “Grade level” is a proxy: aim for plain language
   Path:
   `/admin/config/content/formats`

2) **Manual editorial checklist**
   - Reading level appropriate?
   - Headings structured correctly?
   - Descriptive links?
   - Short paragraphs?
   - Active voice?

If an AI step makes accessibility worse:
> Reject it. Human governs final copy.

---

## Part C — Ensure governance: humans always decide

**Drupal’s advantage:**
- AI output can be kept in **draft**
- Reviews are built into publishing workflow
- Permissions limit who can use AI tools

**Checklist:**
- Edits saved as **draft**
- AI actions restricted to trained roles
- Final publish requires approval

Path for permissions:
`/admin/people/permissions`

If stakeholders push for “full automation”:
> Explain the risk. Drupal gives safety rails for a reason.

---

## Part D — Proven workflow

1) Generate with AI  
2) Review with human judgement  
3) Validate accessibility  
4) Approve and publish

Always keep this order.

---

## Part E — Real-world guidance for site builders

When leaving the demo environment:

- Add **review fields** for AI output
- Enforce **workflow states** requiring approval
- Keep model settings and tone definitions **centralised**
- Document which content types allow AI assistance
- Track usage in editorial guidelines

Responsible controls:
- [ ] Editorial power stays with humans
- [ ] Automation saves time but never owns truth

---

## Troubleshooting

AI content looks wrong?
- Reject. Fix manually.  
- Review Tone taxonomy guidance.

Readability warnings appear?
- Prefer plain language.  
- Rephrase with CKEditor AI or edit manually.

Editor feels uneasy publishing AI text?
- Keep as draft
- Use workflow to escalate for second review

---

## What’s next (Session 6 preview)

- Summary of what you learned
- Resources to continue building your own AI workflows
- Where Automators and Recipes unlock real production efficiency

---

## Attribution and licence

Copyright © 2025 James Matthew Saunders and Rod Martin.  
Created with support from amazee.io and Promet Source.  
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).
