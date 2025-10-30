# Session 2 — Installing and Configuring DrupalAI

Copyright © 2025 James Matthew Saunders and Rod Martin.
Created with support from amazee.io and Promet Source.
Licensed under Creative Commons Attribution–ShareAlike 4.0 International (CC BY-SA 4.0).

## Modules to know
- AI Core (ai) — framework and UI surfaces
- AI Agents (ai_agents) — natural-language actions and assistants
- Provider bridges — OpenAI, LiteLLM proxy, amazee.io
- Optional: Auto Translation, AI SEO, AI Image/Alt Text, AI Media Image

## Setup checklist
1. Enable AI Core and at least one provider.
2. Add keys at Configuration → System → Keys (provider-specific).
3. Visit Configuration → AI → Default Settings to confirm capabilities (chat, vision, embeddings, JSON).
4. Enable editor integrations (CKEditor tools, Content Suggestions).
5. Enable AI Automators, AI Agents, and AI Chatbot as needed.

## Permissions
Only grant AI capabilities to the roles that need them. Keep bulk operations restricted.

## Notes
- Provider choice affects features and costs.
- Keep a non-prod site for testing prompts and automators before rollout.
