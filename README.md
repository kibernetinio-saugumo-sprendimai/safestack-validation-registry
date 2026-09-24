# SafeStack Validation Registry

This repository maintains the official authoritative registry of validated SafeStack projects, nodes, and cryptographic specifications.

Projects registered here must:
- Comply with the **Root Canon** (`safestack-canon` v1.0.0)
- Comply with the **Technical Canon** (`safestack-technical-canon` v1.0.0)
- Possess a verified entry in [`safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- Provide reproducible cryptographic artifact hashes (`SHA256SUMS`) and signed audit reports

---

## Canonical Authority & Verification

- **Root Reference:** `ROOT_REFERENCE.txt` &rarr; [`safestack-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-canon)
- **Technical Reference:** `TECH_REFERENCE.txt` &rarr; [`safestack-technical-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon)
- **Registry State:** `REGISTRY.json` (SHA-256: `cb1e7ea061dd9a0b37788c833d3ee88247828d20a9e34d605ab18ed08c913cd2`)
- **Detached Signature:** `REGISTRY.json.asc`
- **Verification Command:**
  ```bash
  shasum -a 256 -c REGISTRY_HASH.txt
  ```

---

## Validated Ecosystem Projects

### 1. SafeStack NodeOS
- **Repository:** [`kibernetinio-saugumo-sprendimai/node-os`](https://github.com/kibernetinio-saugumo-sprendimai/node-os)
- **Deployment:** Autonomous Zero-Trust edge security layer & NVMe health monitoring for Raspberry Pi 5
- **Compliance Status:** **Fully Validated** (v0.2.0, Root Canon v1.0.0, Technical Canon v1.0.0)
- **Key Fingerprint:** `a89d861185c7603c0c01722150ee5ea6d61c5da94cabe99973baa41ab9a9c288` (`project-005`)
- **Release Manifest:** [`v0.2.0`](https://github.com/kibernetinio-saugumo-sprendimai/node-os/releases/tag/v0.2.0) (`SHA256SUMS`)
- **Attestation:** `AUDIT_REPORT.md` (Ed25519 signed: `AUDIT_REPORT.md.sig`)

### 2. SafeStack Audit System
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-audit_system`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-audit_system)
- **Role:** Deterministic AI-assisted security audit pipeline and fail-closed runtime governance
- **Compliance Status:** **Fully Validated** (v2.0.0, 25/25 automated tests OK)
- **Key Fingerprint:** `1ca5120e6237db1148bf328d269dc783d96bde8aba213cf68c50bbdb3c3b131e` (`project-001`)
- **Manifest:** `SHA256SUMS` (58 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 3. SafeStack Technical Canon
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-technical-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon)
- **Role:** Technical governance, schema specifications, and cryptographic hash registry
- **Compliance Status:** **Fully Validated** (Technical Canon v1.0.0, Status ACTIVE)
- **Key Fingerprint:** `13034f6afa3a1f1d8db6d0cb9c5c83210d8f01a90036308dd8db5813e5e827e4` (`project-012`)
- **Integrity Anchor:** `TECHNICAL_CANON.json` (SHA-256: `596ad60c745505440863e5e77a042ecf2e8506ae482555e03e07550704745bdf`)

### 4. SafeStack Control Architecture
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-control-architecture`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-control-architecture)
- **Role:** Layered Control Model (Network, Encryption, Infrastructure, Application, Identity)
- **Compliance Status:** **Fully Validated** (Architectural Framework)
- **Key Fingerprint:** `e91f92abe2e4ca9d4b65dd6c49e8230ff2d7266c0a6990d91e104628a89b6766` (`project-006`)
- **Dossier:** `index.html` (published control dossier)

### 5. SafeStack Zero Trust
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust)
- **Role:** Local-first policy decision engine, default deny, and device posture gates
- **Compliance Status:** **Fully Validated** (v0.1.0, 6/6 automated tests OK)
- **Key Fingerprint:** `fbca5cce3c88dced96f0439414e91e524bfce550f29f4131db360aaf25f7373d` (`project-014`)
- **Manifest:** `SHA256SUMS` (15 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 6. SafeStack Zero-Trust Platform
- **Repository:** [`kibernetinio-saugumo-sprendimai/SafeStack-Zero-Trust-Platform`](https://github.com/kibernetinio-saugumo-sprendimai/SafeStack-Zero-Trust-Platform)
- **Role:** Zero-trust security platform and decentralized policy orchestration components
- **Compliance Status:** **Fully Validated** (v0.1.0, 14/14 automated tests OK)
- **Key Fingerprint:** `07daa52d48ba769fce52cd8c1a87a63d72d48a9a6a49ce9473da70e8cae9dde9` (`project-015`)
- **Manifest:** `SHA256SUMS` (48 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 7. SafeStack Sentinel
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-Sentinel`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Sentinel)
- **Role:** Continuous node security monitoring and telemetry daemon
- **Compliance Status:** **Fully Validated** (v0.1.0, 4/4 automated tests OK)
- **Key Fingerprint:** `b224f35d049e73b964d5b7fa1849f26b9d5896f4bcbe0a85ed7c9ff52743150f` (`project-010`)
- **Manifest:** `SHA256SUMS` (43 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 8. SafeStack Suite
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-suite`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-suite)
- **Role:** Integrated runtime utilities and cryptographic CLI tools
- **Compliance Status:** **Fully Validated** (v0.1.0, 2/2 automated tests OK)
- **Key Fingerprint:** `884a930c8c55a76d126aaddbba74240f868a70f60102ff7bb61a0b6d6a6218bc` (`project-011`)
- **Manifest:** `SHA256SUMS` (23 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 9. SafeStack OSINT
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-OSINT`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-OSINT)
- **Role:** Modular, policy-driven OSINT framework with cryptographic integrity verification
- **Compliance Status:** **Fully Validated** (v1.5.0, 5/5 automated tests OK)
- **Key Fingerprint:** `49b30c612f117ee4dd4f46c2cfa81f59b6dfa5f76b10da1e745fd863dd43087d` (`project-007`)
- **Manifest:** `SHA256SUMS` (65 verified files)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 10. SafeStack Project Public Keys
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- **Role:** Central root-signed Ed25519 identity key registry and release signing keys
- **Compliance Status:** **Fully Validated** (Schema: `safestack.project-key-registry.v1`)
- **Key Fingerprint:** `a3c6dd7cbcca31eb861a8de8dbe13f33fe21e59335c1f31388dbffb44ea1b141` (`project-013`)
- **Root Public Key:** `z8oMmyDuGRm4eqNiML6Av2B16GCNMcDOrpZJwaJGsgY=`

### 11. Verification Artifacts
- **Repository:** [`kibernetinio-saugumo-sprendimai/Verification-artifacts`](https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts)
- **Role:** Detached factual cryptographic checksums and verification manifests for external validation
- **Compliance Status:** **Fully Validated**
- **Key Fingerprint:** `cf748daff8695375496791d67ca963e0add179e5065cbc50295fcce1b51bd6e4` (`project-018`)
- **Verification Engine:** `verify_ecosystem.py`
