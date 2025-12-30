Hash DID

Hash DID is a decentralized identity backend built for normal people.

It provides identity ownership without passwords, centralized databases, or mandatory blockchain usage.

Hash DID is offline first, privacy focused, and lightweight.

---

Why Hash DID Exists

Most decentralized identity systems:

• are too complex
• assume stable internet
• assume crypto knowledge
• ignore real users

Hash DID flips this.

It focuses on:

• simplicity
• offline usage
• human-friendly flows
• backend reliability

---

Hash-DID/
│
├── app/
│   ├── main.py
│   │
│   ├── core/
│   │   ├── config.py
│   │   ├── security.py
│   │   ├── crypto.py
│   │   ├── constants.py
│   │   └── exceptions.py
│   │
│   ├── did/
│   │   ├── models.py
│   │   ├── service.py
│   │   ├── resolver.py
│   │   └── utils.py
│   │
│   ├── wallet/
│   │   ├── storage.py
│   │   ├── encryption.py
│   │   └── backup.py
│   │
│   ├── credentials/
│   │   ├── models.py
│   │   ├── issuer.py
│   │   ├── verifier.py
│   │   └── storage.py
│   │
│   ├── qr/
│   │   ├── generator.py
│   │   ├── scanner.py
│   │   └── schemas.py
│   │
│   ├── zk/
│   │   ├── proofs.py
│   │   ├── verifier.py
│   │   └── challenges.py
│   │
│   ├── api/
│   │   ├── v1/
│   │   │   ├── did.py
│   │   │   ├── wallet.py
│   │   │   ├── credentials.py
│   │   │   ├── auth.py
│   │   │   └── health.py
│   │   │
│   │   └── router.py
│   │
│   ├── db/
│   │   ├── session.py
│   │   ├── base.py
│   │   └── migrations/
│   │
│   └── utils/
│       ├── encoding.py
│       ├── time.py
│       └── validators.py
│
├── tests/
│   ├── test_did.py
│   ├── test_wallet.py
│   ├── test_credentials.py
│   ├── test_qr.py
│   └── test_zk.py
│
├── scripts/
│   ├── init_wallet.py
│   └── generate_did.py
│
├── .env.example
├── .gitignore
├── pyproject.toml
├── requirements.txt
├── README.md
└── LICENSE

---

Core Capabilities

1. Decentralized Identifiers (DID)

• Create and manage DIDs locally
• No central registry
• No blockchain dependency

DID format

did:hash:<public-key-hash>

DID Document

{
  "id": "did:hash:abc123",
  "publicKey": [],
  "authentication": [],
  "service": []
}

2. Encrypted Identity Wallet

• Stores private keys securely
• Password-derived encryption
• Local-only by default
• Portable via encrypted backup

3. Verifiable Credentials (VC)

• Issue credentials
• Store credentials
• Verify credentials cryptographically
• No online verification required

4. QR-Based Identity Sharing

• Share DID via QR
• Login without passwords
• Sign challenges securely
• Simple scan → approve → done

5. Zero-Knowledge Login

• Prove DID ownership
• No private key exposure
• No personal data leakage
• Based on lightweight cryptographic proofs

---

Architecture Overview

Client (Front-end)
        |
        v
Encrypted Local Wallet
        |
        v
Hash DID Core
        |
        ├── DID Manager
        ├── Wallet Engine
        ├── Credential Engine
        ├── QR Services
        └── ZK Proof Engine

---

Tech Stack:

• Python 3.11+
• FastAPI
• SQLite
• Ed25519 cryptography
• AES-256-GCM
• QR utilities
• Pytest

---

Offline First Design

Hash DID:

• works without internet
• stores everything locally
• only syncs when user wants
• never forces blockchain usage

---

API First Backend

Hash DID exposes clean APIs for:

• DID creation
• wallet access
• credential issuing
• QR login
• proof verification

Frontends are plug and play.

---

Security Principles

• Private keys never leave the wallet
• Encryption at rest
• No centralized identity store
• Minimal metadata exposure

---

Roadmap

• Blockchain anchoring
• Selective disclosure credentials
• Advanced zero-knowledge proofs
• Peer-to-peer DID resolution
• Multi-device sync

---

Contributing

Contributions are welcome.

• Fork the repo
• Create a feature branch
• Add tests
• Open a pull request

---

License

MIT License

---

Vision

Identity should belong to people, not platforms.

Hash DID is a foundation for digital identity systems that respect users and real world conditions.
