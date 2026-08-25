# Sanitization Notes

This repository is a public portfolio version of a production n8n workflow.

## Removed / replaced

- clinic/client identity;
- employee/contact names;
- production phone numbers;
- production messaging tokens and instance identifiers;
- n8n credential references and credential names;
- real API endpoints;
- real webhook path and webhook IDs;
- internal database/table/field identifiers;
- CRM user/department identifiers;
- production Postgres / Redis credential references;
- linked sub-workflow IDs;
- production workflow / instance metadata;
- pinned execution payloads;
- patient/contact data from execution samples;
- clinic address;
- doctor names and provider-specific rules;
- insurance-specific commercial rules;
- proprietary system prompts and business policies.

## Preserved intentionally

- n8n workflow topology;
- node types;
- key orchestration patterns;
- AI-agent/tool architecture;
- Redis buffering architecture;
- memory architecture;
- patient/lead-state concepts;
- booking/cancellation/waitlist patterns;
- safe expressions where they do not expose production data;
- error/human-handoff design.

## Public-demo behavior

The JSON is intended for architecture review and portfolio use.

It will require your own:
- credentials;
- API endpoints;
- database resources;
- CRM configuration;
- linked sub-workflows

before it can run.
