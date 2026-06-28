---
layout: default
title: "Resources — MARC 2026"
lang: en
ref: resources
permalink: /en/resources/
---

# Resources

A single entry point to everything you need. Files live on GitHub / Read the Docs;
this page links to them.

{% unless site.competition_active %}
> Some downloads unlock at public launch (tentatively **2026-07-06**). Links below
> are previews and may be finalized then.
{% endunless %}

| Resource | What it is |
|---|---|
| **Developer guide** | Read the Docs (`marc-challenge`) — environment setup, SDK, scoring, troubleshooting. |
| **Starter kit** | GitHub `marc-starter-kit` — SDK wheel, demo, docker recipes, public scenario. |
| **Platform / Trainer run** | **Dockerfile-only** (Isaac Sim license): you pull the base image and **build locally**. Single build/run command is in the guide Quickstart. |
| **Participant SDK** | **`marc-sdk`** (Python wheel, version **2026.1.0**) — install per the guide / release. |
| **Background USD** | Only the practice **chungmu** background is published (separate bundle). The actual competition background may differ. |
| **Intro video** | Embedded below. While the video is in preparation, a concept image placeholder stands in; the same slot is swapped once ready. |

## Intro

{% include hero-media.html slot="intro" lang="en" %}

> **No prebuilt Docker images are distributed.** Per the Isaac Sim license,
> participants build locally from the NVIDIA base image. See the guide Quickstart.

## Links

- Developer guide: **{{ site.links.dev_guide }}**
- Starter kit: **{{ site.links.starter_kit }}**
- SDK: **`marc-sdk` {{ site.links.sdk_version }}**

> Reminder: the judging runtime is **offline**. Bake weights and dependencies at
> **build time** (internet allowed then); **no runtime downloads or external API
> calls**. See [Notices](/en/notices/).
