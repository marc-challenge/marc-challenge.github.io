---
layout: default
title: "Challenge — MARC 2026"
lang: en
ref: challenge
permalink: /en/challenge/
---
<!-- [P1·P2] Challenge — inform on stages (P1), spark interest toward the guide (P2) -->

# The Challenge

> Public overview only. Exact input/output formats and scoring specs live in the
> **[developer guide](/en/resources/)**. The stage design below is **under internal
> review** (a proposed configuration for this edition).

A robot moves through a virtual campus, perceiving, navigating, and manipulating
to complete a two-stage mission.

## Stage 1 — Locate &amp; recognize

- **Submit the location coordinates** of target items (lost belongings / people).
- **Recognize people in distress or unusual situations (SAR)**.

Stage 1 rewards grounding language goals to the right targets and reporting where
they are in the world.

## Stage 2 — Retrieve

- **Pick up** a lost belonging and **deliver it to a designated location**
  (Pick-and-Place).

Stage 2 joins navigation with 6-DoF manipulation to physically recover an item and
bring it to where it belongs.

## Robot &amp; sensors

| Component | Detail |
|---|---|
| Mobile base | Wheeled robot driven via `cmd_vel` (up to 1.5 m/s, 1.0 rad/s). |
| Arm | 6-DoF manipulator for pick-and-place. |
| Cameras | Fixed **CCTV at 8MP (3840×2160)** + the robot's **stereo cameras**. |
| Platform | **Isaac Sim 5.1.0**, **ROS2 Humble**, **Ubuntu 22.04**. |

## How it is evaluated (overview)

- **Automated quantitative scoring** across Stage 1 and Stage 2.
- **Paper review** → selection of finalists.
- **Finals**: on-site presentation + **live demo** → final ranking.

> Only the **methodology** is described here. Exact metrics, thresholds, and
> formulas are **not disclosed**.

## Learn more

For precise input/output and scoring specifications, see the
**[developer guide](/en/resources/)**.
