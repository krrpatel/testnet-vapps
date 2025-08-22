# vApp Submission: ProofSpace

## Verification
```yaml
github_username: "krrish-patel"
discord_id: "987654321098765432"
timestamp: "2025-08-22"
```

## Developer
- **Name**: Krrish Patel
- **GitHub**: @krrish-patel
- **Discord**: krrish#2025
- **Experience**: 4+ years in full-stack + blockchain. Built DeFi dApps, identity solutions, and AI-powered note/chat apps. Experienced in Rust, Node.js, and smart contract integrations.

## Project

### Name & Category
- **Project**: ProofSpace
- **Category**: identity + infrastructure

### Description
**ProofSpace** is a decentralized verification hub that allows users and dApps to generate, verify, and share zero-knowledge proofs of identity, actions, and data without revealing private details.

- For users: verify credentials (e.g., “I am 18+”, “I paid my bill”, “I voted”) without exposing personal data.  
- For dApps: instantly verify attestations from Soundness Layer (SL) testnet/mainnet to build trustless features.

This tackles the problem of data authenticity & privacy in Web3. Today, apps must either trust centralized providers or expose sensitive info. ProofSpace solves both.

### SL Integration  
ProofSpace will directly use **Soundness Layer** to:
1. **Proof Verification**: Submit ZK proofs to the SL testnet, verified trustlessly by SL validators.
2. **Cross-Chain Attestations**: Use SL as the neutral verification hub that dApps on Sui/EVM chains can query.
3. **Privacy Guarantees**: Build user flows where sensitive inputs never leave the client; only SL-validated proofs are shared.

## Technical

### Architecture
- **Frontend (React)**: Users connect wallets, generate claims, and request verifications.
- **Backend (Rust/Node.js)**: Proof generation with SL SDK, routes data to SL testnet.
- **SL Testnet**: Verification layer for ZK proofs (SP1 Groth16 Verifier on Sui).
- **dApps / Consumers**: External chains & apps can call ProofSpace API or directly read from SL.

**Data Flow**  
User → ProofSpace Frontend → Proof Generator (Backend) → SL Testnet Verifier → On-chain Attestation → Queried by dApps.

### Stack
- **Frontend**: React + Tailwind
- **Backend**: Rust (Actix) + Node.js microservices
- **Blockchain**: Soundness Layer (SL) + Sui
- **Storage**: WALRUS for proof blobs, IPFS for metadata, PostgreSQL for app state

### Features
1. **Proof Generator** – Generate ZK proofs of claims on the client.
2. **SL Attestation** – Submit proofs to SL testnet, verified trustlessly.
3. **Cross-chain Access** – Other chains/dApps can query verified proofs.
4. **User Dashboard** – Manage proofs (e.g., active, expired, shared).
5. **Privacy-Preserving Sharing** – Share proof links without leaking underlying data.

## Timeline

### PoC (2-4 weeks)
- [ ] Basic functionality
- [ ] SL integration
- [ ] Simple UI

### MVP (4-8 weeks)
- [ ] Full features
- [ ] Production ready
- [ ] User testing

## Innovation
- **First universal proof hub on SL** – makes Soundness Layer usable for identity, DeFi, and social.  
- **User-owned verification** – credentials stay private; only proofs move.  
- **Cross-ecosystem interoperability** – any dApp can plug in for trustless verification.  

This combines **privacy + usability + interoperability**, aligned with Soundness Labs’ vision of a transparent, manipulation-resistant internet.

## Contact
- **Preferred**: Discord (krrish#2025)
- Updates: GitHub repo issues + Soundness Labs Discord channel

**Checklist before submitting:**
- [x] All fields completed
- [x] GitHub username matches PR author
- [x] SL integration explained
- [x] Timeline is realistic
