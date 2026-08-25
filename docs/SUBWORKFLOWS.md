# Linked Sub-workflows

The original production architecture is modular. The main AI agent orchestrates specialized
n8n sub-workflows instead of putting every integration and transactional step into one canvas.

The public repository intentionally omits their internal production implementation.

| Public component | Responsibility |
|---|---|
| `resolveSchedulingCriteria` | Maps specialty, provider, coverage/modality and business criteria to internal scheduling identifiers |
| `checkAvailability` | Retrieves current appointment availability from the scheduling platform |
| `createPatient` | Creates a patient record when required |
| `findPatient` | Finds an existing patient before transactional actions |
| `bookAppointment` | Performs the final appointment-booking action |
| `searchAppointments` | Retrieves active appointments for lookup/cancellation/rescheduling |
| `cancelAppointment` | Cancels a confirmed appointment |
| `joinWaitlist` | Registers scheduling preferences for the waitlist |
| `humanHandoff` | Transfers context to a human operator |

## Why not publish every sub-workflow?

For a portfolio, the main goal is to prove that the system was architected and shipped, not to
publish an entire client's production environment.

The main workflow already demonstrates:

- orchestration;
- AI-agent tool use;
- state and memory;
- multimodal input handling;
- Redis buffering;
- CRM integration;
- API interaction;
- transactional safety;
- fallback / escalation design.

If a recruiter asks for deeper technical proof, a single additional sanitized representative
sub-workflow can be shared privately or published as a separate demo.
