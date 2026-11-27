# Lab 02 – LLMs in Everyday Life: FocusMate

**Module:** PUSL3205 – Large Language Models and Generative AI   
**Laboratory:** 02  
**Group:** Group 02 – The Distracted Student  
**Date:** 3 October 2026

> **Related documents:** This README contains the full FocusMate design. The group-work record is kept separately in [`group-activity/activity-outcomes.md`](group-activity/activity-outcomes.md) (what the group produced) and [`group-activity/discussion-summary.md`](group-activity/discussion-summary.md) (how the group reached its decisions).

---

## 1. Laboratory Session

**Topic:** LLMs in Everyday Life – Designing an AI-Powered Student Focus Management System

**Group Scenario:** Group 02 – The Distracted Student

The group identified a common student problem: difficulty maintaining concentration during study sessions because of digital notifications, social media, environmental noise, interruptions and reduced attention. Our proposed solution is **FocusMate – AI-Powered Student Focus Management System**.

## 2. Objective

The objective was to identify a real-world problem affecting students and design an AI-powered product to address it, applying ideas from Natural Language Processing, Computer Vision, Machine Learning, recommendation systems and Large Language Models to a practical scenario.

## 3. Problem Statement

Students face many distractions during study sessions, including social media notifications, frequently used mobile applications, environmental noise and interruptions from other people. They may also experience sleepiness, eye strain and reduced attention during long sessions without realising that their productivity is falling.

Existing productivity applications mainly focus on time management or blocking applications. They do not address environmental distractions, notification prioritisation and attention monitoring together, and they usually apply the same rules to every student.

## 4. Tasks and Implementation

The group activity involved six design tasks:

1. **Identify the problem:** Analyse why students lose concentration, including internal distractions.
2. **Define the product:** Propose an integrated system of a mobile application, a smart headset and an eye-tracking camera.
3. **Identify AI components:** Map each AI technology to a specific function (see Section 7).
4. **Design the user flow:** Define how a session starts, how distractions are handled and how focus is recovered.
5. **Consider responsible design:** Identify privacy, consent, safety, accessibility and cost issues.
6. **Plan evaluation:** Select measurable indicators for a future user trial.

The system has not been implemented or experimentally validated. The technologies and features described here are proposed design choices.

## 5. Product Concept

**FocusMate** is an AI-powered student focus management system designed to create a personalised, distraction-minimised study environment. It has three components.

| Component | Main functions |
|---|---|
| **Smart Headset** | Active Noise Cancellation (ANC), adaptive transparency, audio notifications, optional music, configurable audio settings |
| **AI-Powered Mobile Application** | Starts and manages study sessions, restricts apps, classifies notifications with NLP, sends alerts to the headset, tracks usage, provides recommendations, analytics and the optional AI Study Assistant |
| **AI Eye-Tracking Camera** | Estimates gaze direction and visual attention, identifies prolonged eye closure and potential drowsiness, and sends estimates to the mobile app |

