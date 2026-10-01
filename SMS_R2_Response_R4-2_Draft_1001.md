# SMS Technical Note — R2 답변서 초안: Reviewer 4, Comment 2 (MRD 셀 '블랙박스')

- **논문**: A free-volume-based Bingham–Papanastasiou model for temperature-dependent flow behavior of magnetorheological fluids (Technical Note)
- **원고 번호**: SMS-120630.R1 → 이번 수정본 .R2 (마감 2026-10-13, 연장 요청 예정)
- **대상 코멘트**: R4-2. R1-6(원심 편석)·R4-1/R1-1(실용성)과 교차 참조
- **작성**: 2026-10-01, 초안 v0.1
- **표기 규칙**: `[A1-n]`, `[A2-n]`, `[B-n]`은 엘리자 작업 결과로 채울 자리(소유자는 §0.3), `[P]`는 교수님 판단, `{IF D}` / `{IF R}`는 진단 결과에 따라 택일하는 블록
- **연계 문서**: `SMS_R2_Revision_Roadmap_1001.md` (P1-7, P1-4), `SMS_R2_Elliza_Instructions_1001_EN.md` (지시 메일)

> 이 초안은 **엘리자 작업(A1~A3, B1~B4) 결과 없이는 제출할 수 없음**. 수치 자리를 채우기 전에는 문장 구조만 확정하는 용도임.

---

## 0. 작성 메모 (국문)

### 0.1 답변 전략 (10/1 의견서 반영)

1. **첫 문장에서 '블랙박스' 지적을 인정**함. 기조는 방어가 아니라 "문서화 + 정량 상한 + 주장 수위 조정".
2. **로드맵 P1-7에서 삭제한 논거**
   - "대부분의 MRF 연구가 PP20/MRD를 쓴다": 리뷰어가 "all these cells…"로 선제 차단함. [50]은 커스텀 셀, [37]은 셀 아티팩트를 다룬 논문이라 인용하면 역효과.
   - "셀 의존성은 어떤 모델에도 공통": tu quoque. 아티팩트는 모델에 균등하게 흡수되지 않음(저전단 형상 파라미터 m_p를 가진 BP가 가장 많이 보상받음).
   - "더블갭은 향후 과제"식 브러시오프: 리뷰어는 더블갭도 evaluation-grade라고 했음. 요구는 장비가 아니라 주장 수위.
   - 갭 변화(Mooney) 슬립 시험 제안: MRD에서는 갭이 B(r)를 바꿔 판별 불가([37]). 제안 자체가 순진해 보임.
3. **유지하되 격하한 논거**
   - 2종 유체(§3.3) → "구조의 일반성" 근거로만. 같은 셀이라 셀 독립성 근거는 아님.
   - 데이터시트 τ_y(B) 대조 → 내부 계산 후 25 % 이내일 때만 제시. 472 mT에서 데이터시트보다 낮게 나오면 벽면 한계로 읽힐 수 있음.
   - Lv et al. [29] Doolittle → a, b 비교가 아니라 정규화 η(T)/η(25 °C) 곡선 비교로. "different rheometer" 표현은 Lv의 장비 확인 후에만.
4. **새로 넣는 것**: §2.2 측정 소절(프로토콜 전면 공개), 발열·에지·편석의 정량 상한, n′(γ̇) 공개, 신선 시료 온도순서 반전·상하향 스윕, 자기장 확장(4–5 A), 링 유/무 토크, τ_y(B,T)·m_p(B)의 "프로토콜 조건부 보정 파라미터" 재정의, 초록·결론 표현 완화, Table 3가 조건별 τ_y 18개 기반임을 명시.
5. **쓰지 말 것**: "shear-rate-independent cell factors are multiplicative and cannot generate the B or T dependence". 비자성 벽면의 전달가능 응력 한계는 전단율과 무관하면서 B·T에 의존하므로 이 문장은 틀림. 리뷰어가 바로 반박 가능.
6. **분기(decision gate)**: 진단 A2와 대조실험 B1–B2 결과를 보고 결정
   - **경로 D(방어)**: 50→70 °C 계단과 고온에서의 자기장 지수 저하(0.75→0.35)가 신선 시료에서 재현되고, 상하향 이력이 작으며(<10 %), 4–5 A에서 90 °C의 τ_y가 계속 증가함 → "재현 가능한, 프로토콜 조건부 유체 응답"으로 제시. `{IF D}` 블록 사용.
   - **경로 R(재프레이밍/재식별)**: 이력·비가역·응력 상한이 드러남 → 해당 조건 재측정 후 재식별하거나 유효 온도범위를 축소(예: 10–70 °C 헤드라인, 80/90 °C는 탐색적). `{IF R}` 블록 사용.
   - 어느 경로든 폐쇄식 형태와 동일 조건 3모델 비교는 유지됨.

