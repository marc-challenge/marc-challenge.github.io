---
layout: default
title: "MARC 2026 — MetaSejong AI Robot Challenge"
lang: en
ref: home
permalink: /en/
---

<section class="hero">
  <p class="hero__eyebrow">2nd Edition · In conjunction with IEEE MetaCom 2026</p>
  <h1 class="hero__title">MARC 2026</h1>
  <p class="hero__subtitle">MetaSejong AI Robot Challenge</p>

  <p class="hero__catch">
    Teach a robot to <em>see, understand, and act</em>. A campus-scale
    Vision-Language-Action challenge in high-fidelity simulation.
  </p>

  <div class="hero__cta">
    {% if site.registration_open %}
    <a class="btn btn--primary" href="{{ site.links.register_form }}" target="_blank" rel="noopener">Register your team</a>
    {% else %}
    <a class="btn btn--primary" href="/en/register/">Registration opens {{ site.open_date }}</a>
    {% endif %}
    <a class="btn btn--ghost" href="/en/notices/#resources">Developer guide &amp; starter kit</a>
  </div>

  {% include hero-media.html slot="intro" lang="en" %}
</section>

## What is MARC 2026

**MARC** stands for the **MetaSejong AI Robot Challenge**, a robot-simulation
competition for student teams. It is held in conjunction with
**[IEEE MetaCom 2026]({{ site.links.metacom }})**, an international academic
conference. MARC was first held in 2025, and this is its **second edition**.

The challenge runs on a **digital twin — a virtual copy of the Sejong University
campus**. Teams build an **AI agent** that takes a person's natural-language
command and the campus CCTV video as input, locates the target, and drives a robot
to retrieve it.

MARC aims to become an **annually held** event. Where the 1st edition (2025) was a
campus waste-sorting (recycling) mission, the 2026 edition extends the task to
**Vision-Language-Action (VLA) grounding** — understanding a person's words and
carrying them through to action.

## What you compete on

What you build is an **AI agent that — in a virtual campus environment —
understands what people say, analyzes the CCTV video, and controls the robot**.
The robot, the CCTV, and the campus are all provided in simulation; you build the
"brain" that operates inside it.

A user's command comes in one of two forms: asking the agent to **find where the
item is** and report it, or asking for the item to be **brought to them**.

Finding the item is done through the **fixed CCTV cameras** placed around campus.
The agent analyzes this video to work out where the item is, and in the same
footage it also **spots people in distress or unusual situations (SAR)**. If the
user asks for the item to be brought to them, the agent then **controls the robot**
to drive to that location, pick the item up, and move it to a designated place.

In short, the agent needs to:

- **Understand what a person says** — interpret the user's natural-language command
  to work out what **action** the agent should take.
- **Perceive from CCTV** — analyze the fixed CCTV video to locate the item, and
  also spot people in distress or unusual situations (SAR).
- **Retrieve by controlling the robot** — when the command is "bring it," the agent
  drives the robot to the location, picks the item up, and moves it to a designated place.

## Why take part

- Strong teams join a **paper track** with the opportunity to publish via **IEEE Xplore**.
- Advance to an **international finals** in **Xi'an, China** (in conjunction with IEEE MetaCom 2026).

## Key dates

| When | What |
|---|---|
| **Jul 6, 2026** | Website goes live; registration opens |
| **{{ site.open_date | date: "%b %-d, %Y" }}** | Platform, guide &amp; starter kit release |
| **Aug 31, 2026** | Code &amp; paper submission deadline |
| **~Sep 18, 2026** | Finalists announced |
| **Nov 9, 2026** | Finals — Xi'an, China (IEEE MetaCom 2026) |

> See the full schedule and registration on the [Register](/en/register/#schedule) page.

## Organizers

### Organizing committee

| Role | Name | Affiliation |
|---|---|---|
| Program Chair | Prof. Jaeho Kim | Sejong University, South Korea |
| Co-Chair | Prof. JaeSeung Song | Sejong University, South Korea |
| Co-Chair | Prof. Li Bai | Temple University, USA |
| Technical Chair | Prof. Taehyun Kim | Sejong University, South Korea |

### Hosted by

**[IEEE MetaCom 2026]({{ site.links.metacom }})** — the host conference of MARC.

### Organized by

<div class="org-logos">
  <a href="https://www.iotcoss.ac.kr/" target="_blank" rel="noopener" title="IoT Convergence &amp; Open Sharing System"><img src="{{ '/assets/images/iotcoss-logo.png' | relative_url }}" alt="IoT Convergence &amp; Open Sharing System"></a>
  <a href="https://meta.sejong.ac.kr/" target="_blank" rel="noopener" title="Research Center for Autotwin Technology"><img src="{{ '/assets/images/sponsor-itrc-rcatt.png' | relative_url }}" alt="Research Center for Autotwin Technology"></a>
  <a href="http://sejong.ac.kr/" target="_blank" rel="noopener" title="Sejong University"><img src="{{ '/assets/images/sponsor-sejonguniv.png' | relative_url }}" alt="Sejong University"></a>
  <a href="https://www.temple.edu/" target="_blank" rel="noopener" title="Temple University"><img src="{{ '/assets/images/temple-logo.png' | relative_url }}" alt="Temple University"></a>
</div>

## Contact {#contact}

For inquiries, please use the contact channel below.

- Email: **{{ site.event.contact_email }}**
- Submission collaborator account (for scoring): **`marc-challenge-office`**
  (added as a collaborator to your private repo — see [Register](/en/register/)).
