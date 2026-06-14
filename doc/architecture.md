# Inquiro Advanced Content Automation - Architecture

## System Overview

This is a modular, agentic n8n workflow that intelligently routes content-related requests to specialized LLM agents and delivers results via rich email.

## High-Level Architecture

```mermaid
flowchart TD
    A[Webhook Trigger] --> B[Validate & Extract]
    B --> C[Agentic Planning Layer]
    C --> D[Intelligent Agent Router LLM]
    D --> E[Parse Agent Decision]
    E --> F[Switch Router]
    F --> G1[Summarization Agent]
    F --> G2[Content Creation]
    F --> G3[Content Improvement]
    F --> G4[Research Agent]
    F --> G5[Analytics Agent]
    F --> G6[General Assistant]
    F --> G7[Clarification Agent]
    G1 --> H[Assemble Email Response]
    G2 --> H
    G3 --> H
    G4 --> H
    G5 --> H
    G6 --> H
    G7 --> H
    H --> I[Send Response JSON]
    H --> J[Send Gmail]
