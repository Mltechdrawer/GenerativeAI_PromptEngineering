## Delimiters in prompts

### What are delimiters?

**Delimiters** are **symbols or special markers** used in a prompt to **clearly separate and indicate different parts of the text**, such as instructions, context or input data.

Their purpose is to help the model **understand what role each piece of information plays** within the prompt.

In simple terms:

> **A delimiter indicates where a specific part of the prompt starts and ends.**

---

### Why are they important?

Without delimiters, a language model may: 

- Confuse instructions with data.  
- Mix the text to be processed with the main instruction.  
- Misinterpret which information is relevant.  

Using delimiters allows: 

- Improving prompt understanding.  
- Increasing the accuracy of responses.  
- Reducing ambiguity.  
- Making prompts clearer and reusable.  

---

### Common types of delimiters

There is no single mandatory delimiter. Some of the most common ones are:

#### Triple quotes

"""
Delimited text
"""

#### Code blocks

#### Bloques de código
```
Delimited text
```

#### Explicit tags
```
<text>
Delimited content
</text>
```

#### Dashes
```
--- Delimited content ---
```

#### Tags
```
<Delimited content> 
```

#### Equals
```
=== Delimited content === 
```

#### Custom markers
```
### INSTRUCTION ###
### CONTEXT ###
### TEXT ###
```

---

### Practical example

#### Without delimiters

```
Summarize the following text Machine learning is a branch of artificial intelligence that...
```

The model may not clearly identify where the text to summarize begins.

#### With delimiters

```
Summarize the following text:

""" Machine learning is a branch of artificial intelligence that... """
```

Ahora el modelo entiende con claridad **qué contenido debe procesar**.

---

### Delimiters and security

Delimiters also help to:

- Isolate external data from the main instructions.
- Reduce prompt injection risks.
- Prevent hidden instructions within a text from influencing the model.

This is especially important when the text comes from users or external sources.

---

### Best practices

- Use delimiters consistently.
- Do not mix too many different types unnecessarily.
- Choose visually clear delimiters.
- Explicitly indicate what each block contains when relevant.

---

<details>
<summary> Examples</summary> Triple double quotes <pre><code> Summarize the following text: """ Software engineering is a discipline of computer science that deals with the design, development and maintenance of high-quality software systems. """ </code></pre> Triple single quotes --- Code blocks <pre><code> Explain what the following code does: ``` for i in range(5): print(i). ``` </code></pre> Explicit tags <pre><code> &lt;instruction&gt; Explain what the following code does. &lt;/instruction&gt; &lt;code&gt; for i in range(3): print(i) &lt;/code&gt; &lt;audience&gt; First-year university student &lt;/audience&gt; </code></pre> Dashes <pre><code> Summarize the following text: --- Software engineering is a discipline of computer science that deals with the design, development and maintenance of high-quality software systems. --- </code></pre> Tags <pre><code> Summarize the following text: &lt;Software engineering is a discipline of computer science that deals with the design, development and maintenance of high-quality software systems.&gt; </code></pre> Equals <pre><code> Summarize the following text: === Software engineering is a discipline of computer science that deals with the design, development and maintenance of high-quality software systems. === </code></pre> Custom markers <pre><code> Summarize the following text: ### Software engineering is a discipline of computer science that deals with the design, development and maintenance of high-quality software systems. ### </code></pre>
</details>

---

### Summary

- Delimiters organize and structure prompts.
- They help differentiate instructions from data.
- They improve accuracy and security.
- They are a key tool in prompt and context engineering.

---

