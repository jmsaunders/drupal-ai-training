# Modules and Providers

This document summarises where AI functionality comes from in Drupal.

## Core Modules Used in Training

**AI Core**  
The foundation for AI in Drupal. Shared UX, services, and plugin architecture.

**CKEditor AI Integration**  
Provides AI actions such as Summarise, Tone, and Rephrase directly in the editor.

**AI Automators (if enabled in demo)**  
Allows structured tasks to run on save. Demo availability varies.

**AI Agents (optional)**  
Guided workflows to help editors accomplish multi-step tasks.

---

## Providers

Capabilities depend on the AI provider selected.  
In this workshop we used **Drupal.org AI Demo** defaults.

Provider capabilities commonly include:
- **Chat** (text generation)
- **Vision** (image captions or recognition)
- **Embeddings** (semantic search)
- **Structured output** (JSON mode)

Note: Availability may vary in demo environments.  
Always **Test connection** in  
`/admin/config/ai/providers`

---

## Recommended Documentation

- Drupal AI documentation:  
  https://www.drupal.org/project/ai
- AI Provider overview:  
  https://www.drupal.org/project/ai_provider
- CKEditor AI tools (Drupal):  
  https://www.drupal.org/project/ckeditor_ai

