# SafeStack Validation Registry

This repository maintains the official registry of validated SafeStack projects, nodes, and cryptographic specifications.

Projects registered here must:
- Comply with the **Root Canon** (`safestack-canon` v1.0.0)
- Comply with the **Technical Canon** (`safestack-technical-canon` v1.0.0)
- Possess a verified entry in [`safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- Provide reproducible cryptographic artifact hashes and signatures

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

### 1. SafeStack PI5 VPN Freedom
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-PI5-VPN-Freedom`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-PI5-VPN-Freedom)
- **Deployment:** Raspberry Pi 5 Autonomous Zero-Trust VPN Node & Web Control Panel
- **Compliance Status:** **Fully Validated** (Root Canon v1.0.0, Technical Canon v1.0.0)
- **Artifact Hash Manifest:** `release/safestack-pi5.sha256`
- **Signing Public Key:** Registered in [`safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys) (`release-signing/safestack-pi5-2026.pub`, fingerprint `SHA256:6bUvQeyGzXxDIUMnUyIoJPRbEeX3khAhRmYycwmgJq4`)
- **Attestation & Declaration:** [`VALIDATION.md`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-PI5-VPN-Freedom/blob/main/VALIDATION.md)
- **Security Audit:** Lynis 3.1.7 Hardening Index 81/100, 0 CVEs

### 2. SafeStack Technical Canon
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-technical-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon)
- **Role:** Technical governance, schema specifications, and cryptographic hash registry
- **Compliance Status:** **Fully Validated** (Technical Canon v1.0.0, Status ACTIVE)
- **Key Fingerprint:** `13034f6afa3a1f1d8db6d0cb9c5c83210d8f01a90036308dd8db5813e5e827e4` (`project-012`)
- **Integrity Anchor:** `TECHNICAL_CANON.json` (SHA-256: `596ad60c745505440863e5e77a042ecf2e8506ae482555e03e07550704745bdf`)

### 3. SafeStack Control Architecture
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-control-architecture`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-control-architecture)
- **Role:** 5-Layer Control Model (Network, Encryption, Infrastructure, Application, Identity)
- **Compliance Status:** **Fully Validated** (Architectural Framework)
- **Key Fingerprint:** `e91f92abe2e4ca9d4b65dd6c49e8230ff2d7266c0a6990d91e104628a89b6766` (`project-006`)
- **Dossier:** `index.html` (published control dossier)

### 4. SafeStack Zero Trust
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust)
- **Role:** Local-first policy decision engine, default deny, and device posture gates
- **Compliance Status:** **Fully Validated** (v0.1.0)
- **Key Fingerprint:** `8c7f6e91f092a482d3b250e97b8d5ea4302bc771b101346f8ba2d4ee460c7259` (`project-014`)
- **Package:** `safestack-zt` CLI with Ed25519 bundle signing & verification

### 5. SafeStack Project Public Keys
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- **Role:** Central root-signed Ed25519 identity key registry and release signing keys
- **Compliance Status:** **Fully Validated** (Schema: `safestack.project-key-registry.v1`)
- **Key Fingerprint:** `a3c6dd7cbcca31eb861a8de8dbe13f33fe21e59335c1f31388dbffb44ea1b141` (`project-013`)
- **Root Public Key:** `z8oMmyDuGRm4eqNiML6Av2B16GCNMcDOrpZJwaJGsgY=`

### 6. Verification Artifacts
- **Repository:** [`kibernetinio-saugumo-sprendimai/Verification-artifacts`](https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts)
- **Role:** Detached factual cryptographic checksums and verification manifests for external validation
- **Compliance Status:** **Fully Validated**
- **Key Fingerprint:** `cf748daff8695375496791d67ca963e0add179e5065cbc50295fcce1b51bd6e4` (`project-018`)

### 7. SafeStack NodeOS
- **Repository:** [`kibernetinio-saugumo-sprendimai/node-os`](https://github.com/kibernetinio-saugumo-sprendimai/node-os)
- **Deployment:** Autonomous Zero-Trust edge security layer & NVMe health monitoring for Raspberry Pi 5
- **Compliance Status:** **Fully Validated** (v0.2.0, Root Canon v1.0.0, Technical Canon v1.0.0)
- **Key Fingerprint:** `a89d861185c7603c0c01722150ee5ea6d61c5da94cabe99973baa41ab9a9c288` (`project-005`)
- **Public Key:** `A5GWe1zzjq43Rjg9xfNgdSa2u8reF5Z4AkVyvHFoZtw=`
- **Embedded Root Key:** `9760c594fe7e5638a2a6c351db7503817fb803a43cf5ad8547a08d8b6297ad22`
- **Release Manifest:** [`v0.2.0`](https://github.com/kibernetinio-saugumo-sprendimai/node-os/releases/tag/v0.2.0) (`SHA256SUMS`)
- **Attestation:** `AUDIT_REPORT.md` (Ed25519 signed: `AUDIT_REPORT.md.sig`)
