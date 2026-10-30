# Formal Verification of TCP with UPPAAL

A timed-automata model of selected TCP connection behaviors, developed in UPPAAL for an academic study of protocol security.

The project examines connection establishment and termination, timing constraints, and two attack scenarios: SYN flooding and TCP reset (RST) injection.

## Scope

- Model TCP client and server behavior using timed automata.
- Explore connection establishment and termination.
- Check reachability and deadlock-related properties.
- Represent SYN Flood and TCP RST Injection attacks.
- Study SYN Cookies and Challenge ACKs as countermeasures.

## Model

The repository's UPPAAL model is [`projet_securit.xml`](projet_securit.xml). It contains the client, server, both attacker automata, and the verification queries.

> The XML model includes the attacker automata. Countermeasure implementations discussed in the project may require a separate or updated model.

## Open in UPPAAL

1. Install UPPAAL from the [official website](https://uppaal.org/).
2. Open `projet_securit.xml` in UPPAAL.
3. Inspect the automata and run the verification queries included in the model.

## Security scenarios

### SYN Flood

The model represents repeated SYN requests that can consume capacity for half-open connections and interfere with legitimate connection attempts.

### TCP RST Injection

The model represents an attacker injecting a TCP RST segment in an attempt to terminate an established connection.

## Countermeasures considered

- **SYN Cookies** reduce the need to retain connection state before the final handshake acknowledgment. See [RFC 4987](https://www.rfc-editor.org/rfc/rfc4987).
- **Challenge ACKs** improve resilience to blind, in-window attacks, including forged resets. See [RFC 5961](https://www.rfc-editor.org/rfc/rfc5961).

## Technology

- [UPPAAL 5.0 / UPPAAL-SMC](https://uppaal.org/) — timed-automata modeling and verification
- [TCP, RFC 9293](https://www.rfc-editor.org/rfc/rfc9293) — protocol specification

## Academic context

**Course:** Security of IoT Protocols and Distributed Systems  
**Academic year:** 2025–2026

## References

- [RFC 9293 — Transmission Control Protocol (TCP)](https://www.rfc-editor.org/rfc/rfc9293)
- [RFC 4987 — TCP SYN Flooding Attacks and Common Mitigations](https://www.rfc-editor.org/rfc/rfc4987)
- [RFC 5961 — Improving TCP's Robustness to Blind In-Window Attacks](https://www.rfc-editor.org/rfc/rfc5961)

## License

No license has been specified for this project.
