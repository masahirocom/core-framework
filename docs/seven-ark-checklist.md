# Seven Ark Checklist – Guided Design Review Sheet

This checklist helps you apply the Seven Ark framework in design reviews and evaluations.  
Answer each question to identify gaps, clarify logic, and improve your architecture.

---

## 🎯 Purpose

| Question                                              | ✅ OK | 🚧 Needs Review | Notes |
|-------------------------------------------------------|--------|------------------|-------|
| Why does this system or feature exist?                |        |                  |       |
| Who are the primary users and what do they need?      |        |                  |       |
| Are the business or operational goals clearly defined?|        |                  |       |

---

## 🧩 Responsibility

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Are component responsibilities clearly divided?        |        |                  |       |
| Is there any overlap or ambiguity in ownership?        |        |                  |       |
| Does each part have a single, clear duty?              |        |                  |       |

---

## 🏗 Structure

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Are modules or layers logically organized?             |        |                  |       |
| Are boundaries and interfaces clearly defined?         |        |                  |       |
| Is the directory/package structure easy to follow?     |        |                  |       |

---

## 🔁 State

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Are the system states clearly defined?                 |        |                  |       |
| Are transitions between states explicitly modeled?     |        |                  |       |
| What triggers state changes, and are side effects clear?|       |                  |       |

---

## 🧪 Verifiability

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Can the behavior of each component be tested easily?   |        |                  |       |
| Are logs or metrics available for tracing problems?    |        |                  |       |
| Is it observable in production (monitoring-ready)?     |        |                  |       |

---

## 🔄 Evolution

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Can this system adapt to foreseeable future changes?   |        |                  |       |
| Are extension points or flexible configurations in place?|      |                  |       |
| Does change affect only local areas (low coupling)?    |        |                  |       |

---

## 🧠 Explainability

| Question                                               | ✅ OK | 🚧 Needs Review | Notes |
|--------------------------------------------------------|--------|------------------|-------|
| Can a new team member understand the structure quickly?|        |                  |       |
| Is the reasoning behind design decisions documented?   |        |                  |       |
| Are names, diagrams, and explanations intuitive?       |        |                  |       |

---

## 🧾 Summary

| Strengths                                    | Areas to Improve                           |
|---------------------------------------------|--------------------------------------------|
| (Write strengths here)                      | (Write weaknesses or unclear areas here)    |

---

© 2025 Masahiro Nakatsugawa – Seven Ark | Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
