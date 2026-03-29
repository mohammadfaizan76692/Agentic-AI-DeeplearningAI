# Agentic-AI-DeeplearningAI
This is course is teach by andrew NG
# 🚀 Agentic AI Notes (Andrew Ng Course)

---

## 📌 Module 1: Introduction to Agentic AI

### 🔹 What is Agentic AI?

An **Agentic AI workflow** is a process where LLM-based applications execute multiple steps to complete a task.

**Example:**

* **Direct Flow:** LLM → Response
* **Agentic Flow:**

  * LLM researches
  * Drafts initial essay
  * Reflects & improves
  * Sends for human review

---

### 🔹 Degree of Autonomy

| Type              | Description                               |
| ----------------- | ----------------------------------------- |
| Less Autonomous   | Predefined steps and tools                |
| Semi Autonomous   | Can choose tools, limited decision-making |
| Highly Autonomous | Decides steps, creates tools dynamically  |

---

### 🔹 Benefits of Agents

* ✅ Better performance (even older models improve)
* ⚡ Parallel execution → faster
* 🔧 Modular & flexible

---

### 🔹 Applications

* Document processing (e.g., invoices)
* Customer support automation
* Browser-based task execution

---

### 🔹 Task Decomposition

Break tasks into smaller steps:

* LLM-based steps
* Tool/API-based steps

**Building Blocks:**

* Models → LLMs, TTS, Image models
* Tools → APIs, Retrieval, Code execution

---

### 🔹 Evaluation (Evals)

* **Objective:** measurable (e.g., token count, banned words)
* **Subjective:** LLM as judge
* **End-to-End vs Component-level**
* **Trace analysis** (like RAG debugging)

---

### 🔹 Design Patterns

1. **Reflection**
2. **Tool Use**
3. **Planning**
4. **Multi-Agent Collaboration**

---

## 📌 Module 2: Reflection Pattern

### 🔹 Types of Reflection

* Self-reflection (same/different LLM)
* External feedback (errors, outputs)

---

### 🔹 Reflection Prompting

* Clearly define reflection task
* Specify evaluation criteria

---

### 🔹 Evaluation of Reflection

* Dataset comparison:

  ```
  Prompt | Without Reflection | With Reflection
  ```
* LLM-as-judge (biased sometimes)
* Rubric scoring (better)

---

### 🔹 External Feedback Examples

* Code errors
* Web fact-checking
* Word count tools

---

## 📌 Module 3: Tool Use

### 🔹 What are Tools?

Functions provided to LLMs for external actions.

---

### 🔹 Tool Calling Approaches

#### 🧠 Old Method

LLM outputs:

```
Function: function_name
```

#### ⚡ Modern Method

```
User → LLM → Tool → LLM → Final Output
```

---

### 🔹 Code Execution Approaches

1. Many predefined tools
2. Generate & execute code dynamically

⚠️ Use sandbox/Docker for safety

---

### 🔹 MCP (Model Context Protocol)

* Standard by Anthropic
* Provides access to tools & data
* Used by tools like Cursor, Claude

---

## 📌 Module 4: Practical Tips

### 🔹 Development Workflow

1. Build system quickly
2. Create evals
3. Improve using evals

---

### 🔹 Error Analysis

* Analyze traces (step-by-step outputs)
* Identify weakest component

---

### 🔹 Example: Invoice Processing

```
PDF → Text → LLM → Database
```

Track errors in spreadsheet:

| Input | PDF Issue | LLM Issue |
| ----- | --------- | --------- |

---

### 🔹 Improving Systems

#### Non-LLM Components

* Tune parameters
* Replace models/tools

#### LLM Components

* Better prompts (few-shot)
* Try different models
* Break tasks
* Fine-tune

---

### 🔹 Model Selection

* Small → factual tasks
* Large → instruction-following

---

### 🔹 Cost & Latency Optimization

* Optimize after quality
* Use parallelism
* Track cost per component

---

### 🔹 Development Summary

* Build → Evaluate → Analyze → Improve

---

## 📌 Module 5: Highly Autonomous Agents

### 🔹 Planning Workflow

LLM creates step-by-step plan:

**Example:**

1. Find items
2. Check inventory
3. Check price

---

### 🔹 JSON Planning Format

```json
{
  "step": 1,
  "tool": "get_item_descriptions",
  "args": {}
}
```

---

### 🔹 Planning with Code

* LLM writes executable code
* More flexible than JSON
* Harder to control

---

### 🔹 Multi-Agent Systems

#### Example Team:

* Researcher (web search)
* Designer (visuals)
* Writer (content)

---

### 🔹 Communication Patterns

* Linear
* Hierarchical
* Deep hierarchy
* All-to-all

---

### 🔹 Example Architecture

* Planner Agent
* Worker Agents (Researcher, Writer, Editor)
* Task Distributor Agent

---

## 🎯 Key Takeaways

* Agentic AI = multi-step intelligent workflows
* Reflection + tools = major performance boost
* Evaluation is **critical**
* Error analysis drives improvement
* Multi-agent systems scale complexity

---

## 📚 Source

Based on notes from: **Agentic AI Course by Andrew Ng** 

---
