# VELA — AI Customer Support & Shopping Assistant

VELA is an AI-powered customer support and shopping assistant designed to help customers get accurate product information, receive personalized guidance, and access human support when needed.

The system combines conversational AI, Retrieval-Augmented Generation (RAG), customer data, and automated routing to provide grounded responses while keeping the seller involved when a request requires human attention.

## The Problem

Customer enquiries can involve repetitive questions about products, materials, sizing, ordering, delivery, returns, care, and other business policies.

Answering these questions manually can take significant time, while a general AI assistant may provide inaccurate information if it responds without access to the business's approved knowledge.

Some requests also require live information or human decisions, such as stock availability, order status, tracking, discounts, custom orders, refunds, or exchanges.

## The Solution

VELA uses a business-specific knowledge base to answer customer questions using approved information.

When a customer sends a message, the system analyzes the request and retrieves relevant information from the VELA knowledge base before generating a response.

The assistant can also use available customer information and conversational context to support more personalized interactions.

Requests are routed through two primary paths:

- **ANSWER** — VELA can respond using approved information available to the system.
- **HANDOVER** — the request requires seller attention or information that the AI should not determine independently.

This allows routine customer enquiries to be automated while maintaining human oversight for requests that require business decisions or live information.

## Core Capabilities

- Answer customer questions conversationally
- Retrieve approved business information using RAG
- Provide product and shopping guidance based on available knowledge
- Support product questions about materials, gemstones, sizes, care, and policies
- Provide ring-sizing guidance using approved sizing information
- Use conversational memory to maintain context
- Access available customer information when required
- Distinguish between questions the AI can answer and requests requiring human attention
- Route unresolved or restricted requests to the seller
- Record customer handovers for follow-up
- Send seller notifications when human intervention is required
- Support system error monitoring and daily health checks

## How It Works

A typical customer interaction follows this process:

1. A customer sends a message to VELA through Telegram.
2. The workflow receives and processes the request.
3. VELA identifies the customer's intent and determines what information is required.
4. For VELA-specific questions, the system retrieves relevant information from the approved knowledge base.
5. Relevant knowledge and conversational context are provided to the AI.
6. The AI generates a response grounded in the retrieved information.
7. If the request can be handled using approved information, it follows the ANSWER path.
8. If the request requires seller intervention, live information, or a business decision, it follows the HANDOVER path.
9. Handover information is recorded and the seller is notified.
10. Supporting monitoring workflows track system errors and overall system health.

## Demo

Watch VELA in action as it demonstrates AI-powered customer support, knowledge retrieval, conversational assistance, and human handover when seller intervention is required.

[**Watch VELA Demo**](https://www.loom.com/share/02312112793240e1816b46f2b9216b75)

## Project Screenshots

### Main Workflow Overview

The main n8n workflow orchestrates customer interactions, AI processing, knowledge retrieval, routing, and automated actions.

![VELA Main Workflow Overview](screenshots/%20%20%20%20vela-workflow-overview.PNG)

### Customer Interaction

Customers interact with VELA through Telegram to ask questions and receive conversational assistance.

![VELA Telegram Customer Conversation](screenshots/%20%20%20%20vela-telegram-conversation.PNG)

### RAG Knowledge Retrieval

VELA retrieves relevant business information from the approved knowledge base to ground responses in available VELA-specific information.

![VELA RAG Knowledge Base Retrieval](screenshots/%20%20%20%20rag-knowledge-base.PNG)

### Human Handover

Requests requiring seller attention are routed through the HANDOVER path instead of being handled autonomously by the AI.

![VELA Human Handover](screenshots/%20%20%20%20vela-human-handover.PNG)

### Seller Handover Notification

When human intervention is required, the seller receives a structured notification containing the relevant customer request and handover information.

![VELA Seller Handover Notification](screenshots/%20%20%20%20seller-handover-notification.PNG)

## Retrieval-Augmented Generation (RAG)

VELA uses Retrieval-Augmented Generation to reduce unsupported or invented responses about business-specific information.

The assistant retrieves relevant information from the VELA knowledge base before answering questions about products, materials, gemstones, sizing, ordering, delivery, returns, care, and business policies.

The knowledge base acts as the approved source of truth for VELA-specific information.

If required information is not available or requires live confirmation, the system is designed to route the request for human attention rather than invent an answer.

## Human Handover

Not every customer request should be handled autonomously.

VELA routes requests requiring seller involvement through a HANDOVER path.

Examples can include:

- Live stock availability
- Order status
- Tracking information
- Discounts
- Custom orders
- Refund decisions
- Exchange decisions
- Other requests requiring seller confirmation

This keeps important business decisions under human control while allowing routine enquiries to be handled automatically.

## Human-in-the-Loop Design

VELA is designed to support the seller rather than replace human judgment.

The AI handles repetitive information retrieval and customer-support tasks where approved information is available.

Requests involving live business information, exceptions, approvals, or decisions outside the assistant's authority are escalated for human review.

## Monitoring & Reliability

VELA includes supporting monitoring workflows for:

- Workflow error monitoring and alerts
- Daily system health checks

The daily health check verifies important components supporting the assistant, including the main workflow, knowledge base, customer data, handover records, and AI service connectivity.

These monitoring processes help identify failures and provide visibility into system availability.

## Tech Stack

**Automation & Orchestration:** n8n  
**Customer Interface:** Telegram  
**Knowledge Base & Data:** Supabase  
**AI / LLM Access:** OpenRouter  
**Architecture:** Retrieval-Augmented Generation (RAG)  
**Customer Context:** Conversational memory and customer records  
**Human Handover:** Automated handover routing and seller notifications  
**Monitoring:** n8n error monitoring and daily health checks

## Privacy & Data Handling

Public demonstrations and documentation for VELA use fictional or test customer information only.

No private customer information, API keys, authentication tokens, database credentials, webhook secrets, or other sensitive information are included in the public project documentation.

---

**Built by Lydia Ogbene Odey**  
AI Automation Specialist | Health Tech Automation | Sales & CRM Automation
