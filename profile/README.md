# NXTG.ai

**NXTG.ai builds products that check AI's work before you rely on it.**

## Faultline

Paste an AI draft and Faultline checks its claims and citations against real sources. [Check an AI draft free](https://faultline.nxtg.ai) at faultline.nxtg.ai.

### Faultline for teams (alpha)

Put the same checks inside your pipeline: a fail-on gate for agent output, SARIF results in GitHub, an audit trail, and an EU AI Act risk-tier report.

- CLI: `npm i -g @nxtg/faultline` ([faultline-pro](https://github.com/nxtg-ai/faultline-pro), Apache-2.0). Release stage alpha: verdict accuracy has not yet been measured on a labelled test set.
- GitHub Action: [`nxtg-ai/faultline-action@v1`](https://github.com/nxtg-ai/faultline-action).

```bash
claude -p "..." | faultline guard --fail-on refuted
```

### Faultline Team Rollout

Faultline Team Rollout: in 4 weeks we install Faultline in your stack, wire it into your CI and agent pipelines, set the gates with your team, and hand over a running system with an audit trail. To start, email engage@nxtg.ai.

## Dx3

Dx3: the memory and governance layer we run our own agent fleet on. In use internally; not yet available.

## Also from the lab

- **Forge** ([forge.nxtg.ai](https://forge.nxtg.ai)): governance and coordination for AI coding tools. Alpha.
  - [forge-plugin](https://github.com/nxtg-ai/forge-plugin): MIT.
  - [forge-orchestrator](https://github.com/nxtg-ai/forge-orchestrator) and [forge-ui](https://github.com/nxtg-ai/forge-ui): source-available under FSL-1.1-ALv2; each release converts to Apache-2.0 two years after it ships.
- [The Jev calibration test](https://github.com/nxtg-ai/jev-calibration-eval), pre-registered and run in public on 2026-10-01.
- Everything else lives at [nxtg.ai/labs](https://nxtg.ai/labs).

Asif Waliuddin, founder of NXTG.ai, 23+ years leading global digital transformation programs.
