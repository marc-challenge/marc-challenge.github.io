---
layout: default
title: "MARC 2026 — MetaSejong AI Robot Challenge"
lang: ko
ref: home
permalink: /ko/
---

<section class="hero">
  <p class="hero__eyebrow">2회차 · IEEE MetaCom 2026 연계</p>
  <h1 class="hero__title">MARC 2026</h1>
  <p class="hero__subtitle">MetaSejong AI Robot Challenge</p>

  <p class="hero__catch">
    로봇이 <em>보고, 이해하고, 행동하도록</em> 가르쳐 보세요. 고품질 시뮬레이션에서
    펼쳐지는 캠퍼스 규모의 Vision-Language-Action 챌린지.
  </p>

  <div class="hero__cta">
    {% if site.registration_open %}
    <a class="btn btn--primary" href="{{ site.links.register_form }}" target="_blank" rel="noopener">참가 등록</a>
    {% else %}
    <a class="btn btn--primary" href="/ko/register/">등록 예정 · {{ site.open_date }}</a>
    {% endif %}
    <a class="btn btn--ghost" href="/ko/notices/#resources">개발자 가이드 · 스타터킷</a>
  </div>

  {% include hero-media.html slot="intro" lang="ko" %}
</section>

## MARC 2026 이란

**MARC** 는 **MetaSejong AI Robot Challenge**(메타세종 AI 로봇 챌린지)의 줄임말입니다.
학생 팀이 참가하는 로봇 시뮬레이션 대회로, 국제 학술대회 **[IEEE MetaCom 2026]({{ site.links.metacom }})**
과 연계해 열립니다. 2025년에 처음 열렸고, MARC 2026 은 그 **두 번째 대회**입니다.

대회는 **세종대학교 캠퍼스를 그대로 옮긴 가상 환경(디지털 트윈)** 에서 진행됩니다. 참가
팀은 사람의 자연어 명령과 캠퍼스 CCTV 영상을 입력받아 대상을 찾고, 로봇으로 이동·회수하는
**AI 에이전트**를 개발합니다.

MARC 는 앞으로 **매년 열리는 대회**로 자리잡는 것을 목표로 합니다. 1회차(2025)가 캠퍼스
쓰레기 분리수거(재활용) 미션이었다면, 2026년에는 사람의 말을 이해해 행동으로 옮기는
**Vision-Language-Action(VLA) 그라운딩**으로 과제를 확장했습니다.

## 무엇을 겨루나

여러분이 개발하는 것은 **가상의 캠퍼스 환경에서 사람의 말을 이해하고, CCTV 영상을
분석하며, 로봇을 제어하는 AI 에이전트**입니다. 로봇과 CCTV, 캠퍼스는 모두 시뮬레이션으로
제공되며, 여러분은 그 안에서 동작하는 '두뇌'(에이전트)를 만듭니다.

사용자의 명령은 두 가지입니다. 하나는 그 물건이 **어디에 있는지 찾아서 알려 달라("찾아줘")**
는 것이고, 다른 하나는 그 물건을 **직접 가져다 달라("가져다줘")** 는 것입니다.

물건을 찾는 일은 캠퍼스 곳곳에 설치된 **고정 CCTV 영상**으로 이뤄집니다. 에이전트는 이
영상을 분석해 물건이 어디에 있는지 알아내고, 같은 영상에서 **위급하거나 이상한 상황에
처한 사람도 함께 알아챕니다(SAR)**. 그리고 사용자가 물건을 가져다 달라고 하면, 에이전트가
**로봇을 제어**해 그 위치로 이동시켜 물건을 집고 지정된 장소로 옮깁니다.

에이전트가 해내야 할 일을 정리하면 다음과 같습니다.

- **사람의 말 이해하기** — 사용자의 자연어 명령을 해석해, 에이전트가 어떤 **행동(action)** 을 취해야 하는지 파악합니다.
- **CCTV 영상으로 인지하기** — 고정 CCTV 영상을 분석해 물건이 어디에 있는지 찾아내고, 위급·이상상황에 처한 사람(SAR)도 함께 알아챕니다.
- **로봇 제어로 회수하기** — "가져다줘" 명령일 때, 에이전트가 로봇을 제어해 물건을 집어 지정된 장소로 옮깁니다.

## 참가 의의

- 우수 팀은 **IEEE Xplore 게재** 기회를 갖는 **논문 트랙**에 참여합니다.
- 중국 **시안(Xi'an)** 에서 열리는 **국제 본선**(IEEE MetaCom 2026 연계)에 진출합니다.

## 주요 일정

| 시점 | 내용 |
|---|---|
| **2026-07-06** | 홈페이지 공개 및 참가 등록 시작 |
| **{{ site.open_date }}** | 플랫폼·개발자 가이드·스타터킷 공개 |
| **2026-08-31** | 코드·논문 제출 마감 |
| **~2026-09-18** | 본선 진출팀 발표 |
| **2026-11-09** | 본선 — 중국 시안(Xi'an), IEEE MetaCom 2026 |

> 전체 일정과 등록 안내는 [참가 등록](/ko/register/#schedule) 페이지에서 확인하세요.

## 주최 · 연계

### 조직위원회

| 역할 | 이름 | 소속 |
|---|---|---|
| Program Chair | 김재호 교수 | 세종대학교, 대한민국 |
| Co-Chair | 송재승 교수 | 세종대학교, 대한민국 |
| Co-Chair | Li Bai 교수 | Temple University, 미국 |
| Technical Chair | 김태현 교수 | 세종대학교, 대한민국 |

### Hosted by (주최)

**[IEEE MetaCom 2026]({{ site.links.metacom }})** — MARC 의 host conference.

### Organized by (주관)

<div class="org-logos">
  <a href="https://www.iotcoss.ac.kr/" target="_blank" rel="noopener" title="IoT Convergence &amp; Open Sharing System"><img src="{{ '/assets/images/iotcoss-logo.png' | relative_url }}" alt="IoT Convergence &amp; Open Sharing System"></a>
  <a href="https://meta.sejong.ac.kr/" target="_blank" rel="noopener" title="Research Center for Autotwin Technology"><img src="{{ '/assets/images/sponsor-itrc-rcatt.png' | relative_url }}" alt="Research Center for Autotwin Technology"></a>
  <a href="http://sejong.ac.kr/" target="_blank" rel="noopener" title="Sejong University"><img src="{{ '/assets/images/sponsor-sejonguniv.png' | relative_url }}" alt="Sejong University"></a>
  <a href="https://www.temple.edu/" target="_blank" rel="noopener" title="Temple University"><img src="{{ '/assets/images/temple-logo.png' | relative_url }}" alt="Temple University"></a>
</div>

## 문의 {#contact}

문의는 아래 채널을 이용하세요.

- 이메일: **{{ site.event.contact_email }}**
- 채점용 제출 collaborator 계정: **`marc-challenge-office`**
  (참가자 Private 리포에 collaborator 로 추가 — [참가 등록](/ko/register/) 참조).
