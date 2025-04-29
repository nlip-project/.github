## Use Cases

- Universal travel assistant interacting with transit systems across cities.
- Financial transactions across different banking agents.
- Retail shopping and customer service via a common chat interface.
- Conference support agents that guide users through event logistics.

## Stakeholders

- ECMA Technical Committee 56
- AI platform providers
- App developers and platform integrators
- Enterprises seeking to streamline customer interactions

## Benefits

- Simplified user experience through a unified interaction layer.
- Reduced development and maintenance burden for service providers.
- Enhanced security and privacy controls within conversational interfaces.
- Greater adaptability and innovation through flexible, extensible architecture.

## Key Concepts

- **Agents** – Software systems that use NLIP to communicate
- **Messages** – JSON objects with rich content (text, audio, location, etc.)
- **Control exchanges** – Used to negotiate authentication, policies, session management
- **Binding** – NLIP messages can be sent over different protocols (e.g., HTTPS, gRPC)

## Goals

- Support **multi-modal data** (text, audio, structured data)
- Define clear **security and identity negotiation** mechanisms
- Be **extensible** without breaking older clients
