# B III — Context Engineering
 
## What is context engineering?

**Context engineering** is the discipline responsible for **designing and managing the information that surrounds a request to a language model** so that it can generate more accurate, coherent and useful responses.

It is not only about writing a good prompt, but about **preparing the appropriate information environment** so that the model correctly understands the task it must perform.

In simple terms:

> **The prompt is the question.  
> The context is everything the model needs to know to respond well.**  

---

## Why is it important?

Language models do not have direct access to reality or external databases unless they are provided as context.

Good context engineering allows:

- Reducing incorrect or irrelevant responses.
- Maintaining coherence in long conversations.
- Adapting responses to a specific domain.
- Building more reliable and scalable AI applications.

Without good context, even a well-written prompt can produce poor results.

---

## Prompt engineering vs Context engineering

| Prompt engineering | Context engineering |
|-------------------|--------------------|
| Focuses on the instruction | Focuses on the complete environment |
| Short-term action | Continuous action |
| Isolated text | Data, memory, rules, tools |
| Ideal for simple tasks | Key for complex systems |

Both complement each other: **a good prompt needs a good context**.

---

## What can be part of the context?

The context may include:

- Previous conversation information.  
- Relevant documents.  
- Domain data (rules, definitions, examples).  
- User or task profile.  
- Results from external tools (search, databases).  

Not everything should always be included: **more context does not always mean better context**.

---

## Basic principles of context engineering

1. **Relevance**  
   Only information useful for the current task should be included.

2. **Clarity**  
   The context must be organized and easy to interpret.

3. **Updating**  
   The context may change over time or with each interaction.

4. **Efficiency**  
   Models have context limits; it must be used carefully.

---

## Simple example

### Without context engineering

**Prompt:**

> Summarize this text.

The model does not know:  
- Who the summary is for.  
- The expected level of detail.  
- Which aspects are most important.  

### With context engineering

Additional information is provided such as:  
- Target audience.  
- Purpose of the summary.  
- Desired style.  

Result: a more precise response aligned with the real need.

---

## Where is context engineering used?

Context engineering is essential in: 

- Advanced chatbots.  
- Intelligent assistants.  
- Retrieval-Augmented Generation (RAG) systems.  
- Autonomous agents based on LLMs.  
- AI-based enterprise applications.  

In these cases, the model needs **much more than an isolated question**.

---

## Summary

- Context engineering prepares the model’s information environment.
- It goes beyond writing prompts.
- It enables more coherent, accurate and useful responses.
- It is key to building real applications with generative AI.