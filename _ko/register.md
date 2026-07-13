---
layout: default
title: "참가 등록 · 일정 — MARC 2026"
lang: ko
ref: register
permalink: /ko/register/
---

# 참가 등록

{% if site.registration_open %}
> 등록이 **진행 중**입니다(2026-07-06 ~ 07-31). 개발자 가이드·스타터킷은
> **{{ site.open_date }}**({{ site.open_time_kst }} · {{ site.open_time_utc }})에 공개됩니다.
{% else %}
> 아직 **등록 전**입니다. {{ site.event.short_name }} 등록은
> **{{ site.open_date }}**({{ site.open_time_kst }} · {{ site.open_time_utc }})에 시작되며, 그 시점에 본 페이지가 활성화됩니다.
{% endif %}

## 참가 자격

**대학생 또는 대학원생**으로 구성된 **5명 이내**의 팀이 참가할 수 있습니다.

팀원을 아직 정하지 못했더라도 먼저 등록하고 개발을 시작할 수 있습니다. 등록한 뒤에도 팀원을 추가하거나 바꿀 수 있으며, **논문 제출 마감일에 제출한 논문의 저자 목록이 팀의 최종 팀원 명단**이 됩니다.

지도교수는 팀원과 별개로 논문 공저자로 올릴 수 있습니다.

다만 팀장은 등록 이후 바뀌지 않는 것을 원칙으로 합니다. 팀 ID 와 인증용 토큰이 팀장 이메일로 발급되기 때문입니다. 팀장을 바꿔야 하는 사정이 생기면 주최 측으로 문의해 주세요.

## 등록 및 제출 절차

1. **{% if site.registration_open %}[등록 폼]({{ site.links.register_form }}){% else %}등록 폼{% endif %} 제출**{% unless site.registration_open %} <em class="reg-note">({{ site.open_date }} 오픈)</em>{% endunless %}
   - 팀명·소속·연락처·참가 동의 등 기본 정보를 입력해 참가를 신청합니다.
   - *신청이 접수되면 주최 측이 **팀 ID 와 인증용 토큰을 팀장 이메일로 발급**합니다.*
   - 발급받은 **팀 ID 와 토큰**은 이후 제출하는 결과물에 **반드시 적용**해야 합니다.
2. **스타터킷 내려받아 개발**
   - **[제공되는 리소스](/ko/notices/#resources)** 에서 스타터킷·SDK·개발자 가이드를 받아 개발을 시작합니다.{% unless site.competition_active %} <em class="reg-note">(개발자 가이드·스타터킷은 {{ site.open_date }} 공개)</em>{% endunless %}
3. **결과물(논문·프로그램) 제출**
   - **논문** — [IEEE MetaCom 제출 안내](https://metacomm.org/2026/submission.php)에 따라 **IEEE 양식**으로 작성하고, **[EasyChair](https://easychair.org/conferences/?conf=metacom2026)** 에서 **"Meta-Sejong AI Robotics Challenge 2026" 트랙**을 선택해 제출합니다.
   - **프로그램** — 팀의 **Private GitHub 리포지토리**에 주최 계정 **`marc-challenge-office`** 를 **collaborator 로 추가**하는 방식으로 제출합니다. 주최가 이를 내려받아 **순차 채점**합니다.

     > **중요** — 프로그램은 반드시 개발자 가이드에 따라 **Docker 이미지로 패키징**하여 **`docker compose up` 으로 실행되는 형태**여야 합니다.

## 주요 일정 {#schedule}

| 시점 | 마일스톤 | 비고 |
|---|---|---|
| **2026-07-06 ~ 07-31** | **참가 등록** | |
| **2026-08-31** | **논문 제출 마감** — EasyChair<br>**프로그램 제출 마감** — GitHub | |
| **~2026-09-18** | **본선 진출팀 발표**(3~4팀) | |
| **2026-10-09** | **논문 최종본(카메라레디) 제출 마감** — EasyChair<br>**프로그램 최종 리비전 제출 마감** — GitHub | 본선 진출팀만 해당 |
| **2026-11-09** | **본선**<sup>1</sup> — IEEE MetaCom 2026, 중국 **시안(Xi'an)** | 발표 + 라이브 데모<sup>2</sup> |

<sup>1</sup> 본선 라이브 데모가 진행될 경우, 오전에 연동 테스트가 진행될 수 있습니다.<br>
<sup>2</sup> 본선 현장 사정으로 라이브 데모가 어려운 경우, 주최 측이 미리 준비한 데모 영상을 재생하는 것으로 대체할 수 있습니다.

## 등록하기

{% if site.registration_open %}<a class="btn btn--primary" href="{{ site.links.register_form }}" target="_blank" rel="noopener">등록 폼 열기</a> <em class="reg-note">등록 마감: <strong>2026-07-31 24:00 (UTC)</strong> · 한국시간 <strong>2026-08-01 09:00</strong></em>{% else %}<span class="btn btn--primary is-disabled">등록 예정 · {{ site.open_date }}</span> <em class="reg-note">{{ site.open_time_kst }} · {{ site.open_time_utc }} 오픈 예정</em>{% endif %}
