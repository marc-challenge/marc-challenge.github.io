---
layout: default
title: "Challenge — MARC 2026"
lang: en
ref: challenge
permalink: /en/challenge/
---

# The Challenge

A **citizen-safety robotics** concept: a robot patrols a virtual campus to
**find lost belongings** and **recognize people in distress or unusual situations
(SAR)** — a two-stage mission joining perception, navigation, and manipulation.

> This challenge structure is a draft under internal review; details may change before launch.

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

## What makes it technically distinctive

| Theme | What it means |
|---|---|
| **Relational VLA** | Ground language to objects *and* their relations in a scene, not just isolated detections. |
| **Multi-view fusion** | Combine fixed **CCTV** views with the robot's **stereo cameras** for robust perception. |
| **Navigation + manipulation** | One continuous mission joins mobile navigation with 6-DoF pick-and-place. |

## How it is evaluated (overview)

- **Automated quantitative scoring** across Stage 1 and Stage 2.
- **Paper review** → selection of finalists.
- **Finals**: on-site presentation + **live demo** → final ranking.

## Learn more

For precise input/output and scoring specifications, see the
**[developer guide](/en/resources/)**.
