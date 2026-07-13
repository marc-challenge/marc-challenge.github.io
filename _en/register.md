---
layout: default
title: "Register & Timeline — MARC 2026"
lang: en
ref: register
permalink: /en/register/
---

# Register

{% if site.registration_open %}
> Registration is **open** (Jul 6 – Jul 31, 2026). The developer guide and starter kit
> open on **{{ site.open_date }}** ({{ site.open_time_utc }} · {{ site.open_time_kst }}).
{% else %}
> Registration is **not open yet**. {{ site.event.short_name }} opens for
> registration on **{{ site.open_date }}** ({{ site.open_time_utc }} · {{ site.open_time_kst }}),
> and this page will activate then.
{% endif %}

## Who can enter

Open to teams of **up to 5 members** made up of **undergraduate or graduate
students**.

You can register and start developing even if you have not decided on your
teammates yet. Members may be added or changed after you register, and **the
author list on the paper you submit by the paper submission deadline becomes your
team's final roster**.

Your advisor may be listed as a co-author on the paper, in addition to the team
members.

The team leader, however, is expected to stay the same after registration, since
the team ID and authentication token are issued to the leader's email. If you need
to change the leader, please contact the organizers.

## Registration & submission

1. **Submit the {% if site.registration_open %}[registration form]({{ site.links.register_form }}){% else %}registration form{% endif %}**{% unless site.registration_open %} <em class="reg-note">(opens {{ site.open_date }})</em>{% endunless %}
   - Enter your basic details — team name, affiliation, contact, and consent to participate.
   - *Once your entry is received, the organizers issue a **team ID and authentication token to the team leader's email**.*
   - This **team ID and token must be applied to the work you later submit**.
2. **Download the starter kit and develop**
   - Get the starter kit, SDK, and developer guide from the **[resources section](/en/notices/#resources)** and start building.{% unless site.competition_active %} <em class="reg-note">(the developer guide &amp; starter kit open {{ site.open_date }})</em>{% endunless %}
3. **Submit your results — paper and program**
   - **Paper** — write it in the **IEEE format** per the [IEEE MetaCom submission guide](https://metacomm.org/2026/submission.php), and submit it on **[EasyChair](https://easychair.org/conferences/?conf=metacom2026)** under the **"Meta-Sejong AI Robotics Challenge 2026" track**.
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

{% if site.registration_open %}<a class="btn btn--primary" href="{{ site.links.register_form }}" target="_blank" rel="noopener">Open the registration form</a> <em class="reg-note">Registration closes at <strong>24:00 (UTC) on 2026-07-31</strong>.</em>{% else %}<span class="btn btn--primary is-disabled">Registration opens {{ site.open_date }}</span> <em class="reg-note">Opens {{ site.open_time_utc }} · {{ site.open_time_kst }}</em>{% endif %}
