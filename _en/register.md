---
layout: default
title: "Register & Timeline — MARC 2026"
lang: en
ref: register
permalink: /en/register/
---

# Register

{% if site.competition_active %}
> Registration is **open** (Jul 6 – Jul 31, 2026).
{% else %}
> Registration is **not open yet**. {{ site.event.short_name }} opens for
> registration on **2026-07-06**. This page
> will activate then.
{% endif %}

## Who can enter

Open to teams of **up to 5 members** made up of **undergraduate or graduate
students**.

## Registration & submission

1. **Submit the [registration form]({{ site.links.register_form }})**
   - Enter your basic details — team name, affiliation, contact, and consent to participate.
   - *Once your entry is received, the organizers issue a **team ID and authentication token to the team leader's email**.*
   - This **team ID and token must be applied to the work you later submit**.
2. **Download the starter kit and develop**
   - Get the starter kit, SDK, and developer guide from the **[resources section](/en/notices/#resources)** and start building.
3. **Submit your results — paper and program**
   - **Paper** — write it in the **IEEE format** per the [IEEE MetaCom submission guide](https://www.ieee-metacom.org/2026/submission.php), and submit it on **[EasyChair](https://easychair.org/conferences/?conf=metacom2026)** under the **"Meta-Sejong AI Robotics Challenge 2026" track**.
   - **Program** — submit it by adding the organizer account **`marc-challenge-office`** as a **collaborator** on your team's **private GitHub repository**; the organizers pull it and **score submissions sequentially**.

     > **Important** — the program must be **packaged as a Docker image that runs with `docker compose up`**, following the developer guide.

## Key dates {#schedule}

| When | Milestone | Note |
|---|---|---|
| **Jul 6 – Jul 31, 2026** | **Registration** | |
| **Aug 31, 2026** | **Paper submission deadline** — EasyChair<br>**Program submission deadline** — GitHub | |
| **~Sep 18, 2026** | **Finalists announced** (about 3–4 teams) | |
| **Oct 9, 2026** | **Camera-ready paper submission deadline** — EasyChair<br>**Final program revision deadline** — GitHub | Finalist teams only |
| **Nov 9, 2026** | **Finals**<sup>1</sup> — IEEE MetaCom 2026, **Xi'an, China** | Presentation + live demo<sup>2</sup> |

<sup>1</sup> If the live demo takes place, a connectivity test may be held in the morning.<br>
<sup>2</sup> If a live demo is not possible due to on-site circumstances at the finals, the organizers may replace it with a pre-recorded demo video prepared in advance.

## Register

<a class="btn btn--primary" href="{{ site.links.register_form }}" target="_blank" rel="noopener">Open the registration form</a>{% unless site.competition_active %} <em class="reg-note">Registration closes at <strong>24:00 (UTC) on 2026-07-31</strong>.</em>{% endunless %}
