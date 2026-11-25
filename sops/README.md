# sops/

Standard operating procedures - step-by-step, repeatable runbooks. Part of the **shared layer**, available
to every client.

**Current SOPs:**
- `instantly-api.md` - how the OS calls each client's Instantly workspace directly via the v2 API: the
  `.claude/bin/instantly.sh` wrapper, per-client keys, and the read/write gating map. **Every skill that
  pulls Instantly data depends on this.**

**Add your own.** This folder is a staging area for your team's runbooks: a daily structure, a client
escalation path, a handover procedure, a churn-save policy, a domain-warmup checklist. Drop each one in as
its own file, reference it by path, and list it in `INDEX.md`. Claude auto-discovers whatever is here, and
context assembly treats `sops/` as "load whichever SOPs exist."

Other operational method lives in the relevant `wiki/` pages (e.g. `wiki/deliverability.md`,
`wiki/email-benchmarks.md`) and the skills themselves.

**Rule:** nothing in this folder may contain a specific client's private data. SOPs are universal.

See root `CLAUDE.md` → *Shared Brain* for how this fits the OS.