### 0.2 리뷰어가 지목하지 않았지만 선제 처리하는 항목

- Table 2의 온도 감쇠 크기(10→90 °C에서 71–79 %), 50→70 °C 단일 계단(−35/−47/−50 %), 319→472 mT 지수 저하(10–25 °C 0.73–0.76 → 70–90 °C 0.34–0.39). 답변서에는 "내부 일관성 점검을 수행했다"는 한 문단만, 수치·그림은 Supplementary. 상세 논의는 R1-2 답변과 공유.
- Table 3 지표가 조건별 τ_y 18개 기반임을 §2.6/§3.2에 명시하고 식(21)의 자체 잔차(18조건 RMSE 644 Pa, 70 °C/472 mT에서 +23 %, 90 °C에서 −16 %)를 보고. c(B) 선두계수를 4유효숫자 이상으로. R1-8/R1-2 답변과 연결.
- 보정계수 "0.7–0.8" 문구는 n′ 최소값 확인 후 실제 범위로 수정. (0.7은 n′ = −0.2, 즉 토크가 속도에 따라 감소한다는 뜻이므로 그대로 두면 안 됨.)
- 신규 참고문헌(세션에서 원문 미확인, **엘리자 A3에서 서지·내용 확인 필수**): Laun, Schmidt, Gabriel, Kieburg 2008 Rheol. Acta 47:1049 (단일갭 MRD의 림 자속 최대·반경 편석); Laun, Gabriel, Kieburg 2010 J. Rheol. 54:327 (twin-gap); Laun, Gabriel, Kieburg 2011 Rheol. Acta 50:141 (벽면 재질·거칠기와 전달가능 응력); Morillas, Yang, de Vicente 2018 J. Rheol. 62:1485 (double-gap plate–plate).

### 0.3 placeholder 소유자

| 기호 | 내용 | 출처 |
|---|---|---|
| `[A1-n]` | 프로토콜 사실(플레이트 사양·프로파일 깊이, 하판 재질, 링 재질·치수·간극·충전, 시료량, 프리시어, 평형시간, 체류시간, 순서, 반복, 센서 위치, B 보정 방식, 셀 정격 온도, m_p 식별 방식) | 엘리자 A1 |
| `[A2-n]` | 기존 데이터 진단(링 반복성 %, n′ 최소값·실제 보정계수 범위, 오프상태 800–1200 s⁻¹ 기울기 vs 0.102 Pa·s, Lv 대조, 140CG 정규화 감쇠, 데이터시트 대조, 구간별 RMSE, 지수표) | 엘리자 A2 |
| `[B-n]` | 대조실험(온도순서 반전·상하향 이력·25 °C 재측정, 자기장 확장, 60 s 홀드 토크 드리프트·온도, 링 유/무 토크 차) | 엘리자 B1–B4 |
| `[P]` | 교수님 판단(연장 요청, 경로 D/R, 데이터시트 대조 공개 여부, 유효 온도범위) | 오 교수님 |

---

## 1. Response to Reviewer 4, Comment 2 (영문 초안)

