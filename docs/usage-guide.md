# Practical Guide to Using the CORE Framework

The CORE Framework improves design quality through four simple and practical perspectives. This guide offers question patterns and concrete examples for each perspective.

---

## 🌟 Examples of Questions and Answers by Perspective

### C: Context – Purpose and Environment 🎯

| Question                                 | Poor Answer         | Good Answer |
|------------------------------------------|----------------------|-------------|
| Who will use this system?                | "Internal users"     | "20 sales reps (using it on the go) and 5 accounting staff (mostly at the end of each month)" |
| What do they want to achieve?            | "Improve efficiency" | "Sales needs to quickly check stock and reply on delivery dates during client visits. Accounting wants to reduce invoice generation time from 2 days to 0.5 days." |
| What is the most important goal?         | "Usability"          | "To ensure mobile response time under 2 seconds to boost sales productivity on-site." |

**Tips for Context:**
- Clearly identify roles, numbers, and usage scenarios.
- Express goals in concrete terms (quantifiable change).
- Prioritize needs to support trade-off decisions.

---

### O: Object – Responsibilities and Structure 🧩

| Question                                       | Poor Answer               | Good Answer |
|-----------------------------------------------|---------------------------|-------------|
| What are the main components?                 | "Frontend and backend"    | "1) UI, 2) Sales Logic, 3) Inventory Logic, 4) Customer DB, 5) External APIs" |
| What are the responsibilities of each part?   | "Processes data"          | "Inventory handles: 1) checking stock, 2) allocation, 3) reorder point logic. It interacts with Sales via stock API." |
| What gets impacted if one part is changed?    | "Minimal impact"          | "Changing customer schema affects the UI search screen and sales logic for credit checks." |

**Tips for Object:**
- Use functional decomposition with meaningful labels.
- Clarify what each part does and doesn’t do.
- Predict ripple effects from changes.

---

### R: Reaction – Behavior and Changes 🔁

| Question                                         | Poor Answer         | Good Answer |
|--------------------------------------------------|----------------------|-------------|
| What states does the system have?               | "Normal or abnormal" | "'Pending', 'Ready to Ship', 'Shipped', 'Cancelled' with different editable fields per state" |
| What changes happen when key operations occur?  | "Updates data"       | "Order confirmation changes status, allocates inventory, updates history, and may trigger shipment integration." |
| How do you verify correctness?                  | "Do tests"           | "1) Unit tests for state transitions 2) Integration tests for stock impact 3) E2E tests for UI flow 4) Log tracing with TX IDs" |

**Tips for Reaction:**
- List all system states and transitions.
- Track change propagation across operations.
- Clarify multi-level testing strategy.

---

### E: Evolution – Growth and Understanding 🔄

| Question                                          | Poor Answer             | Good Answer |
|--------------------------------------------------|--------------------------|-------------|
| What future features are anticipated?           | "We’ll see when needed"  | "Planned in 6 months: 1) multi-warehouse support, 2) foreign currency, 3) mobile app. Inventory and currency logic are designed accordingly." |
| Can you explain the design in 5 minutes?        | "Read the docs"          | "1-page diagram with system map, 5 UI mockups, state chart, and data model supports quick walkthrough." |
| What happens when something breaks?             | "Check the logs"         | "All actions are traceable with IDs. On-call staff have predefined error flows for rapid response." |

**Tips for Evolution:**
- Anticipate future change with design flexibility.
- Use visual aids to support knowledge transfer.
- Embed operability from the start.

---

## 💡 When and How to Use the CORE Checklist

### 1. Use by Phase

| Phase             | Focus Perspectives     |
|------------------|------------------------|
| Planning / Requirements | Mainly C |
| Basic Design      | Emphasis on C and O |
| Detailed Design   | Balance across O, R, E |
| Review Phase      | Cover all four |

---

### 2. Time Allocation for a 60-min Review

- C: 10 mins  
- O: 20 mins  
- R: 20 mins  
- E: 10 mins  

---

### 3. Team Usage Tips

- Write each question on a board or shared doc.
- If the answer lacks clarity, ask “What exactly do you mean?”
- At the end of each section, ask “Anything else?”
- Turn concerns into action items immediately.

---

### 4. Tips for Solo Use

- Actually write down answers (don’t just think them).
- Imagine explaining to a teammate.
- Note what feels vague or risky.
- Focus on identifying the *next step*, not on perfection.

---

## 📊 Case Study: Internal Order Management System

**Project**: Renewal of internal order system

### C: Context
- **Users**: 20 sales (mobile use), 5 accounting (in-office)
- **Goal**: Cut order time by 50%, improve mobile productivity
- **Constraints**: Launch in 6 months, reuse DB schema, 5,000 orders/month

### O: Object
- Key components:
  1. UI (web/mobile)
  2. Order core logic (CRUD, status)
  3. Inventory integration
  4. Customer integration (credit check)
  5. Report output (PDF, email)

### R: Reaction
- **States**: Estimate → Confirmed → Allocated → Shipped → Completed
- **Processes**: Order confirmation triggers allocation, credit check, approval flow
- **Tests**: Unit (transitions), E2E (flows), logging via TX ID

### E: Evolution
- **Future**: Global expansion, mobile apps, AI order prediction
- **Operations**: Full audit logging, error tracing ID
- **Docs**: Overview, UI map, data model

---

© 2025 Masahiro Nakatsugawa – CORE Framework | Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)