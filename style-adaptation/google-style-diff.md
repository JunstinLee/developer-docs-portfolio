# Style Adaptation: Blog Style vs. Google Developer Style Guide

This document showcases my ability to adapt informal, highly-metaphorical technical blog posts into sterile, high-precision developer documentation that strictly adheres to the **Google Developer Documentation Style Guide**.

Below are two real-world refactoring examples based on my article: *Why Does AI Forget Instructions?*

---

## Example 1: Eliminating Metaphors & Conversational Fluff

Technical blogs use metaphors (like "forgetful interns" or "glass boxes") to engage readers. However, official developer documentation must eliminate these to reduce cognitive load and prevent translation (L10n) errors.

### ❌ Blog Register (Before)
> *"Think of the context window as a fixed-capacity glass box. Once the box is full, putting a new block of information in pushes the oldest block out. This is why your AI starts behaving like a brilliant but forgetful intern—it literally cannot remember what you said ten minutes ago."*

###  Google Style Register (After)
> When the input payload size exceeds the model's context window limit, the system truncates the earliest tokens in the context state. The model cannot reference instructions or data stored in the truncated index.

### 📝 Style Guide Analysis
- **Rule Applied (Avoid Metaphors)**: Removed "glass box" and "forgetful intern." Google style requires literal, denotative terms (e.g., `input payload`, `truncated tokens`) to ensure clarity and support machine translation.
- **Rule Applied (Sentence Structure)**: Converted a descriptive analogy into a cause-and-effect logical statement (*When X happens, the system does Y*).
- **Rule Applied (Voice)**: Maintained active voice ("the system truncates", "the model cannot reference") instead of passive assumptions.

---

## Example 2: Restructuring Narrative into Imperative Lists

Blog posts often present recommendations in a conversational paragraph format. Enterprise documentation requires structured, scannable lists starting with strong, imperative verbs to help developers take immediate action.

### ❌ Blog Register (Before)
> *"If you want to prevent your AI from getting confused, there are several things you should definitely do. First of all, make sure to always monitor your token usage using the counter API before sending. Secondly, you shouldn't put too many system prompt instructions unless they are absolutely necessary."*

###  Google Style Register (After)
> To prevent instruction loss and optimize context window efficiency, apply the following practices:
> 
> 1. Query the token counter API to monitor token consumption before initiating a request.
> 2. Limit the size of the system prompt to preserve context space for dynamic user inputs.

### 📝 Style Guide Analysis
- **Rule Applied (Imperative Mood)**: Transformed conversational advice ("*make sure to always...*", "*you shouldn't...*") into direct commands starting with strong imperative verbs (*Query*, *Limit*).
- **Rule Applied (List Formatting)**: Converted a narrative block into a numbered list. According to Google guidelines, numbered lists are used for sequential steps or prioritized instructions, which improves skimmability.
- **Rule Applied (Eliminate Fillers)**: Removed filler qualifiers like "*definitely*" and "*first of all*" to adhere to the principle of "writing for a global audience."

---

## Summary of Style Guide Rules Demonstrated

By implementing the refactoring above, this repository demonstrates competency in:
1. **L10n & Global Readability Optimization**: Ensuring text translates accurately across languages by avoiding idioms.
2. **Action-Oriented Language**: Using the second person ("you") and imperative verbs to guide developer behavior.
3. **Structured Information Architecture**: Using bold lead-ins, ordered lists, and logical headings to make documents skimmable.
