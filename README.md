# EGETO Founder Command Center

Public GitHub Pages shell for the EGETO Founder Command Center.

## Dashboard

The shell presents sanitized executive information for the Founder, including:
- MVP and current-phase evidence progress;
- milestone runway;
- lane-by-lane G1 / G2 / G3 / G4 / Joint Ops summaries;
- Done / Now / Next;
- incident state;
- Founder Action gate queue;
- bounded Founder command controls.

## Public URL

`https://egeto-vn.github.io/egeto-status/`

GitHub Pages deploys from GitHub Actions via `.github/workflows/pages.yml`.

## Access model

The **static shell is publicly hosted**, but protected operational dashboard data is not anonymously readable.

Before a valid Founder session:
- the UI shows the PIN gate;
- protected status is not loaded;
- Founder commands are unavailable.

After successful server-side PIN verification:
- the shell loads only sanitized allowlisted executive metadata from the Supabase `founder-control` backend;
- a short-lived Founder session enables bounded audited commands;
- the PIN, PIN hash, service role credentials and private repository evidence are never stored in this public repository.

## Source of truth

This repository is only a public presentation shell.

Canonical project truth remains the private repository `EGETO-VN/EGETO` on `main`. Protected dashboard state is a runtime projection and must be synchronized from that canonical source.

## Privacy

This public repository contains static dashboard assets only. EGETO source code, raw Control Tower evidence, security findings, technical identifiers, secrets, real PII and customer data remain private.
