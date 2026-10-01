# Home-Hospice-Operations-Case-Study-CIS-3001-Client-Project-
Semester long project for Managing with AI class
# Dignified Days: Operational Workflow & Customer Service Optimization
### CIS 3001 | Client Consulting Case Study & AI Systems Analysis

> **Project Type:** Semester-Long Enterprise Operations & Applied AI Consulting  
> **Course:** CIS 3001 — Managing with AI | Georgia State University  
> **Role:** Business & Systems Analyst (Workflow Modeling, Root-Cause Analysis, Systems Architecture)  
> **Client Context:** Dignified Days — Multi-State Durable Medical Equipment (DME) Provider for Home Hospice Care  
> **Project Status:** In Progress (Active Deliverable Cycles)

---

## Executive Summary

**Dignified Days** operates as a critical logistics partner delivering specialized Durable Medical Equipment (DME)—including hospital beds, oxygen concentrators, patient lifts, and pressure-relief mattresses—to home hospice patients across multiple states. 

While the organization maintains a customer-facing tracking portal, operational friction inside customer support and dispatch has created severe service bottlenecks:
* High Customer Service Representative (CSR) handle times on routine delivery queries.
* Manual coordination breakdowns in reverse logistics and equipment reclamation.
* Call center queue lockups caused by basic equipment user error misclassified as mechanical failure.

This project delivers a full-lifecycle systems investigation to evaluate, design, and architect **AI-augmented self-service workflows, automated dispatch scheduling, and intelligent triage systems** without compromising the high-empathy communication required in hospice care.

+-------------------------------------------------------------------------------------------------+
|                                 CORE OPERATIONAL BOTTLENECK TRIAGE                              |
+-----------------------------------+--------------------------------+----------------------------+
| 1. Status Inquiries & Anxiety    | 2. Reverse Logistics Friction  | 3. Malfunction Misdiagnosis|
| 35-45% of inbound call volume.    | Multi-touch coordination.      | 25-30% false-alarm calls.  |
| Tracking portal ignored due to    | Grief-sensitive pickup timing  | Basic operational errors   |
| emotional stress and urgency.     | requires manual CSR calls.     | trigger unnecessary trucks.|
+-----------------------------------+--------------------------------+----------------------------+


### 1. Delivery & Pickup Inquiry Saturation ("Where is my equipment?")
* **Symptom:** Inbound phone queues are continuously saturated with family members and hospice nurses requesting real-time Estimated Time of Arrival (ETA) updates.
* **Root Cause:** A digital self-service tracking portal exists, but under high emotional stress, caregivers default to calling. The portal lacks proactive push communication, forcing CSRs to manually look up driver manifests and bridge dispatch radios while holding callers on the line.

### 2. High-Touch Equipment Return Scheduling (Reverse Logistics)
* **Symptom:** Scheduling equipment pickups post-bereavement or following patient discharge consumes up to 20 minutes of CSR time per instance.
* **Root Cause:** Schedulers must balance vehicle cargo capacity, local disinfection/sanitation protocol windows, and delicate grief-sensitive communication. A lack of automated scheduling integration forces CSRs into protracted back-and-forth phone tag between caregivers and dispatchers.

### 3. Equipment Malfunction Triage Deflection Breakdown
* **Symptom:** Technical escalations flood senior support tiers and trigger costly, unnecessary field dispatches for presumed hardware failures.
* **Root Cause:** Approximately 25–30% of reported "breakdowns" (e.g., oxygen concentrator flow alerts, hospital bed hand-control lockouts) stem from basic user error or unseated power cables. Without structured diagnostic triage at the intake layer, frontline CSRs immediately reroute tickets to emergency dispatch.

---

## Target Measurable Organizational Value (MOV)

The project's architectural recommendations are evaluated against concrete operational and financial targets:

| Operational Metric | Baseline Performance | Target MOV (Post-Implementation) | Business Impact |
| :--- | :--- | :--- | :--- |
| **Routine ETA Inquiry Deflection** | 0% automated deflection | **40%–50% Deflection** | Redirects routine traffic to automated SMS/IVR, freeing bandwidth for high-acuity hospice calls. |
| **Average Handle Time (AHT) - Returns** | 15–20 minutes / transaction | **< 6 minutes / transaction** | Compresses scheduling steps via dynamic self-service calendar integration. |
| **First-Touch Triage Accuracy** | ~50% misclassification | **75%+ Accurate Resolution** | Resolves non-mechanical issues at intake, avoiding costly emergency truck rolls. |
| **Customer / Caregiver CSAT** | Declining due to hold times | **> 90% Satisfaction** | Provides immediate, 24/7 visibility during urgent hospice transitions. |

---

## Proposed System Architecture & AI Workflows

                       [ Inbound Caregiver / Nurse Request ]
                                         │
                    ┌────────────────────┴────────────────────┐
                    ▼                                         ▼
        [ Voice IVR Channel ]                      [ SMS / Web Channel ]
                    └────────────────────┬────────────────────┘
                                         │
                              [ Intelligent Intake Layer ]
                     (Intent Extraction & Sentiment Classification)
                                         │
             ┌───────────────────────────┼───────────────────────────┐
             ▼                           ▼                           ▼
    [ Delivery / ETA ]          [ Equipment Return ]        [ Equipment Issue ]
             │                           │                           │
    Automated Look-up           Bereavement Workflow        Guided Diagnostic Triage
             │                           │                           │
    Proactive SMS Push          Direct Calendar Booking     Fix Validated?
             │                           │                   ├── YES: Resolved (No roll)
             ▼                           ▼                   └── NO : High-Priority Tech
    [ Order Closed ]            [ Dispatch Update ]                 [ CSR Escalation ]

* **Intelligent Front-Door Triage (Conversational AI / NLU):** Classifies caregiver intent instantly across voice (IVR) and digital channels. Urgent hospice-critical needs bypass automation straight to dedicated emergency agents.
* **Proactive Status Engine (Event-Driven Logistics):** Integrates ERP inventory with vehicle telematics (GPS) to send automated, proactive milestone SMS alerts ("Driver is 2 stops away"), preempting manual calls.
* **Interactive Guided Diagnostic Trees:** Implements guided, multimodal visual troubleshooting workflows (QR-code accessible directly on the equipment chassis) to walk users through simple reset sequences.
* **Dynamic Dispatch & Reverse Logistics Scheduling:** Embeds direct route-optimization APIs into self-service forms, letting caregivers confirm pickup slots directly against local truck capacity.

---

## Project Phases & Ongoing Deliverables

* [x] **Phase 1: Project Charter & Business Case Formulation**
  * Elicited business needs, synthesized problem statements, mapped current-state pain points, and defined project MOV metrics.
* [ ] **Phase 2: As-Is vs. To-Be Systems & Data Flow Analysis (In Progress)**
  * Documenting current operational handoffs using Swimlane process diagrams and Draw.io Entity-Relationship Diagrams (ERDs).
* [ ] **Phase 3: AI Technology Stack Evaluation & Risk Framework**
  * Evaluating LLM/NLP middleware, data governance, and HIPAA-compliant architecture options for protected health operations.
* [ ] **Phase 4: Functional Prototyping, Triage Decision Matrix & Final Advisory**
  * Final business report detailing cost-benefit analysis (ROI), transition roadmaps, and change
---

## Core Operational Bottlenecks & Root-Cause Analysis
