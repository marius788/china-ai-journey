---
layout: page
title: "Agentic 3D Logistics Planner"
permalink: /projects/logistics-3d/
---

*Context: LLM Applications course · status: in progress (started week 3)*

## The vision

Logistics planning is spatial — warehouses, routes, stock levels — but most
planning tools are tables. This project makes planning **visual and
agentic**: a 3D view of the logistics network where AI agents plan
transports and warehouse flows, and you can watch, question and correct
their plans.

## Planned features

- **3D network view** — warehouses, routes and stock levels in one
  interactive scene instead of scattered spreadsheets.
- **Agentic planning** — agents that take a goal ("restock X by Friday"),
  break it into transports, check constraints (capacity, time, cost) and
  propose a plan.
- **Explainable proposals** — every plan step shows its assumptions, so a
  human can approve or adjust before anything is executed.
- **What-if comparisons** — change a constraint, see the plan adapt.

## Tech direction

> **TODO:** fix the stack once decided — e.g. 3D with Three.js /
> react-three-fiber, agent layer with tool-calling LLMs, backend in Python.
> Keep this section honest: only list what is actually used.

## Status

- Week 3: concept, scope and first implementation steps.
- Next: minimal 3D scene + one agent that plans a single transport.

## Why this project

It connects my whole semester: LLM agents from the course, decision-making
under constraints from the business simulation, and hopefully a physical
robotics perspective from Tactile Robotics later on.
