# Natural Language Interaction Protocol (NLIP)

**NLIP** is an *open*, vendor-neutral application-layer protocol that lets independent **intelligent agents** running on phones, servers, IoT gateways, browsers, or HPC clusters exchange information in a well-typed, secure, multi-modal envelope. 
The official standards can be downloaded from the Ecma website.

<code>
* [ECMA-430: Natural Language Interaction Protocol (NLIP)](https://ecma-international.org/publications-and-standards/standards/ecma-430/)
* [ECMA-431: Binding of NLIP over HTTP/HTTPS](https://ecma-international.org/publications-and-standards/standards/ecma-431/)
* [ECMA-432: Binding of NLIP over WebSocket](https://ecma-international.org/publications-and-standards/standards/ecma-432/)
* [ECMA-433: Binding of NLIP over AMQP](https://ecma-international.org/publications-and-standards/standards/ecma-433/)
* [ECMA-434: Security profiles for NLI](https://ecma-international.org/publications-and-standards/standards/ecma-434/)
* [EMCA TR/113: Explanatory guide to NLIP](https://ecma-international.org/publications-and-standards/technical-reports/ecma-tr-113/)
</code>
## Overview

The Natural Language Interaction Protocol (NLIP) is envisioned as the common wiring layer for the next generation of reasoning systems. Just as TCP/IP turned heterogeneous networks into a single Internet and HTTP unified document exchange, NLIP’s goal is to standardize the envelope, control signals, and policy semantics by which intelligent agents exchange information in natural language (and other modalities). Whether those agents speak on behalf of people, devices, cloud services, or entire organizations, NLIP supplies the predictable substrate that lets them cooperate safely and efficiently.

### NLIP will establish
- A standardized message format for multimodal data exchange between client and server agents, primarily using JSON.
- A protocol specification that defines message types, structure, and control mechanisms necessary for managing sessions, privacy, policy negotiation, and performance optimization.
- A secure communication model, including authentication, encryption, and identity management.
- Flexibility in deployment, supporting various platforms, modalities (text, audio, video, images), concurrent sessions, and underlying transport protocols (initially HTTPS/REST).
- Bindings for base protocols, beginning with a RESTful HTTPS binding to ensure wide accessibility and ease of implementation.

### Why a public, standardized protocol?

| Challenge with proprietary APIs | NLIP advantage |
|---------------------------------|----------------|
| Each vendor invents its own JSON dialect, auth scheme and rate-limit headers. | **Single grammar & control frames**—every compliant agent can talk to every other on day 1. |
| Switching cloud providers or LLM back-ends means rewriting glue code. | **Platform portability**: choose or swap engines without breaking higher layers. |
| Policy negotiation (privacy, jurisdiction, DoS limits) is bolted on per-API. | **First-class policy tokens** travel inside the envelope—auditable and machine-verifiable. |
| Innovation happens in silos; specs change by fiat. | **Open governance (Ecma TC-56)** ensures transparent decision-making and conformance suites for everyone. |

## Protocol at a glance

* **Envelope** – A JSON object whose first sub-message carries `format`, `subformat`, `content`; optional sub-messages attach images, policy tokens (`conversation`, `authentication`), or control directives.
* **Transport-agnostic** – Initial binding is HTTPS/REST; QUIC, WebRTC, gRPC and others can be added without changing the envelope.
* **Multi-modal** – `text/english`, `binary/image/jpeg`, `structured/uri`, `location/gps`, `generic/<ext>` … all legal in the same exchange.
* **Hot-extensible** – New formats or sub-protocols negotiate at runtime; old agents keep working.

### Exclusions
- NLIP does not aim to provide interoperability with existing proprietary systems directly.
- The project excludes the creation of specific end-user applications, focusing solely on protocol and specification.

Think: less app fatigue, more seamless automation.

## Key principles

| Principle | What it means in practice |
|-----------|---------------------------|
| **Openness** | Apache-licensed reference code, public issue tracker, decision records. |
| **Vendor neutrality** | No preferred cloud, LLM, language or runtime; conformance is purely at the wire level. |
| **Security first** | Mandatory encrypted transport, pluggable auth, negotiable rate-controls, anonymous mode. |
| **Forward compatibility** | Extension points and version tags prevent “flag day” upgrades. |

## Contributing

We welcome contributions to the spec and implementations! You can:

- File issues and pull requests
- Propose new extensions (see `/proposals/`)

Please see [Contributing Guidelines](CONTRIBUTING?id=contributing-to-nlip) and [Code of Conduct](CODE_OF_CONDUCT?id=code-of-conduct).

## Governance

Please see [Governance](GOVERNANCE?id=governance)

## Support

Please see [Support](SUPPORT?id=support)

## Security

Please see [Security Policy](SECURITY?id=security-policy)

## License

- **Specs** are licensed under Ecma International’s copyright terms
- **Code** is Apache 2.0

See [`License`](LICENSE) for full terms.

## Resources

- Website: [https://nlip-project.org](https://nlip-project.org/#/)
- Chat: `#nlip`
- Discussions: `#nlip`

> Maintained by Ecma TC-56 and the NLIP community.