```
--------------------------------------------------------------------------
Comment R4-2
"A significant issue appears to be that the MRD cell essentially functions as a
'black box'. While the authors highlight certain critical aspects regarding
measurements, there are many more that are not addressed (wall slip issue, open
surface instability etc). Anton Paar also offers a double-gap magnetic system
for the MRD for good reason. While all these cells enable the evaluation of MR
fluid parameters, they are likely can be inadequate to precise scientific
measurements. The proposed model modification may potentially reflect the
specific characteristics of the cell itself rather than the underlying physics
of MR fluids. In other words, the model may simply be fitting the mathematics
to the specific design of the measuring cell. Furthermore, as previously noted,
its practical utility has not yet been demonstrated."

Response:

We thank the Reviewer for this comment and accept its central point. The
revised manuscript did not document the measuring cell and the protocol in
enough detail for a reader to judge what the cell does to the data, and it did
not state the limits of a single-gap, open-edge parallel-plate magnetocell for
quantitative measurements. We also agree that twin-gap and double-gap cells
(Laun et al. 2010 [new ref]; Morillas et al. 2018 [new ref]; the commercial
TwinGap geometry) were developed because single-gap cells suffer from radial
non-uniformity of the flux density, sample loss and particle migration at high
speed, uncompensated normal force and, with non-magnetic plates, a wall-limited
transmissible stress (Laun et al. 2008, 2011 [new refs]). Such a cell was not
available to us, and we now say so in the manuscript. Our response therefore
has three parts: we document what was controlled, we bound the effects the
Reviewer lists instead of asserting their absence, and we scale the claims of
the paper to what a single-cell data set can support.

(1) Documentation. Section 2.2 now contains a subsection "Measurement
considerations and limitations", and Supplement S1 gives the full protocol. In
brief: the upper plate is a profiled titanium plate (PP20/MRD/TI/P2; the "T1"
in the previous version was a typographical error for "TI"; profile depth
[A1-1] µm), which is the configuration recommended to suppress wall slip of MR
fluids on non-magnetic walls (Laun et al. 2011; [37]); the lower plate is
[A1-2]. A non-magnetic [A1-3] retaining ring (inner diameter [A1-4] mm, height
[A1-5] mm, radial clearance to the plate [A1-6] mm) was fitted after sample
expulsion above approximately [A1-7] rpm was diagnosed; with the ring the
run-to-run deviation of the flow curves was below [A2-1] % (n = [A1-8]),
against 25-48 % without it (Table S1). We also state the sample volume, the
loading and trimming procedure, the off-state pre-shear, the equilibration time
at each temperature, the measurement sequence, the dwell time per point
([A1-9] s), the point spacing (30 points from 100 to 3000 rpm in 100 rpm
steps), the number of repeats, the location of the temperature sensor, and how
the quoted flux densities were obtained ([A1-10]: Hall-probe position;
empty-gap or in-sample calibration). The ring repeatability data, which were
shown in our first-round reply and had been removed from the manuscript, are
restored as Table S1.

(2) Bounds. Rather than assert the absence of the effects the Reviewer lists,
we estimated them and, where possible, measured them.

- Viscous heating. At the most severe condition (10 °C, 472 mT, 3000 rpm) the
  dissipation is approximately 13 W in the 0.31 mL sample. A one-dimensional
  conduction estimate gives a mid-gap temperature rise at the rim of [8-16] K
  for k = [1-0.5] W m^-1 K^-1 with both plates at the set temperature, reached
  within a few seconds. A 60 s hold at 3000 rpm showed a torque drift of [B3-1]
  % and the ascending and descending sweeps differed by [B1-1] % (Fig. S2).
  Because the dissipation scales with tau_y(B,T), this effect reduces the
  apparent temperature dependence at low temperature and high field; it cannot
  produce the decrease of tau_y with temperature reported in Table 2.

- Open surface and edge. The ring converts the free rim into a confined edge.
  The torque of fluid wetting the cylindrical edge of the plate is bounded by
  3t/R relative to the face torque (about 30 % per millimetre of wetted
  height); a direct comparison with and without the ring at <= 500 rpm, where
  no expulsion occurs, gave a difference of [B4-1] % (Fig. S[ ]).

- Wall slip. The profiled upper plate and the magnetic lower plate are the
  standard countermeasures. The non-Newtonian index n' = d ln M / d ln
  gamma-dot_R was [A2-2: non-negative in all 18 curves, with (3+n')/4 between
  0.75 and 0.80; the range "0.7 to 0.8" given in the previous version was a
  rounding and has been corrected] (Fig. S1).
  {IF D} In addition, when the current was raised to [4-5] A ([B2-1] mT), the
  yield-stress parameter continued to increase with field at both 25 and 90 °C
  (Fig. S3), which argues against a wall-limited stress ceiling at the fields
  used in the study.
  {IF R} We note, however, that the field dependence of tau_y flattens at the
  higher temperatures (Table 2), which may reflect a temperature-dependent
  limit of the transmissible stress at the non-magnetic wall; we have
  therefore restricted the headline validation to [10-70] °C and present the
  80 and 90 °C data as exploratory (Section 3.2).

- Particle migration and settling. Under field, the magnetic interparticle
  force exceeds the centrifugal force on a particle by three to four orders of
  magnitude, and the wall-supported particle-phase body force at 101 g (about
  1 kPa) is below tau_y at every condition, so centrifugal migration is not
  expected in the on-state data used for identification; the off-state
  viscosity data were taken at 100 s^-1, where the rim acceleration is 0.1 g.
  Settling during the off-state equilibration was controlled by [A1-11:
  pre-shear at 100 s^-1 for [ ] s immediately before the field was applied /
  a fresh sample at each temperature]. These points are expanded in our reply
  to Reviewer 1, Comment 6.

- Field. The quoted flux densities (166, 319 and 472 mT at 1, 2 and 3 A) are
  [A1-10: Hall-probe readings in the empty gap at the measuring temperature /
  in-sample values from the instrument's calibration]. In single-gap cells the
  in-sample flux density depends on the sample permeability and varies
  radially (Laun et al. 2008), so we treat B as a calibrated label of the field
  condition rather than as the local flux density in the fluid, and we now
  state explicitly that c(B), d(B) and m_p(B), which pass through three field
  levels, are interpolants tied to this labelling.

(3) Does the model fit the cell or the fluid? We cannot settle this from a
single cell, and the revised text no longer implies that we can. We can,
however, separate what is robust from what is conditioned on the cell. The
off-state viscosity-temperature relation is measured at low speed and low
stress, agrees with the manufacturer's value at 40 °C within [A2-3] % (slope
over 800-1200 s^-1), and its normalised form eta(T)/eta(25 °C) agrees with the
Doolittle-form fit reported by Lv et al. [29] for the same fluid within [A2-4]
% (Fig. S4); this component is not in question. The field-induced part,
tau_y(B,T) and m_p(B), is identified from high-shear data in this cell and
therefore inherits its wall, edge and field characteristics. We have taken
three steps on this part.

First, we examined the internal consistency of Table 2 on freshly loaded
samples, with the temperature sequence reversed and intermediate temperatures
(40 and 60 °C) added: [B1-2: the decrease of tau_y between 50 and 70 °C and the
weaker field dependence at high temperature were reproduced within [ ] %, the
ascending/descending hysteresis was below [ ] %, and the 25 °C curve measured
after the 90 °C run agreed with the initial one within [ ] %] (Fig. S2).
{IF R} [Replace with: the repeat measurements showed [ ]; the affected
conditions were re-measured and the parameters in Tables 2-4 re-identified.]

Second, the normalised decay tau_y(T)/tau_y(25 °C) of MRF-140CG, measured with
the same protocol, [A2-5: coincides with / differs from] that of MRF-132DG
(Fig. S[ ]). We report this without claiming it as evidence of cell
independence, since both fluids were measured in the same cell; it shows only
that the constitutive form applies to both.

Third, [P: include only if within ~25 %] the identified 25 °C yield stresses
agree with the manufacturer's tau_y-H data within [A2-6] % at 166, 319 and 472
mT when the fluid's B-H curve is used for the conversion (Supplement S1),
[with the largest deficit at 472 mT, which we discuss as a possible wall effect].
Reported temperature sensitivities of the on-state yield stress of carbonyl-
iron MRFs vary widely in the literature, from nearly temperature-independent in
sealed or device-type fixtures [22,50] to decreases comparable with ours in
commercial parallel-plate magnetocells [23,51]. Part of this spread is likely
to reflect cells and protocols as much as fluids, and we therefore do not
claim that the temperature coefficients identified here are cell-independent.

(4) Claims. Accordingly, we have revised the wording throughout. tau_y is now
defined as the high-shear dynamic yield-stress parameter (the Bingham intercept
over 10^2 to 3.1 x 10^3 s^-1) obtained with the documented cell and protocol;
m_p is described as an empirical transition parameter (1/m_p = 90-135 s^-1)
rather than as a numerical regularisation; and the Doolittle term is described
as a free-volume-type viscosity-temperature fit. The Abstract, Section 3.2 and
the Conclusion no longer state that the model captures the underlying physics
of MR fluids or provides a robust framework; they state that the model provides
a compact, well-behaved constitutive closure for the measured high-shear
response, whose field- and temperature-dependent parameters are calibration
values that must be re-identified for other fluids, cells or devices. The
limitation paragraph in the Conclusion makes the cell dependence explicit. We
also now state that the pooled metrics in Table 3 use the 18 per-condition
tau_y values, and we report the deviation of the closed-form expression (21)
from these values together with the temperature at which it reaches zero,
which defines its range of validity (see also our reply to Reviewer 1,
Comments 2 and 8).

(5) Practical utility. This point is addressed under Comment 1 and under
Reviewer 1, Comment 1, where a device-level example is now given. We note here
only that the limitation paragraph specifies the conditions under which such
use is legitimate: the closure can be used for a device operating with the
same fluid once its parameters have been identified under conditions
representative of that device.

Changes made: Section 2.2 (new subsection "Measurement considerations and
limitations", pp. [ ]); Section 2.6 (identification of m_p(B); statement on
the tau_y values used in Table 3; coefficients of Eqs. (17)-(21) to four
significant figures); Sections 3.1-3.3 (wording); Abstract and Conclusion
(wording; limitation paragraph); Supplement S1 (protocol table), Table S1 (ring
repeatability), Figs. S1-S4 (n'(gamma-dot) for all flow curves; ascending/
descending and reversed-sequence sweeps on fresh samples; field extension at
25 and 90 °C; off-state viscosity cross-checks).
--------------------------------------------------------------------------
```

