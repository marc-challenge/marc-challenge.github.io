---
layout: default
title: "Challenge — MARC 2026"
lang: en
ref: challenge
permalink: /en/challenge/
---

# The Challenge

The stage for MARC 2026 is a **digital twin — a virtual copy of the real Sejong
University campus**. There, you build a single **AI agent** that understands what
people say, looks through the campus CCTV video, and drives a robot.

For example, if someone says "find the umbrella I left next to the bench," the agent
understands the request and uses the CCTV video to work out where the umbrella is.
If they say "bring it," the robot then goes there, picks the umbrella up, and moves
it to a designated place.

This page lays out **how that mission is split into the tasks you compete on**
(Stage 1 and 2), together with **what is provided for you, what you have to build
yourself, and what knowledge and skills you'll need** — step by step.

The challenge has **two stages**. **Before you register, you decide** whether to
enter **Stage 1 only** or **both Stage 1 and Stage 2**. If you're not confident about
robot control (navigation and manipulation), you can simply register for **Stage 1
only**. The two stages are as follows.

## Stage 1 — Find it and pinpoint where it is

First the agent works out **what to look for** from the person's words, then
**analyzes the fixed CCTV video** to figure out **where it is** and submits that
position (coordinates). The target may be a lost item or a person who needs help.

In particular, the command often refers to the target not by its appearance but by
its **relationship to nearby objects** — for example, "the **umbrella near the
bench**." To pick the right one among several similar-looking items, the agent must
interpret **relation words** ("beside," "on," "around," "behind") and analyze how
**objects relate to one another** in the scene.

- **Analyze the fixed CCTV video** and **submit the location coordinates** of the
  target (a lost belonging or a person).
- Or, spot **people in distress or unusual situations (SAR)**.

In other words, Stage 1 tests how well the agent **works out which target the
person's words refer to** and, using the CCTV video, finds and reports its location
accurately.

Stage 1 runs over **several rounds**. You submit an answer to the problem given in
each round, and the **average of your per-round scores** becomes your final Stage 1 score.

## Stage 2 — Retrieve it

**Once you finish all the rounds of Stage 1, Stage 2 begins automatically**, and its
problem is a command that asks the robot to **"bring it."** Stage 2 **starts the same
way as Stage 1 — by finding the target through VLA grounding**: the agent understands the
person's words and interprets the relationships between nearby objects to work out
**which item to look for and where**.

Once the target is found, the robot moves to actually **collect** it. It **navigates
on its own** along the campus paths to the target location, and on arrival **uses its
various onboard sensors to compute the item's exact position** before **picking it up
with the arm and placing it in a basket mounted on the robot**.
With the item loaded in the basket, it **drives to the designated place** to deliver
it and finish. This "pick it up and move it" action is called **pick-and-place**.
Planning a collision-free path through tight spaces and picking the item up accurately
and securely are the core challenges here.

- **Find** the target (VLA grounding), then **pick it up** with the arm, **place it
  in the robot's basket**, and **deliver it to the designated place**.

On top of Stage 1's **finding (VLA grounding)**, Stage 2 adds **navigation** (moving
across campus) and **manipulation** — handling the item with a 6-DoF, six-axis arm —
to actually recover the item and bring it back to where it belongs.

## What the organizers provide

You do **not** have to build everything from scratch. Everything you need comes as a
single **starter kit (`marc-starter-kit`)** — you just add the "intelligence" on top.
The starter kit includes:

- **Simulation platform (for practice)** — a tool (`marc.sh`) that runs the **same
  environment used to run and score the competition** on your own machine, so you can
  develop and validate under **the same conditions as the real event**.
  - **Sejong campus digital twin** — a 3D copy of the real campus, built on Isaac Sim.
  - **Robot & sensors** — a four-wheeled mobile robot (with a loading basket), a 6-axis arm, fixed CCTV, and the robot's stereo cameras.
  - **Standard interface** — robot control and sensor input via standard ROS 2 messages.
  - **Sample training problems & public scenario** — practice problems in the same format as the real tasks, plus a practice background (chungmu).
