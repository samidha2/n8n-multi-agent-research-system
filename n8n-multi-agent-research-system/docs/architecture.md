# System Architecture

## Overview

This project implements a multi-agent AI research workflow using n8n.

The system combines Google Gemini for language processing, Tavily for web search, and Simple Memory for maintaining conversational context.

## Architecture

```text
User Query
     ↓
Chat Trigger
     ↓
AI Agent #1
     ↓
AI Agent #2
     ↓
Tavily Search
     ↓
Web Information
     ↓
Gemini Processing
     ↓
Final Response
```

## Components

### 1. Chat Trigger

Receives the user's research question through the n8n chat interface.

### 2. AI Agent #1

Processes the initial user request and passes the task through the workflow.

### 3. AI Agent #2

Performs additional processing and can use external tools such as Tavily Search.

### 4. Google Gemini

Provides the language model capabilities for understanding, reasoning, summarization, and response generation.

### 5. Tavily Search

Provides web search capabilities for retrieving external information relevant to the user's query.

### 6. Simple Memory

Maintains conversational context during the interaction.

## Data Flow

```text
User
 ↓
Chat Trigger
 ↓
AI Agent #1
 ↓
AI Agent #2
 ↓
Tavily Search
 ↓
Retrieved Web Information
 ↓
Gemini Processing
 ↓
Final Response
```

## Key Design Principle

The workflow separates AI processing and external information retrieval into multiple stages.

This modular architecture allows additional agents and tools to be added in the future.

## Future Architecture Improvements

Potential improvements include:

- Specialized research agents
- Source citation
- Fact verification
- Research report generation
- Structured outputs
- Persistent memory
- Agent evaluation
- Monitoring and logging