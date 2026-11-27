# Group Discussion Summary – FocusMate

**Module:** PUSL3205 – Large Language Models and Generative AI  
**Laboratory:** Lab 02 – LLMs in Everyday Life  
**Group:** Group 02 – The Distracted Student  
**Product:** FocusMate – AI-Powered Student Focus Management System

This file records **how the group discussed the problem and reached its decisions**. The resulting design is in the [main README](../README.md), and the list of outputs is in the [activity outcomes](activity-outcomes.md).

## 1. Starting Point

The group asked how AI could help students who start studying with good intentions but lose focus. We first listed the distractions students face:

- Social media and mobile notifications.
- Frequent switching between applications.
- Environmental noise and interruptions from other people.
- Sleepiness and reduced attention.
- Personal thoughts and unrelated tasks during study.

The group agreed that these cannot all be solved by simply blocking applications.

## 2. Issues Raised, Options Considered and Decisions

| Issue raised | Option considered | Decision and reason |
|---|---|---|
| Is an app enough? | App only, or app plus hardware | Combine an app, headset and camera, because noise and attention are not visible to an app alone |
| Notifications interrupt study, but some are important | Block all notifications, or judge importance | Prioritise by importance, so university and emergency messages still get through |
| Some apps are both useful and distracting | Block whole apps, or consider how they are used | Context-aware blocking, for example educational video allowed and entertainment restricted, where the OS allows it |
| Noise cancellation could hide alarms or someone calling | Full noise cancellation, or let important sounds through | Adaptive transparency for safety sounds |
| Looking away may not mean distraction | Treat every look-away as distraction, or add safeguards | Calibration, several signals and confidence thresholds to reduce false alerts |
| Students study differently | One fixed timer, or learn individual habits | Adaptive, personalised sessions and recommendations |
| Camera and notifications are sensitive | Cloud processing, or local processing | On-device processing, consent, a visible camera indicator and no raw video storage |
| Hardware could be expensive | Sell everything together, or release in stages | Three development phases |
| Where do LLMs fit? | Focus tools only, or also learning support | Optional AI Study Assistant, kept optional to avoid new distractions |

## 3. Main Concerns Discussed

- **Accuracy:** Eye tracking and notification classification can be wrong, and a wrong classification could hide an important message.
- **Privacy:** Camera data and message content are personal, so students must stay in control.
- **Safety:** Isolating students from their surroundings is a risk.
- **Cost and access:** Needing several devices could exclude some students.
- **Platform limits:** Mobile operating systems may restrict what an app can block or read.
- **Student autonomy:** AI should support students with recommendations, not control them or interrupt without need.

## 4. Points of Agreement

- A good solution must deal with digital, environmental and attention-related distractions together.
- The camera can only **estimate** attention, not measure concentration or understanding.
- Students should be able to customise and override the system.
- The product should be evaluated with real students before any benefits are claimed.

## 5. Open Questions

- How accurate can attention and drowsiness estimates be with glasses, poor lighting or different camera positions?
- How much can be done on-device without hurting battery life and response time?
- Which blocking and notification features will mobile operating systems actually allow?
- Will students find the personalised recommendations helpful rather than intrusive?

## 6. Conclusion

The discussion produced FocusMate as a proposed integrated solution. The main conclusion was that an effective focus tool should consider individual study behaviour, privacy, safety, accessibility and affordability, and should use AI to support students rather than control them.