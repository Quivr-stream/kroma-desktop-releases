## Quivr architecture maintenance

Canonical system map and maintenance contract: https://github.com/Quivr-stream/quivr-architecture. Read its AGENTS.md and README.md before architecture-affecting work.

When changing communication between products/services, API routes or payloads, HTTP/WebSocket/SSE/gRPC/IRC flows, webhook/subscription behavior, authentication/scopes/permissions, account links, token ownership/storage, databases, deployment boundaries or external platforms:

1. Inspect the affected implementation and consumers, then update Quivr-stream/quivr-architecture in the same task. Cosmetic changes without an architecture impact need no map update.
2. Update the topology/descriptions in build-network.py, detailed directionalFlows and inspected source revisions in architecture.json, and ARCHITECTURE.md / index.template.html where affected. Preserve request/event direction and verified trust boundaries. Do not assume all traffic goes through Quivr API or ChatHub.
3. Run `python build-network.py` and `python check-artifacts.py` in the architecture repo; commit source and generated outputs together. Verify browser interactions when those change.
4. Cross-link source and architecture commits/PRs in the final task report. Follow the user's publication/branch policy. If access or authorization prevents the companion update, explicitly report the exact missing changes; never claim synchronization is complete.

Do not commit credentials, provider tokens, personal data, server inventories or unpublished security findings. Instructions do not grant additional access or permission. Existing project-specific instructions still apply.
