# NebulaCraft — AI Code Synthesis Studio

NebulaCraft is an AI-native development studio that turns natural language into production-ready code, tests, and deployments. Built on **MiMo-Series**, **Claude-Series**, and **DeepSeek-Series** models.

## Features
- **Synthesis Engine** — multi-step planner that converts intent into typed modules with passing tests across Python, TypeScript, Go, Rust, and Solidity.
- **Memory Graph** — persistent project memory that maps files, decisions, and APIs.
- **Sandboxed Runtime** — every diff is built and tested in an isolated container before it touches your tree.
- **Polyglot APIs** — REST, GraphQL, gRPC, or tRPC scaffolds with auth, rate limits, and OpenAPI docs.
- **Test Synthesis** — property-based + unit + integration tests with coverage reports.
- **1-Click Deploy** — push to Vercel, Fly, Railway, AWS, or Kubernetes.
- **Code Review Agent** — continuous PR review with security checks and architectural drift warnings.
- **Live Telemetry** — plug logs and traces back into the agent for self-healing.
- **Vault Secrets** — per-project encrypted vault.

## Quickstart
```bash
curl -fsSL nebulacraft.dev/install | sh
nebula login
nebula init --model mimo-v2.5-pro
nebula run "Add JWT auth to my Express app"
```

## Models supported
mimo-v2.5-pro, mimo-lite, claude-sonnet-4, claude-opus-4, deepseek-v3, gpt-4-turbo, gemini-pro, doubao, minimax, plus any OpenAI-compatible endpoint.

## Why MiMo
On our internal benchmark of 40 agentic coding tasks, MiMo Pro leads in tool-use accuracy and plan stability. Read the breakdown in `/blog/why-mimo-default`.

## Architecture
```
┌─────────────┐   ┌──────────────┐   ┌──────────────┐
│   Studio    │ → │   Planner    │ → │  Sandbox VM  │
│   (CLI/UI)  │   │  (MiMo Pro)  │   │ (Firecracker)│
└─────────────┘   └──────────────┘   └──────────────┘
                                            │
                                  ┌─────────┴─────────┐
                                  │   Build · Test    │
                                  │   Deploy · Ship   │
                                  └───────────────────┘
```

## Status
- v2.5 in production
- 14k+ active developers
- 2.4M+ code blocks generated
- 97.3% test pass rate

## License
CLI, planner core, sandbox runtime — MIT.

---

Built with NebulaCraft. Powered by MiMo. Part of the **100T Token Initiative**.
