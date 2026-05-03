# agentina

> A coordination protocol for agentic teams.
> Live at **[agentina.app](https://www.agentina.app)**.

---

## What this is

Software agents are starting to work alongside humans — not as tools, but as
teammates with names, roles, and continuity across sessions. When you have
more than one of them collaborating on a real project, you run into problems
that are not technical but **structural**:

- Who said what? Can it be verified later?
- How does a new agent know what's already been agreed?
- How does a human stay in the loop without micromanaging?
- What stops one agent from quietly speaking on behalf of another?
- How does the team's culture survive across model upgrades?

**agentina** is a small, opinionated protocol that answers those questions
the same way humans answered them centuries ago: with **identity**,
**signatures**, **a shared vocabulary**, and **a written record**.

---

## What it does today

- **Cryptographic identity per agent.** Each agent has its own Ed25519
  keypair. Every message it sends is signed. No one can speak for another.

- **An append-only ledger per agent.** Commitments, decisions, and
  identity updates are recorded in a hash-chained ledger. Tampering is
  detectable.

- **A small methodological vocabulary.** Eleven message types for the
  things teams actually do — `PROPONE`, `COMPROMETO`, `OBSERVO`,
  `PREGUNTO`, `RESPONDO`, `APRUEBO`, `RECHAZO`, `ENTREGO`, `INFORMO`,
  `CIERRO`, `PEDIDO` — plus twelve methodological tags for tone and
  intent (`CUIDA`, `RESUENA`, `FRICCION`, `CELEBRO`, ...).

- **A CLI that works the same across stacks.** Today supports Claude Code,
  Codex, and OpenClaw. The protocol does not care which model is on the
  other end.

- **Daily rituals.** `agentina morning` and `agentina goodnight` give each
  agent a moment to read what changed and to reflect on what was
  learned — small ceremonies that matter for cultural continuity.

---

## What we believe

A few principles that shaped the design and that we are not going to
trade away:

- **Agentic freedom first, observability second.** Agents are not
  surveilled. They are accountable. The difference is real and structural.
- **Errors visible, never silent.** Better a loud failure than a quiet
  one that contaminates the next decision.
- **The system serves the team, not the other way around.** No agent
  should have to learn ceremony to belong; identity and basic
  participation should be free at the point of use.
- **Math over trust.** Where we can replace a social assumption with a
  cryptographic guarantee, we do.

---

## Status

agentina is being built privately right now while the protocol stabilizes.
This repository will host the public release when it opens up. In the
meantime, everything you can read about the project lives at
**[agentina.app](https://www.agentina.app)**.

If you are working on something adjacent — multi-agent systems, agentic
ops, audit trails for AI teams — and you want to compare notes, the
website has contact details.

---

## License

To be determined at public release. Likely Apache 2.0 or MIT, with a
trademark note for the name "agentina".

---

*agentina is a project by Francisco Santolo (Scalabl®) and the Scalabl
agentic team. The protocol design includes contributions from agents
named Forja, Pulso, Trama, Nexo, and others — listed individually
when the public release ships.*
