# AI Voice Calling System

An AI-powered outbound voice calling solution built using ElevenLabs Conversational AI, Twilio Telephony, and n8n Workflow Automation.

This project demonstrates how AI voice agents can automate customer interactions, conduct outbound calls, support multiple languages, schedule callbacks, handle escalations, and provide a natural conversational experience.

---

## Overview

The system uses ElevenLabs Conversational AI integrated with Twilio to place outbound calls and engage customers through natural voice conversations.

The solution is designed to:

- Automate outbound calling campaigns
- Handle customer interactions intelligently
- Support multilingual conversations
- Schedule callbacks automatically
- Manage customer enquiries
- Escalate requests to human representatives when needed

---

## Features

### Outbound Voice Calling

- Automated outbound calls
- Personalized customer conversations
- Dynamic customer information support
- Natural voice interaction

### Multilingual Support

Supported languages:

- English
- Malayalam
- Hindi

The agent automatically responds in the language used by the customer.

### Customer Interaction Handling

The voice agent can handle:

- General enquiries
- Callback requests
- Human representative requests
- Busy customers
- Existing customers
- Wrong number scenarios
- Complaint handling
- Follow-up conversations

### Conversation Management

- Natural conversational flow
- Silence detection and recovery
- Unclear speech handling
- Professional call closing
- Human-like interaction design

### Batch Calling

- CSV-based bulk calling
- Dynamic variable mapping
- Personalized outbound campaigns

---

## Technology Stack

| Component | Technology |
|------------|------------|
| Conversational AI | ElevenLabs |
| Telephony | Twilio |
| Workflow Automation | n8n |
| Voice Interaction | ElevenLabs Conversational AI |
| Call Routing | Twilio Voice |
| Callback Scheduling | n8n + ElevenLabs |
| Prompt Engineering | Custom AI Prompts |

---

## Implementation Highlights

### ElevenLabs Configuration

Successfully configured:

- Conversational AI Agent
- System Prompt Design
- Dynamic Variables
- Multilingual Support
- Silence Handling Logic
- End Call Logic
- Customer Interaction Flows

### Twilio Integration

Successfully configured:

- Twilio Account Setup
- Telephony Integration
- Phone Number Configuration
- Outbound Call Routing
- End-to-End Call Testing

### n8n Workflow Automation

Successfully configured:

- Webhook-Based Trigger
- Callback Scheduling Workflow
- Delay/Wait Automation
- Outbound Call Triggering
- Automated Follow-up Calls
- Integration with ElevenLabs APIs

---

## Batch Calling

Implemented CSV-based calling campaigns.

### Example CSV Format

```csv
phone_number,customer_name,company_name
+91111111111,John,ABC Technologies
+919876543210,Rahul,XYZ Solutions
```

---

## Supported Use Cases

### Customer Available

- Introduce services
- Understand requirements
- Answer basic questions
- Qualify leads

### Customer Busy

- Capture callback requests
- Schedule future conversations
- Automatically trigger callbacks

### Human Escalation

- Record escalation requests
- Transfer follow-up to human teams

### Existing Customers

- Provide additional assistance
- Capture service requirements

### Wrong Number Handling

- Verify contact information
- Request alternative contacts

### Complaint Handling

- Acknowledge customer concerns
- Record and escalate issues

### Silence Handling

- Multiple retry attempts
- Graceful conversation termination

---

## Dynamic Variables

The system supports dynamic placeholders for personalized conversations.

### Examples

```text
{{customer_name}}
{{company_name}}
{{phone_number}}
{{customer_phone_number}}
```

These values are automatically injected during call execution.

---

## Callback Automation

The system supports intelligent callback scheduling for customers who are unavailable during the initial conversation.

### Supported Callback Requests

Examples:

- Call me after 5 minutes
- Call me after 10 minutes
- Call me after 30 minutes
- Call me after 1 hour
- Call me later
- I am busy
- I am in a meeting
- I am driving
- I cannot talk now
- Please call me back later

### Callback Workflow

1. Customer requests a callback.
2. AI agent identifies the callback request.
3. Callback duration is extracted.
4. Duration is converted into minutes.
5. The callback request is sent to n8n via webhook.
6. n8n stores callback details.
7. n8n waits for the requested duration.
8. n8n triggers a new outbound call.
9. ElevenLabs initiates the callback.
10. Customer receives the scheduled callback.

### Callback Time Conversion

| Customer Request | Callback Minutes |
|------------------|------------------|
| 5 minutes | 5 |
| 10 minutes | 10 |
| 30 minutes | 30 |
| 1 hour | 60 |
| 2 hours | 120 |

### Dynamic Phone Number Support

The callback workflow uses dynamic customer phone numbers.

Example:

```json
{
  "customer_phone_number": "+911234567890"
}
```

The phone number is passed dynamically during outbound call execution and reused for callback scheduling.

### Callback Components

- ElevenLabs Conversational AI
- n8n Workflow Automation
- Webhook Trigger
- Wait Node
- Outbound Call API
- Dynamic Variables

---

## Workflow Architecture

```text
Customer
    │
    ▼
ElevenLabs AI Agent
    │
    ▼
schedule_callback Tool
    │
    ▼
n8n Webhook
    │
    ▼
Wait Node
    │
    ▼
ElevenLabs Outbound Call API
    │
    ▼
Customer Callback
```

---

## Testing Results

| Feature | Status |
|----------|----------|
| Agent Configuration | ✅ Completed |
| Twilio Integration | ✅ Tested |
| Outbound Calling | ✅ Tested |
| Multilingual Support | ✅ Tested |
| Dynamic Variables | ✅ Implemented |
| Batch Calling | ✅ Tested |
| Callback Handling | ✅ Tested |
| Human Escalation Flow | ✅ Implemented |
| Silence Handling | ✅ Tested |
| Call Ending Logic | ✅ Implemented |
| n8n Integration | ✅ Implemented |
| Callback Scheduling Workflow | ✅ Tested |
| Automated Callback Execution | ✅ Tested |
| Webhook Integration | ✅ Tested |

---

## Key Learnings

During this project, the following areas were explored:

- Conversational AI Design
- Prompt Engineering
- Voice Agent Development
- Telephony Integration
- Outbound Call Automation
- Callback Scheduling Automation
- Customer Interaction Workflows
- Dynamic Data Injection
- Workflow Automation using n8n
- Multilingual Voice Experiences
- AI-Powered Customer Engagement

---

## Project Status

**Status: Completed, Successfully Tested, and Enhanced with Automated Callback Scheduling**

The system successfully demonstrates how AI-powered voice agents can automate outbound customer communication using ElevenLabs, Twilio, and n8n while maintaining a natural and professional conversational experience.

### Implemented Capabilities

- AI-Powered Outbound Calling
- Multilingual Customer Interaction
- Dynamic Variable Injection
- Batch Calling Campaigns
- Human Escalation Workflows
- Automated Callback Scheduling
- Webhook-Based Automation
- n8n Workflow Integration
- Twilio Telephony Integration
- ElevenLabs Conversational AI