---

## 2. 원고 삽입 문안 (영문 초안)

### 2.1 §2.2 신설 소절 "Measurement considerations and limitations" (본문, 약 350단어; 표·그림은 Supplementary)

```
2.2.1 Measurement considerations and limitations

All flow curves were obtained in a single-gap parallel-plate magnetocell (MRD
170/1T) with a profiled titanium upper plate (PP20/MRD/TI/P2, profile depth
[A1-1] µm) and a [A1-2] lower plate that forms the magnetic pole. The profiled,
non-magnetic upper plate is the configuration recommended to suppress wall slip
of MR fluids on non-magnetic walls [Laun 2011; 37]. A non-magnetic ([A1-3])
retaining ring (inner diameter [A1-4] mm, height [A1-5] mm, radial clearance
[A1-6] mm) was fitted after sample expulsion above approximately [A1-7] rpm was
observed; with the ring, run-to-run deviations of the flow curves were below
[A2-1] % (n = [A1-8]), compared with 25-48 % without it (Table S1). A sample of
[A1-12] µL was loaded [A1-13], trimmed [A1-14], pre-sheared at 100 s^-1 for
[A1-15] s in the off-state and equilibrated for [A1-16] min at each temperature
before the field was applied; [A1-17: a fresh sample was used at each
temperature / the same sample was used in the order ...]. Each flow curve
consisted of 30 points from 100 to 3000 rpm in steps of 100 rpm (about 105
s^-1 in nominal rim shear rate), in ascending order, with [A1-9] s per point,
and was repeated [A1-8] times. Temperature was measured [A1-18] and controlled
by the circulator; the upper plate is not actively thermostatted [A1-19: hood
used / not used]. The quoted flux densities (166, 319 and 472 mT at 1, 2 and 3
A) are [A1-10]. In single-gap cells the flux density in the sample depends on
the sample permeability and varies radially [Laun 2008]; B is therefore used
here as a calibrated label of the field condition rather than as the local flux
density in the fluid.

Several cell-related effects were bounded rather than assumed absent. (i)
Viscous dissipation at the highest speed and field (10 °C, 472 mT, 3000 rpm)
is approximately 13 W in the 0.31 mL sample; a one-dimensional conduction
estimate gives a mid-gap temperature rise at the rim of [8-16] K for k =
[1-0.5] W m^-1 K^-1 with both plates at the set temperature, consistent with
the torque drift of [B3-1] % measured during a 60 s hold at 3000 rpm and the
ascending/descending difference of [B1-1] % (Fig. S2). Because the dissipation
scales with tau_y(B,T), this effect reduces the apparent temperature
dependence at low temperature and high field and cannot generate the decrease
of tau_y with temperature reported in Section 3.1. (ii) The torque of fluid
wetting the plate edge inside the ring is bounded by 3t/R per unit wetted
height t relative to the face torque; a comparison with and without the ring
at <= 500 rpm gave a difference of [B4-1] % (Fig. S[ ]). (iii) Under field,
the magnetic interparticle force exceeds the centrifugal force on a particle
by three to four orders of magnitude and the wall-supported particle-phase
body force at 101 g (about 1 kPa) is below tau_y at every condition, so
centrifugal migration is not expected in the on-state data used for
identification; the off-state viscosity data were taken at 100 s^-1 (0.1 g at
the rim). (iv) The non-Newtonian index n' = d ln M / d ln gamma-dot_R was
[A2-2] in all flow curves, with (3+n')/4 between [0.75] and [0.80] (Fig. S1).
(v) Thermal expansion of the measuring stack changes the gap by about [A1-20]
% over 10-90 °C [A1-21: compensated / not compensated], which affects the
shear-rate axis but not the yield-stress plateau.

Within these bounds the identified parameters remain conditioned on the cell
and the protocol: the absolute level of tau_y may differ in cells with other
wall, edge and field-homogeneity characteristics, such as twin-gap or
double-gap cells [Laun 2010; Morillas 2018], and tau_y(B,T) and m_p(B) should
be read as calibration parameters of the documented measurement rather than as
intrinsic material constants.
```

