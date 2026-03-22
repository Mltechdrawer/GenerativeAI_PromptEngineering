# B II — Prompt Engineering

## Objective
Master techniques to control the **level of detail, format, and quality** of responses.

## 1. Introduction

**Prompt engineering** (*Prompt Engineering*) is the discipline that studies how to **design, formulate and optimize instructions** to effectively interact with Large Language Models (*Large Language Models*, LLMs).

Since LLMs generate their responses based on the input text, the quality of the *prompt* is crucial to obtain responses that are **accurate, coherent, useful and aligned with the user's objectives**.

---

## 2. What is a prompt?

A **prompt** is the input text provided to a language model to guide the generation of a response. It can take multiple forms, from a simple question to a complex instruction including context, examples and constraints.

Prompts allow:  
- Guiding the generation of responses.  
- Optimizing the performance of the model.  
- Adapting the model’s behavior to different contexts.  
- Evaluating the quality and reliability of the obtained responses  

---

## 3. Objectives of prompt engineering

The main objectives of prompt engineering are:

1. **Guide the generation of responses**, reducing ambiguity.
2. **Optimize the performance of the model**, obtaining more relevant responses.
3. **Adapt the prompt to the context**, domain and user level.
4. **Evaluate and improve the quality of prompts**, identifying deficiencies and biases.

---

## 4. Anatomy of a prompt

An effective prompt usually consists of the following elements:

1. **Clarity and specificity**  
2. **Context and background**  
3. **Objective or purpose**  
4. **Keywords and relevant terms**  
5. **Constraints or specific guidelines** 

### Example of efficient structure

- **Introduction:**  
  *I am interested in sustainable practices in modern agriculture.*

- **Specific question:**  
  *Could you explain how precision agriculture techniques and organic farming contribute to environmental sustainability?*

- **Guidelines:**  
  *The response should be technical, detailed and not exceed 500 words.*

---

## 5. Inefficient prompts

A poorly designed prompt can generate vague or irrelevant responses.

**Example of inefficient prompt:**
> *“Tell me things about plants.”*

This prompt lacks:  
- clarity,  
- context,  
- a defined objective,  

It does not specify which aspect of plants is of interest (biology, gardening use, ecological importance, etc.), it does not provide context or background, and it does not establish a clear objective or purpose for the response.  
This lack of structure and detail may result in an AI response that does not meet the user’s expectations or needs.

---

## 6. Types of prompts

Depending on their purpose, prompts can be classified as:

1. **Informational**  
   *Example:* Explain the causes and effects of climate change.

2. **Creative**  
   *Example:* Write a short story about a trip to Mars in the year 2100.

3. **Educational**  
   *Example:* Describe the process of photosynthesis.

4. **Interactive**  
   *Example:* What is your favorite movie and why?

5. **Analytical**  
   *Example:* Analyze the sales trends of the last quarter.

6. **Technical**  
   *Example:* Explain how electric motors work.

---

## 7. Prompt design principles

Good prompt design is based on the following principles:

1. **Clarity and precision**  
2. **Specificity**  
3. **Context and relevance**  
4. **Defined objective**  
5. **Conciseness**  
6. **Adaptability**  

These principles help maximize the usefulness of the model and reduce incorrect or ambiguous responses.

[Delimiters](delimiters.md)

---

## 8. Advanced prompting techniques

### 8.1 Trigger words
*Trigger words* are words that guide the model toward a specific type of reasoning or response, for example: *analyze*, *justify*, *compare*, *summarize*.

