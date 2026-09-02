# 힉스필드 영상 생성 프롬프트 (C01–C16)

Image-to-Video 방식. 각 컷의 시작 프레임(`Cxx.png`)을 업로드하고, 아래 Motion Prompt를 그대로 붙여넣으면 됩니다.

## 공통 설정
- **Aspect ratio**: 16:9 (1920×1080 소스와 동일)
- **공통 Negative prompt** (모든 컷에 적용 권장):
  `extra limbs, extra legs, extra arms, distorted hands, malformed fingers, warped anatomy, morphing face, flickering identity, floating objects, text, watermark, blurry, low quality`
- **후반 합성 요소는 프롬프트에 넣지 않음**: 빛 리본, 하트 폭죽, 별자리, 물음표, 먹구름, 자막 등은 기획안상 Post(후반 합성) 항목이라 영상 생성 단계가 아니라 편집 단계에서 별도로 얹습니다. 영상 생성 모델은 이런 그래픽 오버레이를 안정적으로 그리지 못해서, 여기 프롬프트는 "실사/애니메이션 동작"만 묘사합니다.
- 힉스필드가 지원하는 길이 프리셋(보통 5s/10s 등)이 기획안의 컷 길이(5~10s)와 정확히 안 맞으면, 가장 가까운 프리셋으로 생성한 뒤 편집에서 트림하세요.

---

### C01 — 치마 뒤 빼꼼 (6s)
이미지: `C01.png` · Camera: Low angle, slow push-in
> The boy leans out a little further from behind the skirt, cherry blossom petals drifting past in the breeze, his eyes blinking with curiosity as a shy smile grows. Gentle handheld sway, warm dappled sunlight flickering through the blossoms.

### C02 — 무릎을 꿇다 (8s) — KEY
이미지: `C02.png` · Camera: Static frontal eye-level, locked-off
> The father's hands gently place the folded white belt into the boy's open palms; the boy looks up and gives a small proud nod. Subtle natural breathing motion, soft warm lamplight, faint dust motes drifting in the air. Keep the belt itself simple and physical — no glow effects.

### C03 — 사범이 되다 (8s) — 몽타주, 별도 처리 권장
이미지: `C03.png` · Camera: Fixed frame, subject-replacement transition
> ⚠️ 이 컷은 흰→검은 띠로 색이 바뀌고 인물이 성장하는 몽타주라 영상 생성 모델 한 번에 자연스럽게 만들기 어렵습니다. 두 가지 방법 중 선택 추천:
> 1) **정지 이미지 그대로 두고 편집에서 크로스디졸브**로 성장 과정을 표현 (가장 안전)
> 2) 짧은 동작만 요청: `The young martial artist practices a slow, confident kick and returns to a ready stance, surrounded by cheerful younger students clapping. Warm dojang lighting, steady camera.` (색이 바뀌는 띠는 프롬프트에 넣지 말고 편집 단계에서 색보정/디졸브로 처리)

### C04 — 물음표 뿅, 손사래 (8s)
이미지: `C04.png` · Camera: Two-shot, same framing repeated
> The woman speaks warmly with an inviting open-hand gesture; Namgyu waves both hands "no" twice with a flustered smile, then pauses, tilts his head, and slowly nods in agreement. Natural idle sway, warm dojang ambient light.

### C05 — 혼자 걷는 길 (6s) — KEY
이미지: `C05.png` · Camera: Side tracking shot, golden hour
> Namgyu walks at a steady, confident pace along the sunset street, his suit jacket swaying gently, warm golden light catching his silhouette. Camera tracks smoothly alongside him at the same pace.

### C06 — 매무새 정리 (5s)
이미지: `C06.png` · Camera: Medium shot, reflection framing
> Namgyu adjusts his jacket lapel with both hands while glancing at his reflection in the window glass, exhales nervously, then gives a small satisfied smile. Subtle head tilt, warm golden-hour light glinting softly off the glass.

