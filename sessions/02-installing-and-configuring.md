# Session 2 — Installing and Configuring DrupalAI

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

Audience: Beginning Drupal users
Admin theme: Gin
Environment: Drupal.org AI Demo environment (Drupal AI Demo)

Session goals
By the end of this session you will:
- Identify the Drupal AI modules that power what you used in Session 1
- Confirm provider capabilities and defaults
- Ensure CKEditor AI tools are correctly enabled for your editors
- Lock down permissions so only the right roles can use AI actions
- Understand where Recipes and Automators will plug in for Session 3 and 4

Part A — Confirm the modules behind the features
Step 1. Verify modules are present
1) Go to Extend (admin/modules).
2) Confirm that AI Core is enabled.
3) Confirm that AI provider bridge modules are present. In the demo these are prewired.
4) If you see AI Agents and AI Automators, leave them enabled for now.
TODO: screenshot — Extend page highlighting AI Core and related modules

Expected result: Core AI features are available. Providers and optional tools are visible.

Part B — Provider capabilities and defaults
Step 2. Check provider(s)
1) Go to Configuration → AI → Providers (admin/config/ai/providers).
2) You should see at least one active provider. Click Test connection.
3) Click View capabilities or an equivalent control on the active provider.
   Look for: chat, vision (image), embeddings, and JSON mode availability.
TODO: screenshot — Providers list with “Test” and “Capabilities”

Expected result: The active provider returns a success test and shows supported capabilities.

Step 3. Set default provider and model
1) Go to Configuration → AI → Settings (admin/config/ai/settings).
2) Choose the default provider.
3) Choose a default model suitable for editorial tasks. Prefer predictable output.
4) Temperature: set to 0.0–0.2 for deterministic results in training.
5) Save configuration.
TODO: screenshot — AI settings with default model and temperature

Expected result: A low-variance default is set so exercises behave consistently.

Part C — CKEditor AI tools configuration
Step 4. Enable the AI toolbar buttons in your text format
1) Go to Configuration → Content authoring → Text formats and editors (admin/config/content/formats).
2) Edit the format used by Basic page (often Basic HTML or a custom format).
3) In the toolbar builder, drag the AI button group into the active toolbar if not present.
   Include: Reformat HTML, Fix Spelling, Summarise, Tone, and other tools you plan to demonstrate.
4) Save the text format.
TODO: screenshot — Text format edit screen with AI buttons added

Expected result: CKEditor now shows the AI tools in the editor toolbar.

Step 5. Turn on AI Content Suggestions (optional but recommended)
1) In the same text format, enable Content Suggestions if available.
2) Enable Readability, Summarise Text, Suggest Title.
3) Save.
TODO: screenshot — Content Suggestions checkboxes enabled

Expected result: Editors can invoke sidebar suggestions for clarity and titles.

Part D — Role permissions and governance
Step 6. Restrict who can use AI tools
1) Go to People → Permissions (admin/people/permissions).
2) Search for AI. Review all AI-related permissions.
3) Grant toolbar and content-suggestion actions to Editor and higher only.
4) Do not enable bulk operations or destructive actions for unauthorised roles.
5) Save permissions.
TODO: screenshot — Permissions page filtered to AI

Expected result: Only trained staff can access AI authoring features.

Governance note
Keep high-impact actions behind roles that receive training. Prefer drafts or review fields to keep humans in the loop before publishing.

Part E — Quick validation pass
Step 7. Validate editor experience
1) Create or edit a Basic page.
2) Confirm the AI toolbar group is visible in CKEditor.
3) Select a paragraph and run Summarise.
4) Run Tone on the result and review.
5) Save as draft.
Expected result: Same successful outcomes as Session 1, now guaranteed by configuration.

Part F — Where Recipes and Automators will fit (preview)
Step 8. Recipes in practice
1) Recipes are named prompts plus model settings that drive repeatable tasks.
2) We will store them where your team can reuse them consistently.
3) For now, note the Settings area as the global home for defaults you will reference later.

Step 9. Automators in practice
1) Automators run specific transformations on save or via bulk operations.
2) In Session 4 we will attach automators that write to separate fields such as Simplified Title and Simplified Body.
3) Low temperature and strict output formats will give training-friendly, repeatable results.

Troubleshooting
- Cannot see AI buttons: verify the correct text format is assigned to the content type and that the AI group is in the toolbar.
- Provider tests fail: wait 10–15 seconds then test again. Switch provider if the demo lists another option.
- Editors cannot see features: recheck role permissions and that they can use the specific text format.

What’s next (Session 3 preview)
We will apply AI to real editorial workflows:
- CKEditor AI for structured content
- Tone vocabulary configuration
- Content Suggestions for titles and readability
- Guardrails for publishing and review

Attribution and licence
Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).
