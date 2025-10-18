
# hackathon-feedback.md — QuadraTech × Enclave

**Event:** ETH Rome 2025

## What Worked Well

* Technical support during the hackathon
* The tech is really intersting
* More Decentralized than MACI

## What Didn’t Work / Frictions

* Documentation not up to date
* Package installation not compatible with Mac M3 & M4 & Debian 13
* [ ] We did not know which repo to use to start
* [ ] Runtime issues (latency, crashes, edge cases)
* [ ] Dependency installation not clearly indicated
* [ ] Front end demo not fully working, Vote are not showing

---


## Developer Journey (rate 1–5)

* Getting started guide: [ ]1 [X]2 [ ]3 [ ]4 [ ]5
* Error messages/Debuggability: [ ]1 [ ]2 [ ]3 [ ]4 [ ]5
* Local dev loop (build/run/test): [ ]1 [X]2 [ ]3 [ ]4 [ ]5
* Sample apps/templates quality: [ ]1 [X]2 [ ]3 [ ]4 [ ]5

---

## DX Wishlist 

* End‑to‑end quickstart (vote → tally → proof → verify) in <10 min
* Local mock to unit‑test logic without remote infra
* Clear repo to boostrap a project
* Minimal reference UI for QF rounds (plug‑and‑play)

---

### Idea Bank

* **Sybil resistance:** plug‑and‑play modules for Gitcoin Passport (score threshold), BrightID (verified status), Sismo (selective disclosure), World ID (proof‑of‑personhood)
* **Anti‑collusion:** delayed tally reveal, randomized batch ordering, blinded acknowledgements, per‑round salts; publish non‑interactive proofs of correct tallying
* **Transparency:** a public “verify‑the‑round” CLI that downloads artifacts and recomputes commitments locally; reproducible Docker image with hash pinning
* **Usability:** inline proof status on each grant card; one‑click vote receipts; recovery flow if a vote fails mid‑flight
* **Operations:** runbook for incident response; rate‑limit & queueing strategy; circuit breaker when error rate >X%
* **Cost controls:** dynamic batching, off‑peak scheduling, simulation of cost per 1k votes before opening a round
* **Ecosystem:** Hypercerts export for impact attestations; GrantStack import for proposals; zapper to split donations across multiple grants in one action
* **Evaluation rubric for judges:** originality, technical depth, user value, privacy strength, verifiability, polish (rate 1–5 each)
* **Comparison grid (MACI vs Enclave‑backed flow):** columns for DevEx, privacy model, proofs, throughput, operational roles; fill with measured data, not claims
* **Legal & compliance:** DPIA checklist for personal data handling; consent text for participants; data‑retention policy