### 2.2 결론 한계 단락 (3문장)

```
All flow curves were obtained in a single-gap, open-edge parallel-plate
magnetocell (profiled titanium upper plate, 1 mm gap, retaining ring) under
the protocol documented in Section 2.2 and Supplement S1. The identified
yield-stress and transition parameters are therefore protocol-specific
calibration values whose absolute level, and possibly part of their
temperature dependence, may differ in cells with other wall, edge and
field-homogeneity characteristics, whereas the constitutive form and the
off-state viscosity-temperature relation are expected to transfer. The model
should accordingly be read as a semi-empirical description of the measured
high-shear response within the tested ranges, and its parameters should be
re-identified for other fluids, cells or device geometries.
```

### 2.3 표현 교체표 (초록·§3.2·§3.3·결론)

| 현재 표현 | 교체 | 위치 |
|---|---|---|
| "provides a robust and accurate framework for describing the coupled effects…" | "provides a compact constitutive closure for the measured high-shear response under coupled field and temperature conditions, within the documented measurement protocol" | 초록, 결론 |
| "physically interpretable" / "free-volume representation" (물리 해석 주장 맥락) | "free-volume-type (Doolittle-form) viscosity–temperature fit" | 초록, §2.3, §3.2 |
| "exponential regularization" (m_p 설명 맥락) | "exponential transition term with an empirical transition parameter m_p (1/m_p ≈ 90–135 s⁻¹)" | §2.4, §3.1 |
| "yield stress τ_y" (정의 첫 등장) | "high-shear dynamic yield-stress parameter τ_y (Bingham intercept over 10²–3.1×10³ s⁻¹)" | §2.4, §2.6 |
| "suitable for numerical simulation, device design modeling, and model-based control" | "provides the quasi-static constitutive map τ(γ̇, B, T) required by…" (R1-5 답변과 통일) | 서론, 결론 |
| "the correction factor consistently remained within the range of 0.7 to 0.8" | "[A2-2]에 따라 실제 범위로 수정, 예: 0.75 to 0.80" | §2.2 |
| "PP20/MRD/T1/P2" | "PP20/MRD/TI/P2" | §2.2 |
| Table 3 캡션/§3.2 | "Metrics computed with the per-condition τ_y values of Table 2; the deviation of the closed-form Eq. (21) from these values is given in Table [ ]" 추가; Table 3의 "0–472 mT"는 "166–472 mT"로 | Table 3, §3.2 |

