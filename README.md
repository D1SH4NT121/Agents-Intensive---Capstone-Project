# Multi-Agent Concierge System

A Python-based **multi-agent concierge system** that routes user requests to specialized agents for restaurants, activities, and bookings. It includes session memory, custom tools, observability, a background monitoring service, and an automated evaluation framework.

## Features

- Multi-agent architecture with specialized roles:
  - RestaurantAgent
  - ActivityAgent
  - BookingAgent
- Custom tools:
  - SearchTool
  - SessionManager
- Session memory with:
  - InMemorySessionService
  - Memory bank for storing user context
- Observability:
  - Logging
  - Tracing
  - Metrics
- Long-running operations support via a background service
- Automated evaluation and testing framework
- Interactive demo workflow
- Competition-ready implementation for a concierge agents track

## How It Works

1. The orchestrator receives a user request.
2. It stores the request in session history.
3. It routes the request to the appropriate agent based on keywords.
4. The selected agent returns a response using available tools and memory.
5. The background service can monitor system health and active sessions.

## Project Structure

- `SessionManager` handles session history and stored memory.
- `SearchTool` returns restaurant, activity, and weather data.
- `RestaurantAgent` handles food and restaurant requests.
- `ActivityAgent` handles activity and sightseeing requests.
- `BookingAgent` creates booking confirmations.
- `ConciergeOrchestrator` manages routing across agents.
- `BackgroundService` monitors active sessions.
- `AgentEvaluator` runs automated tests.

## Example Usage

```python
response = orchestrator.processrequest("demo-session", "I need restaurant recommendations")
print(response)
