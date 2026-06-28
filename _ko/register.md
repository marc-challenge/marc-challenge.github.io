---
layout: default
title: "참가 등록 — MARC 2026"
lang: ko
ref: register
permalink: /ko/register/
---

# 참가 등록

{% if site.competition_active %}
> 등록이 **진행 중**입니다(잠정 2026-07-06 ~ 07-31). 일정은 변경될 수 있습니다.
{% else %}
> 아직 **등록 전**입니다. {{ site.event.short_name }} 등록은 공개일(잠정
> **2026-07-06**)에 시작됩니다. 그 시점에 본 페이지가 활성화됩니다.
{% endif %}

## 참가 자격

**학생 팀** 챌린지(워크숍형)입니다. 팀 구성·규모 안내는 공개 시 확정되며, 현재
**내부 검토 중**입니다.

## 등록 절차

1. **등록 폼 제출**(팀명·소속·연락처·동의).
2. 제출 인증용 **팀 ID / 토큰 발급**.
3. **스타터킷 내려받아** 개발 시작.

## 제출 모델 (요약)

- 참가자 앱은 **Docker 기반 개발**, 표준 진입점은 **`docker compose up`**.
- 자기 **Private GitHub 리포**에 주최 계정 **`marc-challenge-office`** 를
  **collaborator 로 추가**.
- 주최가 **동결 태그를 clone** 하여 **순차 채점**합니다.

> 상세 제출 모델은 **[개발자 가이드](/ko/resources/)** 를 참조하세요. 토큰 등
> 비밀은 절차로만 안내하며 **값·메커니즘은 비공개**입니다.

## 등록하기

{% if site.competition_active %}
<a class="btn btn--primary" href="/apply/">등록 폼 열기</a>
{% else %}
<p><em>등록이 시작되면 이곳에 등록 폼이 표시됩니다.</em></p>
{% endif %}

## 문의

연락 채널은 [Organizers](/ko/organizers/) 를 참조하세요.