### 2.4 Supplementary S1 구성안

| 항목 | 내용 | 출처 |
|---|---|---|
| Table S0 | 프로토콜 표(장비·플레이트·링·시료·프리시어·평형·체류·간격·순서·반복·센서·B 보정·셀 정격) | A1 |
| Table S1 | 링 유/무 반복성(7.29 회신 Fig A–D·Table A–C 복원, n 명시) | A2 |
| Fig. S1 | n′(γ̇) 18곡선 + (3+n′)/4 범위 | A2 |
| Fig. S2 | 신선 시료 25→40→50→60→70→90→25 °C, 472 mT 상하향 스윕, 25 °C 재측정 | B1 |
| Fig. S3 | 자기장 확장(4–5 A) 25 °C vs 90 °C τ_y(B) | B2 |
| Fig. S4 | 오프상태 점도: 800–1200 s⁻¹ 기울기 vs 데이터시트, 정규화 η(T)/η(25) vs Lv et al. [29] | A2 |
| Fig. S5 | 링 유/무 토크(≤500 rpm, 0 mT·166 mT) | B4 |
| Table S2 | 발열 추정(토크·동력·q·ΔT, k와 체류시간 가정 명시) + 60 s 홀드 토크·온도 로그 | A2/B3 |
| Table S3 | 식(21) vs Table 2 잔차, τ_y=0 온도(106/112/120 °C), c(B)·d(B)·m_p(B) 4유효숫자 | A2 |
| (선택) Fig. S6 | 140CG vs 132DG 정규화 τ_y(T)/τ_y(25) | A2 |
| (선택) Table S4 | 25 °C τ_y(B) vs LORD τ_y–H (B→H 변환 명시) — `[P]` 25 % 이내일 때만 | A2 |

