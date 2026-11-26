# SnapPwd

SnapPwd shares passwords, API keys, `.env` files and other secrets through one-time links. The secret is encrypted in your browser with AES-256-GCM before upload. The decryption key sits in the URL fragment, which browsers do not send to the server. The stored ciphertext is deleted after the first successful read or when the link expires.

**[snappwd.io](https://www.snappwd.io)** · [Docs](https://www.snappwd.io/docs) · [Security model](https://www.snappwd.io/docs/security) · [Self-hosting](https://www.snappwd.io/docs/self-hosting)

## Repositories

| Repository | What it is |
| --- | --- |
| [snappwd-service](https://github.com/SnapPwd/snappwd-service) | Backend API, written in Rust (Axum) with Redis storage |
| [snappwd-web](https://github.com/SnapPwd/snappwd-web) | Self-hosted web client |
| [snappwd-cli](https://github.com/SnapPwd/snappwd-cli) | Command-line client: `npm install -g @snappwd/cli` |
| [snappwd-skill](https://github.com/SnapPwd/snappwd-skill) | Agent skill for handing secrets to and from AI agents |

All four are MIT licensed.

## What a one-time link does not do

A link that expires does not revoke the credential it carried, and it cannot erase a copy the recipient saved. Rotate a key at its provider if you think it leaked. The [security model](https://www.snappwd.io/docs/security) lists the limits in full.

## Contact

Questions and security reports: [support@snappwd.io](mailto:support@snappwd.io)
