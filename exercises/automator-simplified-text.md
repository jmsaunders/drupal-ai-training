# Exercise — AI Automators (Hands On): Simplify Text to 6th Grade Level

> Audience: **Beginning Drupal users**  
> Admin theme: **Gin**  
> Environment: Local or any site with required modules available

AI Automators are tools or workflows in Drupal that automatically apply AI-generated actions to content or fields without manual intervention each time.

We’ll create a workflow that rewrites content to a 6th grade reading level.

---

## The Simplify Text Demo

### Required Modules
Ensure Drupal has the following modules available/enabled:

- amazee.ai AI Provider  
- AI Search  
- AI Core  
- Key  
- Search API  
- LiteLLM AI Provider  
- OpenAI Provider  
- Postgres VDB Provider  

---

## Enable AI Automators
1) Go to **Extend**  
2) Filter for **AI Automators** and enable the module

---

## Create a Content Type
1) Go to **Structure → Content types**  
2) Click **Add content type**  
3) Name it **Article** → Save and **Manage fields**

### Add Field: Body
1) Add field **Body** → **Text (formatted, long)**  
2) Allowed text formats: **Content**

### Add Field: Simplified Title
1) Add field **Simplified Title** → **Text (formatted)**  
2) Allowed text formats: **Content**  
3) **Enable AI Automator** for this field  
4) Choose **LLM: Text**  
5) Set **Automator Input Mode** to **Base Mode**  
6) **Automator Base Field**: **Title**  
7) Enter the following Automator Prompt:

**Source link:**  
https://gist.github.com/jmsaunders/bb6e8669f98bec46415748a5385151c1

**Title Prompt**
Rewrite the following title to a clear, concise version appropriate for a 6th-grade reading level.

Requirements:
Wrap the output in an <h2> HTML tag.
- Do NOT use a <p> tag under any circumstances.
- Return only the tag and text — no explanation, no line breaks, no commentary.

Example of correct output:
<h2>Why Volcanoes Erupt</h2>

Context:
_______________________________________
{{ context }}
_______________________________________

**Advanced settings:**
- Status bar: **Batch** or **Direct**
- AI Provider: **amazee.ai AI**
- Provider Configuration: **claude-3-5-sonnet**
- Temperature: **0** or **0.1**
- Text format: **Content**
- Save settings

---

### Add Field: Simplified Body
1) Add field **Simplified Body** → **Text (formatted, long)**  
2) Allowed text formats: **Content**
3) **Enable AI Automator** for this field  
4) Choose **LLM: Text**
5) Set **Automator Input Mode** to **Base Mode**
6) **Automator Base Field**: **Body**
7) Enter the following Automator Prompt:

**Source link:**  
https://gist.github.com/jmsaunders/2164f1ab74ddcbd4e001e1e16201c7cf

**Body Prompt**
Rewrite the main body content (between the “Context:” delimiters) for a general audience at a 6th-grade reading level. Preserve all key ideas and logical flow, but simplify vocabulary and sentence structure. Ignore the field called title.

1. Rewrite the body into 8–10 paragraphs using simple language. Save this to field_simplified_text body.
2. Rewrite the summary into a short, friendly overview (maximum 2 short paragraphs) appropriate for a general audience. Save this to field_simplified_text summary.

Requirements:
For the body, use only these HTML tags: <h3>, <em>, <strong>.
For the summary, do not use any HTML.
Output only a valid JSON array structured like this:

[
  { "field": "body", "value": "<h2>Rewritten body content...</h2><p>More text...</p>" },
  { "field": "summary", "value": "Short rewritten summary text here." }
]

Do not include any explanations, markdown, or extra commentary.

_______________________________________
{{ context }}
_______________________________________

**Advanced settings:**
- Status bar: **Batch** or **Direct**
- AI Provider: **amazee.ai AI**
- Provider Configuration: **claude-3-5-sonnet**
- Temperature: **0** or **0.1**
- Text format: **Content**
- Save settings

---

## Manage Display
Set field display order to:

1) **Links**
2) **Body**
3) **Simplified Title**
4) **Simplified Body**

---

## Test It
Create a test Article using this sample text:

Graduate-level article on Tariffs (1263 words)  
https://docs.google.com/document/d/1V_K7_Nqw_eh2M14cduWsZzPJ1owkQtqzHT2SOk4QOLc/edit?usp=sharing

Steps:
1) **Content → Add content → Article**
2) Fill in **Title** and **Body**
3) Click **Save**
4) Observe **Simplified Title** and **Simplified Body**

---

## Tips and Thoughts

1) Test prompts manually first  
2) Avoid overwriting human-written content  
3) Use read-only AI fields for review  
4) Organise recipes and automators clearly  
5) Limit automators to relevant content types  
6) Restrict permissions for bulk operations  
7) Test bulk actions on a few nodes first  

