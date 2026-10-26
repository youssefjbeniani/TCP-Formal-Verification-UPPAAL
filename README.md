# Formal Verification of the TCP Protocol Using UPPAAL

## Overview

This academic project applies formal verification techniques to the Transmission Control Protocol (TCP) using UPPAAL and timed automata.

The project studies TCP connection establishment, connection termination, timing constraints, and selected security attacks.

## Objectives

- Model TCP client and server behavior using timed automata.
- Verify reachability and deadlock-related properties.
- Model SYN Flood and TCP RST Injection attacks.
- Analyze security countermeasures, including SYN Cookies and Challenge ACK.

## Technologies

- **UPPAAL 5.0 / UPPAAL-SMC** — formal modeling and verification
- **TCP** — protocol specified in RFC 9293
- **Timed automata** — system modeling and analysis

## Project Structure

- `projet_securit.xml` — UPPAAL model containing the Client, Server, SYN Flood attacker, RST attacker, and verification queries.
- `Rapport_Projet_securit.pdf` — project report describing the methodology, security analysis, verification results, and proposed countermeasures.

## Security Attacks Studied

### 1. SYN Flood

The model represents repeated SYN requests that can exhaust the server's half-open connection queue, potentially preventing legitimate connections.

### 2. TCP RST Injection

The model represents an attacker injecting a TCP RST segment to terminate an established connection.

## Countermeasures Discussed

- **SYN Cookies** — mitigate SYN Flood attacks by avoiding the allocation of connection state before the final handshake acknowledgment.
- **Challenge ACK (RFC 5961)** — helps protect TCP connections against blind RST injection.

See the project report for the countermeasure analysis and its reported verification results.

## How to Open the Model

1. Install UPPAAL from the [official UPPAAL website](https://uppaal.org/).
2. Download `projet_securit.xml` from this repository.
3. Open the XML file in UPPAAL.
4. Inspect the automata and verification queries.

**Note:** The uploaded XML represents the model with both attacker automata. The countermeasure implementations described in the report may require a separate or updated model.

## Academic Context

Course project: Security of IoT Protocols and Distributed Systems

Academic year: 2025–2026

## Authors

- Yemen Taoufiq Mahmoud
- Yomna Hlaili
- Youssef Jbeniani

## References

- RFC 9293 — Transmission Control Protocol (TCP)
- RFC 4987 — TCP SYN Flooding Attacks and Common Mitigations
- RFC 5961 — Improving TCP's Robustness to Blind In-Window Attacks

## License

This project is provided for academic and educational purposes. No license has been specified yet.
