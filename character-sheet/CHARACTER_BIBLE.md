# 디즈니 프로포즈 영상 — 캐릭터 바이블 (단일 출처)

생성 도구: `~/.claude/skills/codex-image/scripts/gen.sh` (codex-image 스킬)
아래 **고정 블록**을 모든 씬 이미지 프롬프트에 그대로 붙여넣어야 캐릭터가 일관되게 나온다.

## 파일
| 파일 | 용도 |
|---|---|
| `01_namgyu_turnaround.png` | 남규 턴어라운드(앞·3/4·측면·3/4후·뒤 + 위/아래 헤드 인셋) |
| `02_gayoung_turnaround.png` | 가영 턴어라운드(동일 구성) |
| `03_couple_height_compare.png` | **키 차이 기준표** |
| `_refs/` | 실사 레퍼런스 콜라주(생성 시 `--ref` 로 사용) |
| `_rejects/` | 채택 안 된 시안 |

## ⚠️ 키 차이 (절대 규칙)
**가영이의 정수리 = 남규의 눈썹 높이.** 약 12cm 차, 머리 1/3 정도.
- 가영 눈높이 ≈ 남규의 입/턱 높이.
- 흔한 실패: 가영을 남규 어깨/턱 높이로 그림 → **너무 작다. 틀림.**
- 가영은 "키 큰 슬림한 여자", 남규는 "그보다 조금 더 큰 남자".

## 공통 스타일 블록 (항상 포함)
```
STYLIZED DISNEY / PIXAR 3D ANIMATED FEATURE FILM look. Rendered CG cartoon
character — NOT photorealistic. Large expressive glossy eyes, smooth simplified
stylized skin, soft rounded appealing shapes, warm cinematic subsurface shading.
```

## 남규 (NAMGYU) 고정 블록
```
Korean man, early 30s, tall fit athletic taekwondo instructor, about 7.5 heads
tall, long legs, broad square shoulders tapering to a trim waist, defined
muscular arms. Face: soft rounded kind boyish jaw with gently full cheeks
(NOT a chiseled idol jaw, NOT chubby), small warm dark-brown eyes that crinkle
into happy curves when he smiles, straight thick dark eyebrows, small rounded
nose, soft pink lips in a shy closed-lip smile, short messy textured
black-brown fringe falling over the forehead, fair warm skin.
Default wardrobe: black short-sleeve polo shirt, dark charcoal track pants,
white sneakers.
```
씬별 의상 대안: 흰 도복 + 검은 띠(Scene 2) / 정장(소개팅) / 체크 셔츠 + 흰 티(일상) / 코트 + 회색 머플러(겨울)

## 가영 (GAYOUNG) 고정 블록
```
Korean woman, late 20s, slender and graceful, narrow shoulders, long neck,
long legs, tall for a woman. Face: slim oval face with a soft pointed chin,
fair porcelain skin, long straight jet-black center-parted hair falling past
the chest with softly tapered ends, gently arched thin dark eyebrows, large
warm dark-brown almond eyes with a calm gentle gaze, small slim straight nose,
full rosy-pink lips in a soft quiet smile.
Default wardrobe: cream ribbed knit top, light beige wide-leg trousers,
white sneakers, a thin gold necklace with a small pendant.
```
씬별 의상 대안: 검은 슬리브리스 랩 원피스(첫 만남) / 회색 니트(카페) / 아이보리 무스탕(겨울) / 흰 셔츠 + 크림 팬츠 + 네이비 캡(강릉 바다)

## 배경 규칙 (시트 재생성 시)
```
Completely OPAQUE flat light warm-gray studio background (#E8EAEC) filling the
entire frame. NO transparency, NO alpha channel, NO black or red areas.
```
> 이 문구를 빼면 codex가 투명 배경으로 뽑아 검정/빨강 아티팩트가 생긴다(1차 시안 실패 원인).

## 연결 모티프
흰 도복 띠 → 색이 물들며 검은 띠 → 마지막에 붉은 실/반지 리본. 씬 전환에 사용.