[Analytical](examplesprompts.md#1-analytical-prompt)

[Explanatory](examplesprompts.md#2-step-by-step-explanatory-prompt)

[Comparative and critical](examplesprompts.md#3-comparative-and-critical-prompt)

---
### 8.2 Chain of Thought (CoT)

The **Chain of Thought** technique consists of explicitly asking the model to **reason step by step**, which improves performance on complex problems.

**Example:**
> *Solve the problem step by step, explaining the reasoning followed.*

[Quantitative problem](examplesprompts.md#1-quantitative-problem)

[Multicriteria decision](examplesprompts.md#2-multicriteria-decision)

[Route optimization](examplesprompts.md#3-route-optimization)

---

### 8.3 Prompt Priming

**Priming** consists of providing initial instructions that prepare the model before the main task.

**Example:**
> *Start your answer with a brief introduction, continue with a step-by-step example and finish with a practice question.*

[Expert role priming](examplesprompts.md#1-priming-with-expert-role)

[Structure and style priming](examplesprompts.md#2-priming-with-structure-and-style)

[Usage context priming](examplesprompts.md#3-priming-with-usage-context
)

---

### 8.4 One-shot and Few-shot prompting

- **One-shot:** a single example is provided.
- **Few-shot:** several examples are provided to guide the model’s behavior.

These techniques allow **modelling the style, format and level of detail** of the response.

[One shot single example](examplesprompts.md#1-one-shot)

[One shot format and style](examplesprompts.md#2-one-shot)

[Few shot multiple examples](examplesprompts.md#3-few-shot)

[Few shot consistent role and style](examplesprompts.md#4-few-shot)

### 8.5 Tree of Thoughts (ToT)

The **Tree of Thoughts (ToT)** technique is an advanced extension of the *Chain of Thought* approach that allows language models to **explore multiple reasoning paths in parallel**, organized as a tree instead of following a single linear sequence.

#### Main idea

Instead of generating a single reasoning chain, the model:

* Produces **multiple thought alternatives** at each step,
* Evaluates the quality or feasibility of each alternative,
* Discards less promising branches,
* Continues exploring the most relevant branches until reaching a final solution.

This approach is especially effective in **complex problems**, where exploration, planning and intermediate evaluation are essential.

#### Differences with Chain of Thought

| Chain of Thought                    | Tree of Thoughts                  |
| ----------------------------------- | --------------------------------- |
| Linear reasoning                    | Branching reasoning               |
| Single sequence                     | Multiple possible paths           |
| No explicit intermediate evaluation | Evaluation and pruning of branches|
| Suitable for moderate problems      | Suitable for complex problems     |

[Tree of thoughts](examplesprompts.md#1-tree-of-thoughts)

#### Recommended use cases

* Logic and abstract reasoning problems
* Planning and decision-making
* Games, puzzles and strategy search
* Tasks where multiple solutions are possible

#### Advantages

* Encourages more deliberate and deeper reasoning
* Reduces the likelihood of rushed solutions
* Improves quality in tasks requiring exploration

#### Limitations

* Increases computational cost
* Not always necessary for simple tasks

---

### 8.6 Visualization of Thoughts (VoT)

**Visualization of Thoughts (VoT)** is an emerging technique that aims to guide the model to **represent its reasoning in a visual or spatial way**, such as mental diagrams, concept maps or graphical structures, in order to improve reasoning in certain domains.

#### Main idea

The model not only explains its steps, but also:

* Organizes reasoning as a **visual structure**,
* Uses spatial representations (hierarchical lists, graphs, maps),
* Simulates building a “mental map” of the problem.

This technique has shown promising results in **spatial reasoning**, navigation, planning and structural understanding tasks.

[Visualization of thoughts](examplesprompts.md#1-visualization-of-thoughts)

#### Potential use cases

* Spatial or geometric reasoning
* Analysis of complex systems
* Problems that benefit from diagrams or maps
* Support for multimodal reasoning

#### Current state of the technique

**Experimental technique**

* Not yet established as a standard in prompt engineering
* Mainly derived from recent academic research
* Considered an **emerging line**, rather than an established practice

#### Teaching recommendation

This technique is suitable for:

* Introducing current research trends
* Showing the limits and evolution of prompt engineering
* Advanced or exploratory contexts

Not recommended as a basic or general-purpose technique.

---

## 9. Output format specification

Prompts can explicitly specify the **format of the response**, such as:

- Plain text
- Lists and bullet points
- Tables
- Source code
- Summaries
- Translations
- Structured formats (CSV, JSON, etc.)

[Specify output format](examplesprompts.md#1-specify-the-output-format)

---

## 10. Final reflection

Prompt engineering is not only about “asking good questions”, but about **understanding how language models interact with input text**.

Mastering this discipline allows:    
- improving the quality of responses,  
- reducing errors and hallucinations,  
- critically and responsibly leveraging the potential of LLMs.  

This knowledge is essential for the professional and academic use of tools such as ChatGPT.

[Practical examples](examplestotry.md) 

[Activity 1](activity1.md)