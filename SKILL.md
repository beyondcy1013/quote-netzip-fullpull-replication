---
name: quote-netzip-fullpull-replication
description: Govern the authenticated official 5188 full-push protocol shared by netzip-fullpull and all Rust consumers.
---

# Shared official full-push governance

## Authority

- Resolve the shared implementation from the current consumer's
  `netzip-fullpull` Cargo path dependency. Do not assume a host-absolute path;
  the workspace may be mounted through Samba or SSHFS.
- From that resolved crate, read `docs/STATUS.md`, `PROTOCOL.md`, `EVIDENCE_INDEX.md`,
  `HYPOTHESES.md`, `ACCEPTANCE.md`, and `GITHUB_RELEASE.md` first.
- Protocol facts, decoder gaps, fixtures, and acceptance state belong there.
- Product runtime/API/deployment facts remain in the consuming project.
- Project `progress.MD` files are journals, not protocol authority.

## Consumers

Current direct consumers include `quoteNetzipRs`, `netzip_win` packages
`netzip-driver-hub` and `netzip-service`, `tdxRs/tdx-runtime`,
`netzip-supplement`, and `stock-source-netzip`. Re-enumerate Cargo path
dependencies before every major release.

## Evidence discipline

- Record fact, hypothesis, and verdict separately.
- Scope evidence by account, session, TCP flow, `0104` version, time window,
  producer version, and SHA256.
- Keep frame, error-record, omitted, completed, EOF/clamp, missing-seed,
  accepted, and rejected counts separate.
- Dynamic parity requires market/code and exact business second/state group.
- A connection, all-clean replay, internal commit, or successful build does not
  independently prove business correctness.
- Never change token/mask semantics from OEM hit rate alone.

## Current boundary

- NativeWineClamp is `mechanism-pass / business-fail` and explicit opt-in.
- Strict remains the default decoder; `publication=disabled` remains.
- A default-off, bounded, nonblocking, authenticated, noncanonical shadow may
  be deployed through webClx, but must not feed canonical quotes.

## Workflow

1. Claim one-writer ownership for shared source and authority documents.
2. Reproduce narrowly, then replay all required fixtures.
3. Update shared status, protocol, evidence, or hypothesis documents.
4. Run every direct consumer in the shared acceptance matrix through webClx.
5. For a major algorithm breakthrough follow `docs/GITHUB_RELEASE.md`: inspect
   repository boundaries, commit shared code/docs, update consumers, push each
   authoritative repository, and verify remote commit IDs.
6. Never claim all crates reached GitHub when only `quoteNetzipRs` was pushed;
   the enclosing shared-crate worktree currently has no configured remote.

## Ownership

- `netzip-fullpull`: auth protocol, 5188 transport/init/tables/2704/state.
- `quoteNetzipRs`: Linux runtime, shadow/API, publication and rollback.
- `netzip_win`: Windows driver/GUI/service, target build and deployment.
- 7709/K-line/F10 belongs to supplementation, not official full-push.

Use `webclx-compile-and-deploy` for Rust checks and deployment. Preserve
unrelated dirty work. Credentials remain runtime-only and never enter evidence,
messages, docs, commits, or fixtures.
