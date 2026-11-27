# Group Activity Outcomes – FocusMate

**Module:** PUSL3205 – Large Language Models and Generative AI  
**Laboratory:** Lab 02 – LLMs in Everyday Life  
**Group:** Group 02 – The Distracted Student  
**Proposed Product:** FocusMate – AI-Powered Student Focus Management System

This file records **what the group produced**. The full design is in the [main README](../README.md), and the reasoning behind the decisions is in the [discussion summary](discussion-summary.md).

## 1. Final Outcome

The group's outcome was a design proposal for **FocusMate**, an integrated AI-powered focus management system for students. It combines a mobile application, a smart headset and an eye-tracking camera to address digital, environmental and attention-related distractions in one product.

## 2. Deliverables Produced

| Deliverable | Description | Where documented |
|---|---|---|
| Problem definition | Distractions affecting student concentration | README, Section 3 |
| Product concept | Three-component FocusMate system | README, Section 5 |
| Feature set | Eleven proposed features, from noise management to analytics | README, Section 6 |
| AI mapping | Computer Vision, NLP, Machine Learning, recommendations and LLMs, each tied to a function | README, Section 7 |
| Responsible-design measures | Privacy, consent, safety and accessibility | README, Section 9 |
| Phased development plan | Three phases to reduce hardware cost | README, Section 10.1 |
| Evaluation plan | Metrics and user-trial process | README, Section 11 |
| Visual design deliverables | Overview infographic and architecture diagram | README, Section 13 |

## 3. Key Decisions

- Build an **integrated** system rather than an app-only solution.
- **Prioritise** notifications by importance instead of blocking all of them.
- Make application blocking **context-aware**, not all-or-nothing.
- Use **adaptive transparency** so noise cancellation does not hide safety sounds.
- **Personalise** session length and recovery suggestions instead of using one fixed timer.
- Describe camera output as **estimates** of attention, not measures of concentration.
- Process camera and notification data **on-device**, with no raw video storage.
- Keep the **AI Study Assistant optional** so it does not become a distraction.
- Release the product in **three phases** to keep cost manageable.

## 4. Status and Limitations

- FocusMate is a **concept design**. It has not been implemented or experimentally tested.
- No performance improvements have been demonstrated because the system has not yet been implemented or evaluated.
- Camera accuracy, operating-system restrictions and hardware cost remain open practical challenges.

## 5. Next Steps

1. Prototype Phase 1 (the mobile application) first.
2. Test notification classification with real examples.
3. Run a small user trial and compare results against baseline study sessions.