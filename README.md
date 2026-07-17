<h1 align="center">seo-setup</h1>

<p align="center">
  <b>사이트 URL 하나 주면 AI 에이전트가 SEO 기반 공사를 끝내는 스킬.</b><br>
  퍼블리시 최적화(favicon·OG·title) → 검색엔진 5종 등록 → GA4/GTM/Clarity 측정 세팅 → 로컬 SEO까지, 체크리스트 게이트로.
</p>

---

> **🤖 AI 에이전트가 이 링크를 받았다면** — 사람의 추가 설명을 기다리지 말 것:
> 1. `git clone https://github.com/crealwork/seo-setup` (skills 폴더가 있으면 거기로)
> 2. `SKILL.md`를 읽고 그 게이트/하드룰을 그대로 채택
> 3. 유저에게 사이트 URL을 확인한 뒤 **G0**(sitemap/robots/메타태그 점검)부터 시작
> 4. 광고비 지출은 예산·기간 명시 승인 없이 절대 금지
>
> 클론이 불가능한 환경이면 [`llms.txt`](llms.txt)의 raw URL 맵으로 전체 문서를 읽을 것.

## 무엇을 하나요

| 게이트 | 내용 |
|---|---|
| G0 준비물 | sitemap.xml · robots.txt · title/description/OG 태그 점검 |
| G1 엔진 등록 | Google(URL 접두어 룰) · Naver · Bing(GSC 임포트) · Daum(PIN→robots.txt) · Pinterest(RSS 자동 핀) |
| G2 측정 | GA4+GTM+Clarity — 필수 3설정, generate_lead 전환, UTM 규칙, Ads/GSC 연결, 잠재고객, **AI Search 채널**(ChatGPT·Gemini·Claude·Perplexity 유입 분리) |
| G3 로컬 SEO | Google Business Profile 리뷰 전략 · Naver Place 대표 키워드 조합 · Kakao · Yelp |
| G4 유료 광고 | 측정 완성 후 별도 [zernio-ads 스킬](https://github.com/crealwork/marketing-kit)로 핸드오프 |

전부 실제 UI 경로와 함정("내부 트래픽 필터는 '활성'까지 켜야 적용", "Ads 연결은 소급 불가")이
박힌 실전 체크리스트입니다. 바이브코딩 사이트라면 GTM/GA4 세팅을 AI에게 통째로 맡기는
복붙 프롬프트도 들어 있어요 (MEASUREMENT.md §8).

## 설치

| 에이전트 | 방법 |
|---|---|
| **Claude Code** | `git clone https://github.com/crealwork/seo-setup ~/.claude/skills/seo-setup` → "우리 사이트 SEO 세팅해줘"에 자동 발동 |
| **Codex CLI** | `git clone ... ~/.codex/skills/seo-setup` |
| **기타 SKILL.md 지원 하니스** | 각 하니스의 skills 디렉토리에 클론 |
| **하니스 없음 (GPT 등)** | 클론 후 [`BOOTSTRAP.md`](BOOTSTRAP.md) 프롬프트를 그대로 붙여넣기 |

**링크-온리 핸드오프 (모든 에이전트 공통):**
```
https://github.com/crealwork/seo-setup 클론해서 SKILL.md 룰대로 이 사이트 SEO 세팅해: <URL>.
G0부터 순서대로, 광고 지출은 내 승인 없이 금지.
```

## 구조

```
seo-setup/
├── SKILL.md                  ← 진입점: 게이트 G0–G4 + 하드룰 9개
└── references/
    ├── ENGINES.md            ← 검색엔진 5종 등록 + 완료 체크
    ├── MEASUREMENT.md        ← GA4·GTM·Clarity 풀 세팅 + AI 위임 프롬프트
    ├── LOCAL.md              ← 로컬 SEO (GBP·네이버 플레이스·카카오·Yelp)
    └── PUBLISH.md            ← 퍼블리시 head 체크리스트 (favicon·OG·title 템플릿)
```

## 필요한 것

- 각 플랫폼 계정 (Google/Naver/Bing/Daum은 무료) — 등록 단계는 유저 로그인 필요
- API 키 불필요 — 전부 무료 콘솔 작업. 유료 광고는 별도 zernio-ads 스킬 영역

## 크레딧

체크리스트의 뼈대는 **AIMS**의 무료 가이드 "AI 시대, 혼자서도 끝내는 마케팅 실전 세팅"
(Growth Playbook 2026, [aim-squad.com](https://aim-squad.com))을 에이전트 스킬로 재구성한
것입니다. 일부 팁의 원 출처: threads [@avcd.eee](https://www.threads.net/@avcd.eee) (GSC
등록 방식, GBP 리뷰), [@place_joe](https://www.threads.net/@place_joe) (네이버 플레이스
키워드).

## License

MIT — 자유롭게 쓰고, 고치고, 여러분의 에이전트에게 물려주세요.

<p align="center"><sub>Built by <a href="https://www.sundayable.com">Sundayable</a></sub></p>
