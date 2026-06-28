---
layout: default
title: "Register — MARC 2026"
lang: en
ref: register
permalink: /en/register/
---
<!-- [P3] Register — the conversion page -->

# Register

{% if site.competition_active %}
> Registration is **open** (tentatively Jul 6 – Jul 31, 2026). Dates are subject to change.
{% else %}
> Registration is **not open yet**. {{ site.event.short_name }} opens for
> registration on the public launch date (tentatively **2026-07-06**). This page
> will activate then.
{% endif %}

## Who can enter

A **student team** challenge (workshop track). Team composition and size guidance
will be confirmed at launch — details are **under internal review**.

## How registration works

1. **Submit the registration form** (team name, affiliation, contact, agreement).
2. **Receive your team ID / token** to authenticate your submissions.
3. **Download the starter kit** and begin development.

## Submission model (summary)

- Participant apps are **developed with Docker**; the standard entry point is
  **`docker compose up`**.
- Host your work in your **own private GitHub repository** and add the organizer
  account **`marc-challenge-office`** as a **collaborator**.
- The organizers **clone a frozen tag** of your repo and score submissions
  **sequentially**.

> Full submission details are in the **[developer guide](/en/resources/)**.
> Tokens and other secrets are issued through the process; their **values and
> mechanisms are not published here**.

## Register

{% if site.competition_active %}
<a class="btn btn--primary" href="/apply/">Open the registration form</a>
{% else %}
<p><em>The registration form will appear here when registration opens.</em></p>
{% endif %}

## Questions

See [Organizers](/en/organizers/) for the contact channel.
