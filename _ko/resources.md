---
layout: default
title: "리소스 — MARC 2026"
lang: ko
ref: resources
permalink: /ko/resources/
---

# 리소스

필요한 모든 것의 단일 진입점입니다. 실제 파일은 GitHub / Read the Docs 에 있습니다.

{% unless site.competition_active %}
> 일부 다운로드는 공개일(잠정 **2026-07-06**)에 해제됩니다. 아래 링크는 미리보기이며
> 그때 갱신될 수 있습니다.
{% endunless %}

| 리소스 | 내용 |
|---|---|
| **개발자 가이드** | Read the Docs(`marc-challenge`) — 환경 셋업·SDK·채점·트러블슈팅. |
| **스타터킷** | GitHub `marc-starter-kit` — SDK wheel·demo·docker 레시피·공개 시나리오. |
| **플랫폼/Trainer 실행** | **Dockerfile-only**(Isaac Sim 라이선스): base 이미지를 직접 받아 **로컬 빌드**. 단일 빌드/실행 명령은 가이드 Quickstart 참조. |
| **Participant SDK** | **`marc-sdk`**(Python wheel, 버전 **2026.1.0**) — 가이드/릴리스 안내대로 설치. |
| **배경 USD** | 연습용 **chungmu** 배경만 공개(별도 번들). 실제 대회 배경은 다를 수 있음. |
| **소개 영상** | 아래 임베드. 영상 준비 전에는 개념 이미지 placeholder 가 대신하며, 준비 후 동일 슬롯에서 교체됩니다. |

## 소개

{% include hero-media.html slot="intro" lang="ko" %}

> **프리빌트 Docker 이미지는 제공하지 않습니다.** Isaac Sim 라이선스에 따라 참가자가
> NVIDIA base 이미지에서 직접 로컬 빌드합니다. 가이드 Quickstart 참조.

## 링크

- 개발자 가이드: **{{ site.links.dev_guide }}**
- 스타터킷: **{{ site.links.starter_kit }}**
- SDK: **`marc-sdk` {{ site.links.sdk_version }}**

> 유의: 심사 런타임은 **인터넷 차단**입니다. 가중치·의존성은 **빌드 시점**(이때는
> 인터넷 사용 가능)에 baking 하세요. **런타임 다운로드·외부 API 호출 금지**.
> ([Notices](/ko/notices/) 참조)
