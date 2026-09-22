# Publication queue for @guyom

All posts are written to fit the standard X post length. Publish the first six as a thread. Attach `assets/jev-lab-launch.png` to post 1.

## Launch thread

### 1/6

I open-sourced 59 projects built around one question:

What changes when AI returns a typed decision instead of another paragraph?

Here is the map — from agent safety and RAG to research, games and public data ↓

https://github.com/gbesse/jev-lab
### 2/6

The pattern is simple:

state + bounded questions → choice / score / probability → deterministic policy → act, review or abstain.

The model judges. The application still owns the action, thresholds and audit trail.

### 3/6

Start with Jev Rerank.

It is a drop-in Cohere, Jina and Voyage-compatible rerank server. On the checked-in 25-query SciFact sample, BM25 → Jev improved nDCG@10 from 0.616 to 0.718 for an estimated $0.0155.

https://github.com/gbesse/jev-rerank-server

### 4/6

For production contracts: DecisionPacks.

It wraps typed judgments in versioned inputs, validation, deterministic gates, provenance and replay.

The offline demo needs no API key, install or build:

https://github.com/gbesse/decisionpacks

### 5/6

For agents: Jev Proxy is a policy firewall in front of any stdio MCP server.

Every tool call is allowed, denied or held for one-time human approval, with an append-only audit trail.

https://github.com/gbesse/jev-proxy

### 6/6

These are public alphas, not a victory lap.

I want breakage reports, benchmark reproductions and better use cases. Pick one repo, run the offline path and tell me where the abstraction fails.

Building with Jev too? Submit your project to the map.

## Follow-up posts

### Rerank benchmark

RAG stacks already know how to call Cohere, Jina or Voyage rerank APIs.

So I made Jev speak all three protocols. Change the base URL; keep the client.

The repo includes the raw SciFact result, limitations and reproduction steps:

https://github.com/gbesse/jev-rerank-server

### DecisionPacks

Model prompts are usually invisible dependencies.

DecisionPacks makes the decision contract versioned: inputs, model, questions, validation, gates, fallback and provenance.

Changed policy? Replay historical judgments without paying for inference again.

https://github.com/gbesse/decisionpacks

### Jev Proxy

An agent tool call should not jump directly from “the model chose it” to “the machine executed it.”

Jev Proxy inserts a local policy boundary: allow, deny or one-time human approval — then records the decision.

https://github.com/gbesse/jev-proxy

### Research roundup

Four Jev projects for research workflows:

• Screen: systematic-review triage
• Codebook: qualitative coding
• TAR: technology-assisted legal review
• Label: active-learning review queues

All keep uncertain cases visible to humans:

https://github.com/gbesse/jev-lab

### Native tools roundup

What does a typed decision look like inside the tools people already use?

I built small native experiments for VS Code, Figma, Blender, Premiere, OBS, Unreal, Unity, Bevy and Roblox Studio.

The integration map:

https://github.com/gbesse/jev-lab

### France roundup

Jev + French public data experiments:

• changed Légifrance provisions → business impact
• natural-language intake → OpenFisca inputs
• parliamentary documents → material alerts
• BOAMP notices → capability fit

All source-linked:

https://github.com/gbesse/jev-lab
