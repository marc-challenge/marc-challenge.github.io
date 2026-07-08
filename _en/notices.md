---
layout: default
title: "Notices — MARC 2026"
lang: en
ref: notices
permalink: /en/notices/
---

# Notices

## 0 · Release schedule {#schedule-notice}

The MARC 2026 website is live and **registration is now open**. You can read the competition overview, challenge, and key dates and [register your team](/en/register/) right now.

**The developer resources (developer guide and starter kit) open on {{ site.open_date }}** ({{ site.open_time_utc }} · {{ site.open_time_kst }}). We will announce it here and in the top banner as soon as they are ready.

Register early to receive your team ID, and you can start building the moment the resources open.

## 1 · Offline judging runtime

The program you develop **may not use commercial APIs** (external AI APIs such as
cloud LLMs). Scoring runs in a **runtime with no external network access**, so no
external API calls or internet access are allowed during execution.

> **Build time *is* online.** Bake model weights and dependencies into your image
> at build time (internet available then). At runtime, **no downloads and no
> external API calls**.

## 2 · Resources provided {#resources}

Everything you need to take part is gathered here. The actual files — the developer
guide, starter kit, and more — **live on GitHub**, and the links
below take you straight to them.

{% unless site.competition_active %}
> The resources below open on **{{ site.open_date }}**. The links in this table activate that day.
{% endunless %}

| Resource | What it is | Link |
|---|---|---|
| **Developer guide** | Environment setup, SDK usage, scoring, and troubleshooting — everything you need to develop. | {% if site.competition_active %}[Open the guide]({{ site.links.dev_guide }}/en/){% else %}<span class="link-pending">Opens {{ site.open_date }}</span>{% endif %} |
| **Starter kit** | One bundle with everything you need to build:<br>· **Practice simulation platform** (Sejong campus digital twin, robot, sensors, ROS 2, sample problems, practice background *chungmu*)<br>· **Dataset generator**<br>· **Manipulation training tool**<br>· **Participant SDK** (`marc-sdk`)<br>· **Demo** (reference implementation)<br>_(See the [Challenge](/en/challenge/) page for details)_ | {% if site.competition_active %}[GitHub]({{ site.links.starter_kit }}){% else %}<span class="link-pending">Opens {{ site.open_date }}</span>{% endif %} |

## 3 · Third-party asset licenses

MARC uses third-party assets, including **open-source software (OSS)** and **USD**
content. Their licenses and sources are acknowledged here.

- **NVIDIA Isaac Sim** — the simulation platform. Under its license we do not redistribute prebuilt images; participants pull the base image under their own account and build locally. Pulling the base image requires an **NVIDIA (NGC) account**.
- **ROS 2 (Humble)** — the standard interface for robot control and sensor communication.
- **Participant SDK (`marc-sdk`)** — MIT license.
- **Background & character USD** — the practice *chungmu* background and public assets (characters replaced with MakeHuman (CC0), etc.).

A consolidated list of licenses and attributions is provided in the starter kit's
`NOTICES.md` and the developer guide. Participants must respect the licenses of all
bundled and downloaded assets.

## 4 · The competition background (playground) may change

The only competition background (playground) released to participants is the practice
**`chungmu`** environment. **The actual competition may run on a different
background.** This keeps teams from overfitting to one specific stage and prevents the
real stage from being exposed in advance — so build your agent to **generalize and
work well in an environment it hasn't seen before.**
