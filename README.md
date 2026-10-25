# 신메뉴 개발 스킬 (Menu Development Skill)

메뉴개발팀의 **신메뉴 개발을 돕는 Claude 보조 스킬**이다. 아이디어 접수부터 출시 준비까지 7단계로 진행하고 각 단계 산출물을 5인 페르소나 토론으로 검토한다. 현재 외식 트렌드와 제철 식자재를 반영하며 모든 판단을 출시 후 판매 목표와 가맹점 수익으로 연결한다.

🔗 공개 페이지 https://lfsykim-boop.github.io/MenuDevelopment/

## 핵심 특징
- **7단계 개발 흐름** 목표·콘셉트 → 시장·경쟁 → 레시피 → 원가 → 주방 운영 → 검증 → 출시 준비
- **5인 페르소나 토론** R&D 셰프 · 원가·구매 · 슈퍼바이저 · 브랜드 기획 · 성과 비평가
- **9.7 합격선 + 루브릭** 점수 구간 앵커로 자의적 채점 방지
- **가드레일** 데이터 날조 금지 · 데이터 게이트 · 제철 단종·대체 계획 강제 등
- **트렌드·제철 반영** 실행 시 트렌드를 새로 검색하고 출시 시기의 제철 식자재를 반영
- **사람이 주체** 스킬은 보조이며 최종 판단은 메뉴개발팀이 한다

## 저장소 구조
```
.claude/skills/new-menu-development/   스킬 본체
├─ SKILL.md                            스킬 정의 (역할·컨텍스트·도구·워크플로우·루브릭·가드레일)
├─ references/company-reference.md     회사 기준 레퍼런스 템플릿 (브랜드·원가·제철·운영·판정)
└─ templates/template-menu-plan.html   기획안 결과물 빈 서식
docs/                                  설계 근거와 데모 기록
web/                                   공개 열람용 결과물 (데모 HTML·PDF·빈 템플릿)
tests/                                 발동·게이트·가드레일 검증 시나리오
```

## 사용 방법
1. `.claude/skills/new-menu-development/` 폴더를 Claude 스킬 위치에 둔다
2. `references/company-reference.md`에 회사·브랜드 기준을 채운다 (POS 비중·원가·제철·판정 기준)
3. Claude에서 "신메뉴 개발해줘" 또는 "제철 메뉴 기획해줘"로 발동한다
4. 7단계를 진행하고 결과를 HTML로 뽑는다 (`templates/template-menu-plan.html` 양식)

## 데모
- [미역국 브랜드 A 경쟁 분석 기반 신메뉴 추천](web/sample-brand-menu-recommendation.html) ([PDF](web/sample-brand-menu-recommendation.pdf))
- [기획안 빈 서식 템플릿](web/template-menu-plan.html)

## 라이선스
MIT License · [LICENSE](LICENSE)
