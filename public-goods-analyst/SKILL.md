---
name: public-goods-analyst
description: An autonomous agent for Ethereum public-goods funding intelligence (Octant, Gitcoin, Optimism RetroPGF). A real tool-calling agent (Claude Opus 4.8) plus a Go CLI — cross-epoch funding history, composite ranking (k-means + scoring), trust-graph forensics (Jaccard, Shannon entropy), mechanism simulation (4 QF variants incl. Trust-Weighted QF), temporal anomaly detection, multi-chain on-chain scanning (11 EVM chains, BNB Chain first), Octant-forum sentiment, OSO + GitHub corroboration, and branded PDF reports. Powered by Claude Opus 4.8 via Hermes with an Anthropic API fallback.
homepage: https://github.com/yeheskieltame/Tessera
user-invocable: true
disable-model-invocation: false
command-dispatch: tool
command-tool: Bash
command-arg-mode: raw
metadata: {"openclaw": {"always": false, "os": ["darwin", "linux"], "requires": {"bins": ["tessera"]}, "primaryEnv": "ANTHROPIC_API_KEY", "skillKey": "public-goods-analyst", "homepage": "https://github.com/yeheskieltame/Tessera", "install": [{"id": "go-build", "kind": "shell", "command": "go build -o tessera ./cmd/tessera/", "os": ["darwin", "linux"]}]}}
---

# Tessera — Public Goods Analyst

An autonomous agent for evaluating Ethereum public-goods projects with evidence, not narrative. It ships as a single Go binary (`tessera`) that is both a CLI and an HTTP/SSE server. The agent (Claude Opus 4.8) runs a tool-calling loop over live data — Octant, on-chain RPCs across 11 EVM chains (BNB Chain first), OSO, GitHub, the Octant forum, and Optimism RetroPGF — and every figure it reports is traced to a real tool call.

**GitHub:** https://github.com/yeheskieltame/Tessera

## When to use this skill

- Evaluating a public-goods project (Octant / Gitcoin / RetroPGF) or proposal
- Analyzing an Octant epoch (funding, allocations, rewards, composite ranking)
- Detecting funding anomalies, whale concentration, or coordination/Sybil patterns
- Comparing quadratic-funding mechanisms
- Building trust profiles from donor behavior
- Scanning an address across EVM chains (balances, txs, contracts, USDC/USDT/DAI)
- Gener