- **Dataset generator** — a tool that **automatically creates the training datasets**
  you need to train recognition models.
  - **Competition objects (assets)** — generate **object-recognition datasets** from the various objects that appear in the competition.
  - **People (SAR)** — generate **people-recognition datasets** to recognize people in distress or unusual situations.
- **Manipulation training tool** — a module for **practicing and training** the
  pick-and-place action of picking an item up and placing it in the basket.
- **Participant SDK (`marc-sdk`)** — a Python library that talks to the platform to
  **receive observations, submit answers, and check your score**.
- **Demo (reference implementation)** — a worked example chaining navigation,
  arm-grasping, and VLA; replace the mock inference with your own implementation
  before submitting.

## What you build

What you create is a single **AI agent (software)** that acts as the robot's
"brain." The agent has to do the following on its own:

- **Understand the command** — make sense of an everyday-language instruction. The
  target is often described by its relationship to nearby objects ("the **umbrella
  beside the bench**"), so you have to work out **what** to look for (which object or
  person), **by which relationship**, and **where** — and whether the request is just
  to locate it ("find it") or to bring it back ("bring it").
- **Perceive from CCTV** — analyze the fixed CCTV video around campus to **work out
  where the target is**. That means choosing **which camera** shows it and telling it
  apart from similar-looking objects, while also spotting **people in distress or
  unusual situations (SAR)** in the same footage.
- **Control the robot** — when told to "bring it," drive the robot **safely to the
  location you found**, and on arrival **pick the item up with the arm, place it in
  the basket**, and carry it to the designated place. This calls for planning a
  collision-free path in tight spaces and grasping the item accurately.

The platform handles the hardware, physics simulation, and communication, so you can
focus purely on the **perception, decision, and control logic**.

> **Important — your agent must run offline.** Both the qualifying (evaluation)
> environment and the finals demo environment have **restricted internet access**.
> This means you **cannot call commercial AI APIs (cloud LLMs, etc.)**; every model
> and file your agent uses must be **bundled into your submission** so it runs without
> internet.

## Knowledge & the technical elements you compete on

These are the skills that are actually **scored** in this challenge. You don't need
to master all of them up front — the starter kit and developer guide give you a
starting point. **Which skills you need depends on how you enter.**

**Stage 1 (finding) — for everyone**

| Technical element | What it does |
|---|---|
| **Vision-language grounding (VLA)** | Links a person's words to the actual target in the scene. |
| **Spatial-relation reasoning** | Interprets relations like "the umbrella beside the bench" to pick the right one among similar objects. |
| **Perception (detection & localization)** | Finds the target in the CCTV video and estimates its position. |

**Stage 1 + 2 (retrieval) — additionally needed if you take on Stage 2**

| Technical element | What it does |
|---|---|
| **Navigation** | Moves along the campus paths to the target without collisions. |
| **Manipulation** | Picks up an item and places it in the basket reliably with the 6-axis arm (grasp pose). |
| **ROS 2 robot control** | Commands the robot's movement and arm actions via standard messages. |

## How it is evaluated (overview)

**Qualifying round**

- The organizers run each team's submission **on the platform** and check its **automatically scored result**.
- The **automatic score and the paper review** together select the teams that **advance to the finals** (pass / fail).
- Teams that advance are granted **eligibility to publish in IEEE Xplore**.

**Finals**

- Finalist teams give an on-site **paper presentation and live demonstration**.
- The two are assessed together to decide the **final ranking**.

> If a live demo is not possible due to on-site circumstances at the finals, the organizers may instead play a **demo video prepared ahead of the finals by running and recording the team's submission**.

## Start building {#start}

Head to the **[resources section](/en/notices/#resources)** for the developer guide, starter kit, and SDK,
and **[register your team](/en/register/)** to receive your team ID and begin. Precise
input/output and scoring specifications are in the {% if site.competition_active %}**[developer guide]({{ site.links.dev_guide }}/en/)**{% else %}**developer guide** (opens {{ site.open_date }}){% endif %}.
