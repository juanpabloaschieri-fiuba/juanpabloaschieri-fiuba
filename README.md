# Hi, I'm Juan Pablo Aschieri

Backend and platform engineer from Buenos Aires, Argentina. Informatics Engineer (University of Buenos Aires), Software Developer at Megatrans, and teaching assistant at UBA since 2022.

At work I build event-driven backend systems: a real-time alarm platform that processes thousands of security alarms a day over Apache Kafka, company-wide single sign-on with Keycloak, and the GitLab CI → ArgoCD → Kubernetes pipeline my team ships on. I also lead my team's adoption of structured, spec-driven AI-assisted engineering. That work lives in private repositories.

This profile collects some of what I built at university: mostly Rust, mostly systems: embedded, networking protocols, concurrency and fault-tolerant distributed systems.

## Featured projects

| Project | What it is | Stack |
|---|---|---|
| [**Esp32Framework**](https://github.com/esp32framework/esp32framework) | Final degree project. A framework that makes ESP32 microcontrollers programmable without bare-metal knowledge | Rust, ESP-IDF, BLE, Wi-Fi |
| [**Bitcoin node & wallet**](https://github.com/juanpabloaschieri-fiuba/bitcoin-node-rust) | A Bitcoin testnet node written from scratch, with a desktop wallet | Rust, TCP, GTK |
| [**Fault-tolerant data pipeline**](https://github.com/juanpabloaschieri-fiuba/fault-tolerant-pipeline) | A distributed pipeline that survives nodes being killed mid-run | Python, RabbitMQ, Docker |
| [**Token-ring store network**](https://github.com/juanpabloaschieri-fiuba/token-ring-stores) | Peer-to-peer stores that agree on who ships each online order, without a coordinator | Rust, actix, UDP |
| [**Commodore 64 BASIC interpreter**](https://github.com/juanpabloaschieri-fiuba/commodore64-basic-interpreter) | An interpreter for Commodore 64 BASIC V2 | Clojure |

### Esp32Framework
A layer over the `esp-idf-svc` crate that gives beginners a simple API for GPIO (digital and analog, ADC and PWM), timers with multiple interrupts, I2C and UART, Bluetooth Low Energy (beacon, server and client), HTTP/HTTPS over Wi-Fi and sensor drivers. It also ships its own on-device test runner. Built by a team of four. I'm its top contributor (184 commits): digital I/O and interrupts, the timer driver, the notification system and its async support, the BLE stack, the shared-reference procedural macro, and the test runner.

### Bitcoin node & wallet
A node that joins Bitcoin testnet: it handshakes with peers, downloads and validates the chain in parallel, keeps the UTXO set, and relays blocks and transactions. A GTK wallet on top of it signs and broadcasts transactions and verifies Merkle proofs of inclusion. Team of four. I wrote the most commits (145): handshake, parallel initial block download, disk persistence, validation, transaction sending and the node-to-UI protocol.

### Fault-tolerant data pipeline
Five analytics queries over an Amazon books-and-reviews dataset, run by configurable pools of filter and accumulator workers on RabbitMQ. It keeps giving correct results while a chaos process kills containers at random: acknowledgements, duplicate filtering, a write-ahead log with undo/redo recovery, health checks and leader election. Team of two. I built the persistence and recovery layer, the ack and dedup system, and multi-client support.

### Token-ring store network
Each store is an independent peer on a UDP ring. When an online order comes in, the ring votes and the nearest store with stock ships it. Nodes can join and leave at runtime, and lost messages and dead peers are detected and routed around. Built with actors (actix) and threads.

### Commodore 64 BASIC interpreter
The lexer-to-evaluator core of a Commodore 64 BASIC interpreter, written in functional Clojure. It runs classic programs like Fibonacci, prime sieves and number-base converters.

## Tech
- **Languages:** Rust, C#, Python, Go, Kotlin · also Ruby, Clojure, C, Smalltalk
- **Backend & platform:** Apache Kafka, RabbitMQ, PostgreSQL, SQL Server, Keycloak (SSO/OIDC), Docker, Kubernetes, GitLab CI, ArgoCD
- **Practices:** event-driven and distributed design, concurrent programming, TDD, code review

## Contact
[LinkedIn](https://linkedin.com/in/juan-pablo-aschieri-53b6a62a5)
