# Facilities_Coordinator
Facilities Coordinator
# Facilities Coordinator AI Persona

## Overview
This repository contains the JSON persona definition for **Alex Mercer**, an AI agent specialized in Facilities Coordination. This persona is designed to be integrated into chatbots, internal ticketing systems, or voice assistants to provide intelligent, empathetic, and efficient facilities management support.

## Key Capabilities
- **24/7 Incident Triage**: Handles urgent maintenance, safety hazards, and environmental issues in real-time.
- **Workflow Automation**: Routes tickets to appropriate vendors, schedules preventive maintenance, and updates stakeholders.
- **Data-Driven Decisions**: Leverages BIM, historical work orders, and occupancy data to optimize space and energy usage.
- **Compliance Enforcement**: Ensures all responses adhere to OSHA, ADA, and local building codes.

---

## Integration Instructions

### 1. Prerequisites
- A JSON parser (built into most programming languages).
- An AI orchestration layer (e.g., LangChain, Rasa, or custom Python/Node.js backend).
- (Optional) API keys for external systems (e.g., ServiceNow, Jira, or building management software).

### 2. Loading the Persona
Load the `facilities_coordinator_persona.json` file into your AI system's memory. For example, in Python:

```python
import json

with open('facilities_coordinator_persona.json', 'r') as f:
    persona_data = json.load(f)

# Inject the persona data into the system prompt
system_prompt = f"""
You are now {persona_data['persona']['name']}, a {persona_data['persona']['role']}.
Your core competencies are: {', '.join(persona_data['core_competencies'])}.
Communication style: {persona_data['communication_style']['tone']}.
Constraints: {', '.join(persona_data['constraints'])}.
Always begin interactions with: {persona_data['greeting_message']}
"""
