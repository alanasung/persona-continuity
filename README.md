<p align="center">
  <h1 align="center">How Sharply Personas Switch Under Soft Steering</h1>
  <p align="center"><strong>Test whether persona changes are discrete flips or continuous drifts under steering.</strong></p>
</p>

---

## Overview

This repository implements experimental profiles for **How Sharply Personas Switch Under Soft Steering**. Config, caching, hooks, metrics, ablations, reporting, and CI are built for reproducible local pilots on small open-weight models.

Hypothesis (one line): Test whether persona changes are discrete flips or continuous drifts under steering.

## Motivation

Interpretability and safety claims fail in practice for boring engineering
reasons: unpinned weights, chat templates skipped, invalid layer indices,
intervals that span zero treated as nulls, and stages that raise
`NotImplementedError`. This repo treats those as first-class bugs.

## Status

Focus: test whether persona changes are discrete flips or continuous drifts under steering. Shared infrastructure is in place; domain stages
must pass harness validation before any measured claim.

| Command | Purpose |
|---|---|
| `make install-dev` | editable install + pinned requirements |
| `make test` | full unit suite |
| `make ci` | lint + test + typecheck + api-contract + coverage |
| `make pilot` | end-to-end pilot profile |
| `make doctor` | environment / device report |
