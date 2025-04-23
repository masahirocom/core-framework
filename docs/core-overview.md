# CORE Design Framework – A Compass for Design Thinking Through Questions

## 🎯 Concept

When you’re unsure about a design, uncertain about decisions, or worried about blind spots—  
what brings clarity is not an answer, but a question.

The **CORE Design Framework** is a compass for system designers.  
With just four simple, powerful questions, it helps uncover assumptions, clarify intentions, and guide better architectural decisions.

---

## 🔷 The Four CORE Questions

| Viewpoint              | Essential Question                            |
|------------------------|-----------------------------------------------|
| **C: Context**         | **"Who is it for, and for what purpose?"**    |
| **O: Object**          | **"What is this structure responsible for?"** |
| **R: Reaction**        | **"What changes when this action occurs?"**   |
| **E: Evolution**       | **"Can it withstand future change?"**         |

These four questions alone can drive effective design reviews.  
The question you struggle to answer is often where your design is weakest.

---

## 🧭 Supplemental Questions (Use if needed)

| Context (C)                  | Object (O)                    | Reaction (R)                 | Evolution (E)                   |
|-----------------------------|-------------------------------|------------------------------|---------------------------------|
| - Why now? Any constraints? | - Responsibility overlaps?    | - Are states and effects clear? | - Understandable by others? Localized changes? |

These are optional prompts to help you dig deeper when the main question isn't enough.

---

## 🎭 Metaphor: Theater and Design

| CORE Viewpoint | In Theater Terms                                     |
|----------------|------------------------------------------------------|
| Context        | Why say that line? What does it convey to the audience? |
| Object         | What role do props or movements play?                |
| Reaction       | How does this change the mood or scene?              |
| Evolution      | Can this script or role withstand cast or script changes? |

---

## 📘 How to Use CORE in Practice

1. **At the start of design reviews or planning, share these 4 questions with the team.**
2. **Try to answer each one. Aim for a one-sentence answer.**
3. **If a question is hard to answer, that’s the weak spot.**
4. **Use the supplemental prompts to deepen the discussion.**

---

## 🧪 Case Example: Internal Order Management System

**Project**: Redesigning the internal order management system used by sales and accounting. Mobile compatibility is required.

| CORE | Answer Example (from review session) |
|------|--------------------------------------|
| **C** | "Sales staff need to check stock and confirm orders while on the go. The old system was desktop-only and slow." → This clarifies the user role and goals. |
| **O** | "Split into UI, order logic, stock sync, and report output. Each has its own responsibility." → Follow-up questions focused on boundaries and data flow. |
| **R** | "Confirming an order decreases inventory and triggers shipping. Errors occur if stock is insufficient." → Led to discussions on side effects and logging. |
| **E** | "The system is structured to support future expansion to overseas offices and mobile apps." → Prompted review of scalability and design intent. |

**Review Summary**:

- **Strength**: Clear in Object and Evolution. No structural issues detected.
- **Concern**: Context was still vague. Business KPIs needed clarification.
- **Next Steps**: Define KPIs and improve stock allocation error logging.

---

> CORE Design Framework  
> Author: Masahiro Nakatsugawa
