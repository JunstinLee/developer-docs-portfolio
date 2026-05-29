# Style Adjustment: Blog Style vs. Google Developer Style Guide

This document demonstrates my ability to transform informal, metaphor-heavy technical blog posts into rigorous, high-precision developer documentation strictly adhering to the Google Developer Documentation Style Guide.

Below are two practical refactoring examples based on my article *"Why Does AI Forget Instructions?"*.

## Example 1: Removing Metaphors and Conversational Redundancies

Technical blogs use metaphors (such as "sand" and "shovels") to engage readers. However, formal developer documentation must eliminate these metaphors to lower cognitive load and prevent localization errors.

### ❌ Blog Repository (Before Modification)

"The effective output length is like the capacity of the shovel in the AI's hand. Even if there is plenty of sand in the box, it can only scoop out a limited amount of grains at a time. If your task is too massive and you force it to scoop an excessive amount of sand at once, it will begin to 'feel overwhelmed': it will either stop abruptly halfway through (output truncation) or, to make up the numbers, mindlessly grab stale, obsolete scraps from the bottom of the box (historical memory) to hand over to you. As a result, it starts talking nonsense, completely losing track of the original instructions you gave it."

### Google Style Repository (After Modification)

When the currently occupied model context length exceeds the effective output length of the model, the system truncates the earliest tokens in the context state. The model cannot reference instructions or data stored in the truncated indices.

### 📝 Style Guide Analysis

* **Rule Application (Avoid Metaphors):** Removed "sand" and "shovels". The Google Style Guide requires literal, referential terms (e.g., "input payload", "truncated tokens") to ensure clarity and support machine translation.
* **Rule Application (Sentence Structure):** Converted descriptive analogies into causal logic statements (When X occurs, the system executes Y).
* **Rule Application (Voice):** Maintained the active voice ("the system truncates", "the model cannot reference") instead of the passive voice.

---

## Example 2: Refactoring Narrative into Imperative Lists

Blog posts often present recommendations in a conversational, paragraph-based format. Enterprise documentation requires structured, scannable lists starting with strong imperative verbs to help developers take immediate action.

### ❌ Blog Repository (Before Modification)

"If you want to prevent the AI from getting confused, there are a few things you must definitely do. First of all, always make sure to monitor token usage using the counter API before sending a request. Secondly, you shouldn't add too many system prompt instructions unless it is absolutely necessary."

### Google Style Repository (After Modification)

To prevent instruction loss and optimize context window efficiency, apply the following practices:

1. Query the token counter API to monitor token consumption before initiating a request.
2. Limit the size of system prompts to reserve context space for dynamic user inputs.

### 📝 Style Guide Analysis

* **Rule Application (Imperative Mood):** Converted conversational recommendations ("make sure to always...", "you shouldn't...") into direct commands starting with strong imperative verbs (*Query*, *Limit*).
* **Rule Application (List Formatting):** Converted the narrative paragraph into a numbered list. According to the Google Guide, numbered lists are used for sequential steps or prioritized items, enhancing scannability.
* **Rule Application (Eliminate Filler Words):** Removed filler qualifiers like "definitely" and "first of all" to adhere to the principle of "writing for a global audience."

---

## Summary of Style Guide Rule Demonstration

By implementing the refactoring detailed above, this repository demonstrates proficiency in the following areas:

* **Localization and Global Readability Optimization:** Ensuring text translates accurately across languages by avoiding idioms and colloquialisms.
* **Action-Oriented Language:** Directing developer behavior using the second person ("you") and imperative verbs.
* **Structured Information Architecture:** Utilizing bold lead-ins, ordered lists, and logical headings to create highly scannable documentation.
