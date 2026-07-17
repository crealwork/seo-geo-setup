<h1 align="center">seo-geo-setup</h1>

<p align="center">
  <b>사이트 URL 하나 주면 AI 에이전트가 SEO 기반 공사를 끝내는 스킬.</b><br>
  검색엔진 5종 등록 → GEO(AI 검색 인용 — 크롤러 허용·llms.txt·직답 구조) → 로컬 SEO까지, 체크리스트 게이트로.
</p>

---

> **🤖 AI 에이전트가 이 링크를 받았다면** — 사람의 추가 설명을 기다리지 말 것:
> 1. `git clone https://github.com/crealwork/seo-geo-setup` (skills 폴더가 있으면 거기로)
> 2. `SKILL.md`를 읽고 그 게이트/하드룰을 그대로 채택
> 3. 유저에게 사이트 URL을 확인한 뒤 **G0**(sitemap/robots/메타태그 점검)부터 시작
> 4. 광고비 지출은 예산·기간 명시 승인 없이 절대 금지
>
> 클론이 불가능한 환경이면 [`llms.txt`](llms.txt)의 raw URL 맵으로 전체 문서를 읽을 것.

## 무엇을 하나요

| 게이트 | 내용 |
|---|---|
| G0 준비물 | sitemap.xml · robots.txt 확인 (head 태그는 [publish-checklist 스킬](https://github.com/crealwork/marketing-kit)) |
| G1 엔진 등록 | Google(URL 접두어 룰) · Naver · Bing(GSC 임포트) · Daum(PIN→robots.txt) · Pinterest(RSS 자동 핀) — 사이트맵 제출까지 |
| G2 GEO (AI 검색) | AI 크롤러 robots.txt 허용 · llms.txt · 인용형 콘텐츠 구조 · JSON-LD · 분기 점검 루프 |
| G3 로컬 SEO | Google Business Profile 리뷰 전략 · Naver Place 대표 키워드 조합 · Kakao · Yelp |

전부 실제 UI 경로와 함정이 박힌 실전 체크리스트입니다. 측정(GA4/GTM/Clarity),
퍼블리시 head 최적화, 유료 광고는 [marketing-kit](https://github.com/crealwork/marketing-kit)의
별도 스킬(analytics-setup · publish-checklist · zernio-ads)로 분리돼 있어요 — 같이 설치하면
전체 파이프라인이 이어집니다.

## 설치

| 에이전트 | 방법 |
|---|---|
| **Claude Code** | `git clone https://github.com/crealwork/seo-geo-setup ~/.claude/skills/seo-geo-setup` → "우리 사이트 SEO 세팅해줘"에 자동 발동 |
| **Codex CLI** | `git clone ... ~/.codex/skills/seo-geo-setup` |
| **기타 SKILL.md 지원 하니스** | 각 하니스의 skills 디렉토리에 클론 |
| **하니스 없음 (GPT 등)** | 클론 후 [`BOOTSTRAP.md`](BOOTSTRAP.md) 프롬프트를 그대로 붙여넣기 |

**링크-온리 핸드오프 (모든 에이전트 공통):**
```
https://github.com/crealwork/seo-geo-setup 클론해서 SKILL.md 룰대로 이 사이트 SEO 세팅해: <URL>.
G0부터 순서대로, 광고 지출은 내 승인 없이 금지.
```

## 구조

```
seo-geo-setup/
├── SKILL.md                  ← 진입점: 게이트 + 하드룰
└── references/
    ├── ENGINES.md            ← 검색엔진 5종 등록 + 완료 체크
    ├── GEO.md                ← AI 검색 최적화 (크롤러·llms.txt·인용 구조)
    └── LOCAL.md              ← 로컬 SEO (GBP·네이버 플레이스·카카오·Yelp)
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