**Safety consideration:** The headset should not completely isolate students from their surroundings. Adaptive transparency should let safety sounds (fire alarms, doorbells, emergency announcements, the student's name or chosen keywords) through where the headset supports it.

**Accuracy note:** The camera provides estimates, not a definitive measurement of concentration or understanding.

## 6. Key Features

### 6.1 Intelligent Noise Management
ANC reduces background noise, with adaptive transparency, configurable sound preferences and safety-sound passthrough where supported. The aim is a quieter study space without disconnecting students from important sounds.

### 6.2 Smart and Context-Aware Application Blocking
Students select which applications to restrict, set usage limits and temporarily allow apps when needed. Blocking considers how an app is used: YouTube may be allowed for an educational lecture but restricted for entertainment. This depends on the permissions the operating system provides.

### 6.3 AI-Based Notification Prioritisation
NLP classifies notifications by importance and urgency.

| Category | Example | System response |
|---|---|---|
| Critical | Emergency notification | Immediate alert |
| Important | University announcement or lecturer communication | Headset notification |
| Normal | General personal messages | Save for later |
| Distracting | Social media notifications | Suppress during study |

Students can customise categories, priority contacts and emergency overrides, so the AI does not independently decide which personal messages matter. Held notifications are shown as a **digest** during scheduled breaks.

### 6.4 Eye-Tracking and Drowsiness Detection
Proposed techniques are Eye Aspect Ratio (EAR) for eye closure, PERCLOS (percentage of eye closure over a period), gaze estimation and head-position analysis.

Students may look down to write notes or close their eyes while thinking, so looking away is not treated as distraction on its own. The proposed approach is:

1. An initial camera calibration.
2. An individual baseline for each student.
3. Monitoring of indicators over time.
4. Combining camera estimates with other signals, such as app switching and phone pickup.
5. Confidence thresholds before any recommendation is given.

Accuracy may be affected by glasses, lighting, camera position and individual differences. Students can disable camera monitoring at any time.

### 6.5 Adaptive Focus Engine
Instead of one timer for everyone, the engine gradually learns each student's patterns and personalises study session duration, break intervals, application restrictions, notification filtering and recovery recommendations. For example, Student A may focus for about 25 minutes, Student B may prefer 45-minute sessions, and Student C may frequently switch between study materials and social media.

### 6.6 Intelligent Focus Recovery
When drowsiness, reduced visual attention or repeated distractions are identified, FocusMate can display a gentle reminder, recommend a short break, suggest stretching, water or a short walk, apply the 20-20-20 rule to reduce eye strain, or optionally play the student's preferred music. Music is optional because it can itself be a distraction.

### 6.7 Optional AI Study Assistant
An LLM-powered assistant can summarise lecture notes, generate revision questions, explain difficult concepts, create short quizzes and recommend revision topics. For example, uploaded Machine Learning notes could produce five revision questions. It is optional so that students can keep a distraction-free session.

### 6.8 Study Planning Integration
Integration with calendars and Learning Management Systems such as Moodle can import exam dates and deadlines, create study schedules, link sessions to subjects, prioritise upcoming tasks and send revision reminders.

### 6.9 Internal Distraction Management
A **Distraction Parking Lot** lets students jot down a stray thought or task (for example "reply to a message later") without leaving the session. Items are reviewed during breaks.

### 6.10 Motivation and Accountability
Positive reinforcement through daily and weekly goals, streaks, badges, milestones, optional study groups and optional parent-view features with consent. Feedback should be encouraging rather than shaming.

### 6.11 Distraction Analytics Dashboard

| Metric | Description |
|---|---|
| Total Study Time | Time spent in study sessions |
| Focus Session Completion | Percentage of completed sessions |
| Distraction Frequency | Number of detected interruptions |
| Application Usage | Time spent in selected applications |
| Attention Estimates | Estimated visual attention patterns |
| Average Session Duration | Average length of completed sessions |
| Productivity Trends | Weekly and monthly comparisons |

Example insight (illustrative): "Your average completed study session increased from 25 minutes to 38 minutes this week."

## 7. Where and How We Use AI

| AI area | Use in FocusMate |
|---|---|
| **Computer Vision** | Estimates eye movements, gaze direction, eye-closure patterns and visual attention using techniques such as EAR, PERCLOS and gaze estimation |
| **Natural Language Processing** | Classifies notifications (university announcements, lecturer messages, emergencies, general, social media or promotional) by importance and urgency |
| **Machine Learning** | Learns individual study habits, distraction periods, preferred session lengths and app-usage patterns, and drives the Adaptive Focus Engine (6.5) |
| **Recommendation System** | Combines signals from all components to suggest actions, taking confidence levels, student preferences and manual overrides into account |
| **Large Language Models** | Powers the optional Study Assistant: summaries, explanations, quizzes and questions answered from uploaded learning materials |

**Recommendation example:** If the camera estimates prolonged eye closure and the app detects a long study session, FocusMate may recommend a short break.

## 8. Comparison with Existing Solutions

| Capability | Typical app-blocking and timer apps | FocusMate |
|---|---|---|
| Application blocking | Common | Context-aware restrictions |
| Study timer | Common | Adaptive study sessions |
| Environmental noise reduction | Usually not included | Smart headset integration |
| AI notification prioritisation | Limited or not included | NLP-based prioritisation |
| Attention and drowsiness estimation | Usually not included | Camera-based estimates |
| Personalised focus recommendations | Limited | Adaptive Focus Engine |

This comparison describes the intended product concept. Capabilities of individual existing products may vary.

## 9. Privacy, Security and User Control

FocusMate handles camera data, notification content and personal study behaviour, so it follows privacy-first principles.

**Camera**
- Process locally on the student's device wherever possible.
- Never store or upload raw video.
- Retain only derived information, such as attention estimates and drowsiness indicators.
- Require explicit consent, show a visible camera-on indicator, and allow pausing or disabling at any time.

**Notifications**
- Classify on-device wherever supported.
- Do not upload private notification text to external AI services by default.
- Retain only the minimum classification results.

**User control:** Students control camera permissions, notification access, application restrictions, study schedules, audio settings, data retention and personalised recommendations.

## 10. Practical Considerations and Limitations

| Challenge | Proposed solution |
|---|---|
| Hardware cost | Phased development (below) |
| Eye-tracking errors | Calibration, confidence thresholds and multiple signals |
| Glasses and poor lighting | Camera-quality checks and alternative monitoring options |
| Mobile OS restrictions | Use supported operating-system permissions and APIs |
| Notification privacy | Local classification where possible |
| ANC safety | Adaptive transparency and safety-sound passthrough |
| AI classification errors | Customisation and manual overrides |
| Accessibility | Alternative controls and configurable alerts |

### 10.1 Phased Development

| Phase | Scope |
|---|---|
| **Phase 1 – Application-based focus management** | Mobile app, session management, app restrictions, notification prioritisation, basic analytics, optional phone or laptop camera monitoring |
| **Phase 2 – Smart headset integration** | Compatible noise-cancelling headset, audio notifications, adaptive noise management, safety-sound passthrough |
| **Phase 3 – Dedicated eye-tracking camera** | Dedicated camera, improved gaze estimation, drowsiness analysis, advanced attention analytics |

This lets students use the basic system without buying all the hardware at once.

## 11. Evaluation Plan

A small user trial with students who regularly experience study distractions would test whether FocusMate improves the study experience.

| Metric | Purpose |
|---|---|
| Focus Score | Estimate session consistency from defined behavioural indicators |
| Session Duration Before First Distraction | How long students study before the first recorded interruption |
| Notification Classification Precision | How accurately important notifications are identified |
| Notification Classification Recall | How many genuinely important notifications are caught |
| Drowsiness Detection Accuracy | Reliability of drowsiness estimates against labelled observations |
| Session Completion Rate | Percentage of completed sessions |
| User Satisfaction | Feedback on usefulness, comfort, privacy and usability |

**Proposed process:** collect baseline data without FocusMate, let students use the system in normal sessions, record metrics with consent, compare before and after, gather questionnaire feedback, and identify limitations.

No performance improvements are claimed until an actual evaluation has been conducted.

## 12. Target Users and Expected Outcome

**Target users:** university and college students, school students preparing for examinations, online learners and self-study enthusiasts, students who struggle with digital distractions, and anyone who needs a more structured study environment. The system should support different preferences and accessibility needs, including students with ADHD or sensory sensitivities, with customisable alert sounds, visual notifications, session lengths and monitoring options.

**Expected outcome:** an integrated solution for environmental, digital and attention-related distractions. Rather than only tracking time or blocking apps, FocusMate aims to understand the study environment, identify distractions, learn individual behaviour, estimate attention and drowsiness, prioritise important notifications, recommend personalised actions and help students build healthier study habits.

## 13. Results and Evidence

The group activity produced the FocusMate design proposal. The full list of outputs and decisions is in [`group-activity/activity-outcomes.md`](group-activity/activity-outcomes.md), and the discussion that led to them is in [`group-activity/discussion-summary.md`](group-activity/discussion-summary.md).

### 13.1 System Overview

The infographic shows the main components, key features, AI capabilities and an example use-case flow.

![FocusMate System Overview](screenshots/FocusMate_%20AI%20Student%20Focus%20System.png)

### 13.2 System Architecture

The diagram shows the input components, data collection and preprocessing, the AI Processing Engine, the Adaptive Focus Engine and the system outputs.

![FocusMate System Architecture](screenshots/FocusMate%20System%20Architecture%20Infographic.png)

## 14. Observations and Critical Analysis

- Students face several types of distraction, not only mobile notifications.
- Combining noise management, app restrictions and attention estimation is more comprehensive than a basic productivity timer.
- NLP can prioritise notifications, but misclassification could cause important messages to be missed.
- Eye tracking can produce false alerts, because looking away does not always mean distraction.
- Camera and notification processing need strong privacy safeguards.
- Multiple hardware components raise cost and may limit accessibility.
- Personalised sessions may suit students better than one fixed timer.
- AI recommendations should support students without unnecessarily interrupting them.
- Accessibility and customisation matter because study preferences differ.
- Evaluation is needed to show whether the features genuinely improve study behaviour.

A key limitation is that eye movement and app usage cannot directly measure understanding or actual mental concentration, so FocusMate gives estimated indicators rather than definitive claims about attention.

## 15. Learning Outcomes

Through this group activity, I gained experience in:

- Identifying real-world problems that can be addressed with AI.
- Understanding how AI can be integrated into everyday applications.
- Exploring practical uses of Computer Vision, NLP, Machine Learning and recommendation systems.
- Understanding practical applications of Large Language Models in education.
- Designing an integrated AI-powered product with a user-centred approach.
- Identifying privacy, security, accessibility and ethical considerations.
- Evaluating the practicality and limitations of AI-based solutions.

## 16. Tools and Technologies

| Component | Proposed technologies |
|---|---|
| Mobile Application | Android / Flutter |
| Backend Services | Python / FastAPI |
| Computer Vision | OpenCV / MediaPipe |
| Eye Analysis | Eye Aspect Ratio / PERCLOS |
| NLP | Transformer-based NLP models |
| Machine Learning | Scikit-learn / PyTorch |
| LLM Integration | Suitable LLM API or locally hosted model |
| Data Storage | SQLite / PostgreSQL |
| Analytics | Python / Mobile dashboard |
| Hardware Integration | Compatible Bluetooth headsets and cameras |

These are proposed technologies and do not imply that a working implementation has been developed.

## 17. Files Included

- `README.md` – Full FocusMate design and lab report (this file).
- `group-activity/group-members.md` – Group member information.
- `group-activity/activity-outcomes.md` – Outputs and decisions of the group activity.
- `group-activity/discussion-summary.md` – Summary of the group discussion.
- `screenshots/focusmate-system-overview.png` – System overview infographic.
- `screenshots/focusmate-system-architecture.png` – System architecture diagram.

## 18. Conclusion

FocusMate proposes an AI-powered approach to managing student distractions by combining smart hardware, mobile application features, Computer Vision, NLP, Machine Learning, recommendations and an optional LLM study assistant. Its aim is not simply to restrict distractions but to understand individual study behaviour and give appropriate support when needed. With adaptive focus management, context-aware notification filtering, privacy-first processing and personalised recommendations, it aims to create a smarter and more accessible study environment for students.