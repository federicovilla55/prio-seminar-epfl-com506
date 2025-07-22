# Prio: Private, Robust, and Scalable Computation of Aggregate Statistics

> Student seminar: security protocols and applications - [COM-506](https://edu.epfl.ch/coursebook/en/student-seminar-security-protocols-and-applications-COM-506) @ EPFL, Spring 2025

## Topic

__Prio__, a privacy-preserving system for computing aggregate statistics over sensitive client data without revealing individual data points and without sacrificing scalability. The system was presented by _Corrigan-Gibbs_ and _Boneh_ at [_NSDI 2017_](https://www.usenix.org/conference/nsdi17/technical-sessions/presentation/corrigan-gibbs).

Prio combines two key cryptographic primitives:

- _Secret-shared Non-Interactive Proofs_ (_SNIPs_): zero knowledge proofs that enable clients to prove the correctness of their private data without revealing it.
- _Affine-Aggregatable Encodings_ (_AFEs_): encode client inputs into vectors to allow the servers to aggregate the encodings and compute complex statistics.

The system is designed to achieve:

- _Privacy_, as no single server ever sees raw client data
- _Robustness_, as maliciously malformed data is rejected
- _Scalability_, as the system introduces minimal overhead, even at large scale

The protocol is used in various real-world scenarios:

- Collecting anonymized browser statistics ([Mozilla Firefox](https://blog.mozilla.org/en/firefox/partnership-ohttp-prio/) - [Next steps in privacy-preserving Telemetry with Prio](https://blog.mozilla.org/security/2019/06/06/next-steps-in-privacy-preserving-telemetry-with-prio/)).
- Federated learning and privacy-preserving machine learning ([FastSecAgg: Scalable Secure Aggregation for Privacy-Preserving Federated Learning](https://arxiv.org/abs/2009.11248) - [Samplable Anonymous Aggregation for Private Federated Data
Analysis](https://arxiv.org/abs/2307.15017)).
- Secure and private telemetry in mobile devices ([Exposure notification privacy-preserving analytics by Apple and Google](https://covid19-static.cdn-apple.com/applications/covid19/current/static/contact-tracing/pdf/ENPA_White_Paper.pdf)).

## Materials

- [Report](report/prio-report.pdf)
- [Presentation](presentation/prio-presentation.pdf)

## Acknowledgements

This work is based on the research by Henry _Corrigan-Gibbs_ and _Dan Boneh_ presented at _NSDI 2017_ ([Original Paper](https://crypto.stanford.edu/prio/paper.pdf)).