---

## 3. 교차 참조 (다른 답변과의 정합)

- **R1-6 (원심 편석)**: §2.2.1 (iii)와 Table S1·Fig. S2를 인용. 로드맵 P1-4의 Stokes 드리프트 "<1 % of R" 주장은 체류시간 [A1-9]를 명시한 뒤에만 사용(오프상태 캐리어 점도 기준 10 s 체류 시 1–9 % of R까지 가능). 쌍극자력 비(10³–10⁴)와 벽면 지지 체적력(≈1 kPa vs τ_y) 논거를 중심으로. 원고에 "no torque drop"이라 쓰려면 n′ 최소값 확인이 선행돼야 함.
- **R4-1 / R1-1 (실용성)**: 장치 예시는 R1-1에서 한 번만. 식(21) 대신 Table 2 값으로 계산(식(21)은 70–90 °C/472 mT에서 16–23 % 오차).
- **R1-2 / R1-8**: Table 3가 조건별 τ_y 기반이라는 명시, 식(21) 잔차, τ_y=0 온도, 3점 보간의 자유도 0 인정은 여기와 같은 문장을 공유.
- **R1-4 (m_p 온도의존)**: m_p(B) 식별 방식·온도 [A1-22]가 밝혀져야 ablation 서술 가능. 한 온도에서 식별해 고정했다면 전이 형상의 온도의존이 τ_y(T)에 강제로 흡수된다는 점을 R1-4·R4-2 양쪽에서 일관되게 인정.

---

## 4. 제출 전 체크리스트

- [ ] A1 프로토콜 사실표 수령 → §2.2.1·Table S0 채움
- [ ] A2-2 n′ 최소값 확인 → "0.7–0.8" 문구 수정 여부 결정
- [ ] A2 지수표·구간별 RMSE·고전단 기울기 결과로 경로 D/R 결정 `[P]`
- [ ] B1 결과(계단 재현성·이력·25 °C 재측정) → `{IF D}`/`{IF R}` 택일
- [ ] B2 결과(4–5 A) → `{IF D}` 문장 유지 여부
- [ ] B3·B4 수치 삽입
- [ ] 데이터시트 대조 공개 여부 `[P]`
- [ ] 신규 참고문헌 4건 서지·내용 확인(A3) 후 번호 부여
- [ ] 초록·결론 표현 교체(§2.3 표) 완료
- [ ] R1-6·R1-2·R1-4·R1-8 답변과 문장 정합 확인
