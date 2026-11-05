# SafeStack Validation Registry

This repository maintains the official authoritative registry of validated SafeStack projects, nodes, and cryptographic specifications across [`kibernetinio-saugumo-sprendimai`](https://github.com/kibernetinio-saugumo-sprendimai).

Projects registered here must:
- Comply with the **Root Canon** (`safestack-canon` v1.0.0)
- Comply with the **Technical Canon** (`safestack-technical-canon` v1.0.0)
- Possess a verified entry in [`safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- Provide reproducible cryptographic artifact hashes (`SHA256SUMS`) and signed audit reports

---

## Canonical Authority & Verification

- **Root Reference:** `ROOT_REFERENCE.txt` &rarr; [`safestack-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-canon)
- **Technical Reference:** `TECH_REFERENCE.txt` &rarr; [`safestack-technical-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon)
- **Registry Identity Key (`project-013`):** `a3c6dd7cbcca31eb861a8de8dbe13f33fe21e59335c1f31388dbffb44ea1b141`
- **Genesis Registry State:** `REGISTRY.json` (SHA-256: `cb1e7ea061dd9a0b37788c833d3ee88247828d20a9e34d605ab18ed08c913cd2`)
- **Detached Genesis PGP Signature:** `REGISTRY.json.asc`
- **Repository Manifest & Detached Owner Signatures:** `SHA256SUMS` (`SHA256SUMS.sig`), `REGISTRY_HASH.txt` (`REGISTRY_HASH.txt.sig`)

### Verification Commands

```bash
# 1. Verify all SHA-256 checksums in this registry
shasum -a 256 -c SHA256SUMS
shasum -a 256 -c REGISTRY_HASH.txt

# 2. Verify detached OpenSSH Ed25519 signatures signed by the SafeStack Owner
ssh-keygen -Y verify -f release-signing/allowed_signers -I safestack-owner \
  -n file -s SHA256SUMS.sig < SHA256SUMS

ssh-keygen -Y verify -f release-signing/allowed_signers -I safestack-owner \
  -n file -s REGISTRY_HASH.txt.sig < REGISTRY_HASH.txt
```

---

## Owner Cryptographic Signature Attestation (Savininko kriptografinis patvirtinimas)

- **Signer / Savininkas:** SafeStack Organization Owner (`safestack-labs` — Antanas Bistrajus, `<admin@safestack.tech>`)
- **Principal Identity:** `safestack-owner`
- **Public Key:** [`release-signing/safestack-owner-2026-11-05.pub`](release-signing/safestack-owner-2026-11-05.pub)
- **Algorithm:** OpenSSH Ed25519
- **Key Fingerprint:** `SHA256:jpM7K4+8hyAJo9qg4ISDbljuENZzx2UqMHu73+S9q48`
- **Reconciliation & Signing Date:** `2026-11-05`
- **Signed Artifacts:** `SHA256SUMS` (`SHA256SUMS.sig`) and `REGISTRY_HASH.txt` (`REGISTRY_HASH.txt.sig`)

**LT — Savininko patvirtinimas:** Visi šio registro SHA-256 kontrolinių sumų sąrašai (`SHA256SUMS` ir `REGISTRY_HASH.txt`) bei susietų `kibernetinio-saugumo-sprendimai` organizacijos projektų būsenos buvo sutikrinti ir naujai kriptografiškai pasirašyti organizacijos savininko (`safestack-labs` / Antanas Bistrajus, `<admin@safestack.tech>`) OpenSSH Ed25519 parašu (`SHA256:jpM7K4+8hyAJo9qg4ISDbljuENZzx2UqMHu73+S9q48`). Privatus pasirašymo raktas niekada nėra saugomas repozitorijoje.

---

## Registered release-signing keys

### 1. SafeStack Organization Owner Signing Key — active from 2026-11-05

- **Scope:** Ecosystem SHA-256 verification manifests (`safestack-validation-registry`, `Verification-artifacts`)
- **Public key:** [`release-signing/safestack-owner-2026-11-05.pub`](release-signing/safestack-owner-2026-11-05.pub)
- **Allowed signers:** [`release-signing/allowed_signers`](release-signing/allowed_signers) (`safestack-owner`)
- **Algorithm:** SSH Ed25519
- **Fingerprint:** `SHA256:jpM7K4+8hyAJo9qg4ISDbljuENZzx2UqMHu73+S9q48`

### 2. SafeStack Pi 5 VPN — active from 2026-10-14

- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-Pi-5-VPN`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-Pi-5-VPN)
- **Public key:** [`release-signing/safestack-pi5-vpn-2026-10-14.pub`](release-signing/safestack-pi5-vpn-2026-10-14.pub)
- **Algorithm:** SSH Ed25519
- **Fingerprint:** `SHA256:4M3iJl8DNaGgqnDrKPaElv1/Fmsx1G2JRLEaaWgWkHg`
- **First signed commit:** [`82f0897400f9612753c35c201c45f226d29793ed`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-Pi-5-VPN/commit/82f0897400f9612753c35c201c45f226d29793ed)

These SSH Ed25519 signing keys are separate from the root-signed project identity keys in `safestack-project-public-keys`. Private keys are never stored in this registry.

---

## Validated Ecosystem Projects

All project key fingerprints below correspond to the canonical SHA-256 digest of the decoded 32-byte Ed25519 public key in [`safestack-project-public-keys/public-project-keys.json`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys).

### 1. SafeStack NodeOS
- **Repository:** [`kibernetinio-saugumo-sprendimai/node-os`](https://github.com/kibernetinio-saugumo-sprendimai/node-os)
- **Deployment:** Autonomous Zero-Trust edge security layer & NVMe health monitoring for Raspberry Pi 5
- **Compliance Status:** **Fully Validated** (v0.2.0-genesis, Root Canon v1.0.0, Technical Canon v1.0.0)
- **Key Fingerprint:** `a89d861185c7603c0c01722150ee5ea6d61c5da94cabe99973baa41ab9a9c288` (`project-005`)
- **Release Manifest:** `SHA256SUMS` (58 verified files, SHA-256: `91401c8a8057e4118d90a8d2ab79d00ec7eedfd61342921692489565d785c45d`, Ed25519 signed: `SHA256SUMS.sig`)
- **Attestation:** `AUDIT_REPORT.md` (SHA-256: `95e9519c3fad58ec8dbf9e914266d156d28ab81435148c21d676646285f209ec`, Ed25519 signed: `AUDIT_REPORT.md.sig`)

### 2. SafeStack Audit System
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-audit_system`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-audit_system)
- **Role:** Deterministic AI-assisted security audit pipeline and fail-closed runtime governance
- **Compliance Status:** **Fully Validated** (v2.0.0 / `1.0.0-GOLDEN`, 41 unittest + standalone air-gap/chaos regression suites)
- **Key Fingerprint:** `b3b96eddf09a6315e369a1116860a60bb630d0a2fb1e8e3f855279dab90657d6` (`project-001`)
- **Manifest:** `SHA256SUMS` (64 verified files, SHA-256: `23ba3c18a4663fbb042147163b55303c43091b83cef29adada95bba69592183b`)
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
- **Dossier:** `index.html` (SHA-256: `d811e0b7110596644bedc47b5ee13fe47c7058abcc4d6bd1bea2b50f3177e2dd`)

### 5. SafeStack Zero Trust
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust)
- **Role:** Local-first policy decision engine, default deny, and device posture gates
- **Compliance Status:** **Fully Validated** (v0.1.0, 6/6 automated tests OK)
- **Key Fingerprint:** `8c7f6e91f092a482d3b250e97b8d5ea4302bc771b101346f8ba2d4ee460c7259` (`project-014`)
- **Manifest:** `SHA256SUMS` (15 verified files, SHA-256: `6df1bb35640ef907a6fccc16947b8991215f069f3dacb29ac801e49115c00359`)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 6. SafeStack Zero-Trust Platform
- **Repository:** [`kibernetinio-saugumo-sprendimai/SafeStack-Zero-Trust-Platform`](https://github.com/kibernetinio-saugumo-sprendimai/SafeStack-Zero-Trust-Platform)
- **Role:** Zero-trust security platform and decentralized policy orchestration components
- **Compliance Status:** **Fully Validated** (v0.1.1, 54/54 automated tests OK)
- **Key Fingerprint:** `4e98805683fb2ee67bd33b84936d87dea526a9282efe88f7b82155e8aaea2d93` (`project-015`)
- **Manifest:** `SHA256SUMS` (53 verified files, SHA-256: `7ffab85f4d8bfae628adc020f9f7d7182f795695bf755fca4e3150563ada4cbf`)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 7. SafeStack Sentinel
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-Sentinel`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Sentinel)
- **Role:** Continuous node security monitoring and telemetry daemon
- **Compliance Status:** **Fully Validated** (v0.1.0, 38/38 automated tests OK)
- **Key Fingerprint:** `e30339fea80a23031a9d4aa4524eced9294b8e81e120a425d1a7cc085cb43b0d` (`project-010`)
- **Manifest:** `SHA256SUMS` (46 verified files, SHA-256: `1fc5a6c6ba4776acfb43ebb7b1fcc0b53d13fc492cdbaca5cc96e3fcd809b09c`)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 8. SafeStack Suite
- **Repository:** [`kibernetinio-saugumo-sprendimai/Safestack-suite`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-suite)
- **Role:** Integrated runtime utilities and cryptographic CLI tools
- **Compliance Status:** **Fully Validated** (v0.1.0, 15/15 automated tests OK)
- **Key Fingerprint:** `bc30f37a293c706be362e054c95079311664a52b4dc7c796f69fd8c410b62ea4` (`project-011`)
- **Manifest:** `SHA256SUMS` (23 verified files, SHA-256: `1c7415aa482bdbe6dbc66c9a4227d96511ecf5701d685878f21b05442d08ff63`)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 9. SafeStack OSINT
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-OSINT`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-OSINT)
- **Role:** Modular, policy-driven OSINT framework with cryptographic integrity verification
- **Compliance Status:** **Validated** (v1.5.1 code & 9/9 automated tests OK; v1.5.0 `SHA256SUMS` baseline `fb82b34a28b52fc2c166bf4f81438ccd4ece9df3a5440e11892666d1ff761b75` pending refresh for v1.5.1 commit `fdd1834`)
- **Key Fingerprint:** `14b9409112c71047bfd52113fad265cf424cf6a99370d6cc874d7b238a5761e5` (`project-007`)
- **Manifest:** `SHA256SUMS` (65 baseline entries)
- **Attestation:** `AUDIT_REPORT.md` & `AUDIT_REPORT_EN.md`

### 10. SafeStack Project Public Keys
- **Repository:** [`kibernetinio-saugumo-sprendimai/safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
- **Role:** Central root-signed Ed25519 identity key registry and release signing keys
- **Compliance Status:** **Fully Validated** (Schema: `safestack.project-key-registry.v1`, 3/3 automated tests OK)
- **Registry ID:** `3ce517eafe34ae00d0554e5a52a6c2ca`
- **Root Public Key:** `z8oMmyDuGRm4eqNiML6Av2B16GCNMcDOrpZJwaJGsgY=`
- **Registry File SHA-256:** `b22c77ca0e4d26314b3391a3fca8b21d1b5e36b870f264875842cc366d520687` (`public-project-keys.json`)

### 11. Verification Artifacts
- **Repository:** [`kibernetinio-saugumo-sprendimai/Verification-artifacts`](https://github.com/kibernetinio-saugumo-sprendimai/Verification-artifacts)
- **Role:** Detached factual cryptographic checksums, owner-signed `.sha256.sig` manifests, and verification engine for external validation
- **Compliance Status:** **Fully Validated** (Owner-signed manifests verified)
- **Key Fingerprint:** `cf748daff8695375496791d67ca963e0add179e5065cbc50295fcce1b51bd6e4` (`project-018`)
- **Verification Engine:** `verify_ecosystem.py`