### C07 — 문이 열리고 (7s) — KEY
이미지: `C07.png` · Camera: POV from Namgyu, slow motion
> The restaurant door swings open and Gayoung steps through; her hair and dress sway gently in slow motion as she walks in, a soft warm backlight blooming behind her. Cherry blossom petals drift lazily through the air.

### C08 — 하트 폭죽 (7s)
이미지: `C08.png` · Camera: Locked close-up
> Namgyu holds a calm, composed expression on the surface, only a faint nervous swallow and a subtle widening of his eyes betraying him. Restrained, natural micro-expressions — no exaggerated motion, this frame stays mostly still to leave room for a post-production heart-burst overlay.

### C09 — 라자냐가 지워짐 (6s)
이미지: `C09.png` · Camera: Tabletop top-down tilting up to faces
> Camera tilts smoothly up from the plate to Namgyu's face; he is completely absorbed, eyes fixed on Gayoung, gesturing lightly with his fork without ever looking down at his food.

### C10 — 별자리, 소주 다섯 병 (7s)
이미지: `C10.png` · Camera: Two-shot, amber light, slow pull-back
> Namgyu and Gayoung laugh and talk animatedly across the table, leaning in and gesturing warmly; through the window behind them the night sky slowly, subtly brightens toward pre-dawn light. Camera pulls back slowly.

### C11 — 밤마다 야식 (8s)
이미지: `C11.png` · Camera: Two-shot eye-level, amber light
> Both of them open the takeout bag at the same moment, eyes widening in unison, then burst into synchronized laughter, shoulders shaking. Cozy dim living-room lamp light flickers softly.

### C12 — 강릉 바다 (10s) — KEY
이미지: `C12.png` · Camera: Wide → low-angle, slow push-in
> The two of them kick water at each other and laugh at the shoreline, waves rolling in around their feet, hair blown by the sea breeze, water droplets catching the sunlight. Camera slowly pushes in low across the waterline.

### C13 — 얼음 (9s)
이미지: `C13.png` · Camera: Locked two-shot, desaturate on Namgyu's side
> Another splash lands and Gayoung's expression suddenly turns stern; Namgyu freezes mid-motion, his smile fading into a nervous, apologetic grimace. Keep his freeze subtle and natural — the raincloud graphic will be added in post.

### C14 — 못 이기는 척 (9s)
이미지: `C14.png` · Camera: Two-shot, extremely slow push-in
> Namgyu shyly holds out a single flower; Gayoung tries to hold back a smile, fails, and laughs softly as she takes it. Warm sunlight gradually brightens across the scene as the mood lightens.

### C15 — 띠에서 리본으로 (7s)
이미지: `C15.png` · Camera: Close dissolve to frontal (C02와 동일 구도 유지)
> Namgyu kneels in the same pose as the opening scene, looking up with quiet emotion. Keep the motion minimal and steady — a slow breath, a soft blink, a growing smile. The belt-to-ribbon-to-ring transformation and the child-silhouette overlap will be handled in post-compositing, so the live motion here should stay simple.

### C16 — 나와 결혼해줄래? (9s) — KEY
이미지: `C16.png` · Camera: Side angle, extremely slow push-in, hold on final frame
> Namgyu opens the ring box and looks up hopefully; Gayoung's hands rise to cover her mouth in joyful shock, her eyes glistening. The golden backlight glows slightly warmer as the camera holds a slow, steady push-in through to the end.

---

## 체크리스트
- [ ] 각 컷 생성 후 손가락 개수·다리 개수·얼굴 일관성 확인 (C16에서 겪었던 아나토미 오류 재확인)
- [ ] C02와 C15가 실제 영상에서도 같은 리듬/속도로 움직이는지 비교 (수미상관 연출)
- [ ] C03은 몽타주라 별도 처리 방식 결정 필요
- [ ] Post 항목(빛 리본/하트 폭죽/별자리/물음표/먹구름/자막/띠→리본→반지 트랜지션)은 영상 생성 이후 편집 단계 작업으로 별도 진행
