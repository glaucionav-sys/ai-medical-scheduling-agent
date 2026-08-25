# Screenshot Guide

Use screenshots from the **sanitized public workflow**, not directly from production.

## Step 1 — import the public JSON

Import `workflow/ai-medical-scheduling-agent-public.json` into a test/personal n8n workspace.

The linked sub-workflows will intentionally be unresolved placeholders. That is expected.

## Take these 4 screenshots

### 1. `01-workflow-overview.png`
- Fit the entire main workflow on screen.
- Show the scale and overall architecture.
- Close execution-data panels.
- Do not show the browser address bar if it exposes a private domain.

### 2. `02-ai-agent-and-tools.png`
Zoom into:
- `AI Medical Scheduling Agent`
- `resolveSchedulingCriteria`
- `checkAvailability`
- `createPatient`
- `findPatient`
- `bookAppointment`
- `searchAppointments`
- `cancelAppointment`
- `joinWaitlist`
- `humanHandoff`

This is the most important screenshot for an AI Automation recruiter.

### 3. `03-message-processing-and-memory.png`
Show:
- webhook / message entry;
- message-type routing;
- audio download + transcription;
- Redis buffer;
- message aggregation;
- conversational memory.

This proves the workflow is more than a simple chatbot.

### 4. `04-booking-orchestration.png`
Show the area where the agent connects to:
- scheduling criteria;
- availability;
- patient lookup;
- booking;
- cancellation/rescheduling;
- human fallback.

## Before saving each screenshot

Check that the screenshot does NOT show:
- credentials;
- API tokens;
- real patient information;
- phone numbers;
- client name/logo;
- production domains;
- real doctor names;
- insurance-specific rules;
- execution payloads.

## Where to put them

Save them inside:

`docs/screenshots/`

After you have the four images, they can be added to the README as a visual case study.
