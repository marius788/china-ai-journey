---
layout: page
title: "Cesim Decision-Support Agent"
permalink: /projects/cesim-agent/
---

*Context: Summer School Unternehmensplanspiel (Business Simulation) · SZTU semester abroad*

## The problem

A company simulation produces **more round data than a team can digest
between rounds**: financial statements, market shares, cost breakdowns,
competitor moves. Under time pressure, teams either decide by gut feeling or
drown in spreadsheets.

## The idea

A small agent that splits the work the way it should be split:

- **Python computes** — every number in a recommendation comes from a
  function with a test, never from the model's imagination. Financial ratios,
  production quantities, tariff and transfer-price effects: calculated,
  reproducible, sourced from the simulation's decision guide.
- **The LLM judges and explains** — it interprets the computed results,
  weighs options and writes recommendations the team can actually read.

## How it's built

- Runs on the **Pi agent harness**, which gives the model file access,
  shell commands and a reviewable working loop.
- A Python package with one module per concern: decision schema and
  validation, finance KPIs (incl. shareholder return), production planning
  under asymmetric over/under-production costs, transfer pricing against tax
  *and* tariffs, a demand model, and calibration of model parameters from
  observed round data.
- New analysis logic only lands with a test — the calibration round-trip is
  the acceptance test.

## What it does for the team

- Reads round results and flags what actually changed
- Compares decision options with computed KPIs instead of opinions
- Makes tariff, tax and production trade-offs explicit before the team votes

## What I learned

- Where LLM agents genuinely help (interpretation, explanation, workflow)
  and where they must not be trusted (arithmetic, invented numbers).
- That a strict **"compute first, then talk"** architecture makes agent
  output reviewable — crucial when decisions have consequences.
- How much business simulations teach about prioritization: analysis is
  only valuable if it arrives before the deadline.

> **TODO:** link the code repository once it's public, and add one concrete
> example (e.g. "before round X we changed Y because the agent showed Z").
