# Email to Elliza — protocol fact sheet for the Reviewer 4 measurement-cell comment (2026-10-01)

> 발송용 영문 메일. 배경은 `SMS_R2_Response_R4-2_Draft_1001.md` §0 참조. 오전에 보낸 상의 메일(전이 시험)과 별도로, 이번 건은 **지시** 메일임. 날짜는 10/1(목) 기준.
> **10/1 결정: 엘리자에게는 A1(프로토콜 사실표)만 요청함.** 기존 초안의 A2(원시데이터 진단)·A3(문헌 확인)·Part B(대조실험) 항목은 보류. 필요해지면 git 이력(커밋 4749bf8)에서 복원해 별도 메일로 보냄.

**Subject: SMS-120630 R2 — Reviewer 4 (measurement cell): protocol fact sheet needed by Tue 6 Oct**

Dear Elliza,

Following my message this morning, this email asks for one specific piece of work for the second-round revision: a complete fact sheet of our measurement protocol. Reviewer 4 writes that our Section 2.2 treats the MRD cell as a "black box" and that the model may be fitting the cell rather than the fluid. The core of our answer will be to document, in full, what was controlled and how, and to put the ring validation and the data-sheet comparison that you already prepared into the supplement.

I have read your instrument-checking decks (12 March, 28 April, 5 June) and the 3D-printing deck. They contain most of what we need. What is missing is the set of facts below, written down with their sources, so that the new Section 2.2 and the response letter can be filled in. For now I am not planning additional measurements; if the fact sheet shows a gap we cannot close with existing records, we will discuss it.

**One rule: report exactly what the records say.** If something was not recorded, write "not recorded" rather than an estimate. If a published curve turns out to have been measured under different conditions from the rest, tell me the same day.

---

## A1. Protocol fact sheet — by Tuesday 6 October

Please fill in a table with the following, one row each, with the source of each entry (lab notebook page, RheoCompass file name, order sheet, manual page, photo).

0. **First, before anything else.** For the 18 flow curves of MRF-132DG in the paper (Table 2, Figures 8–12) and for the MRF-140CG set: were they all measured with the ring in place, and after the mechanical-mixing step was introduced? Give the measurement date for each temperature and field. If any of the published curves were measured without the ring or before the mixing step, tell me the same day, because the response letter rests on this.
1. Rheometer and cell: MCR302 firmware/software version; MRD 170/1T serial; the **rated sample-temperature range of our MRD 170/1T with the Julabo circulator** (check the manual: Peruzzi et al. report a 70 °C limit for their magnetocell; if ours is similar we must justify 80 and 90 °C).
2. Upper plate: confirm the exact geometry code from the order sheet or calibration certificate (the manuscript says "PP20/MRD/T1/P2"; I believe it is "PP20/MRD/TI/P2", titanium with a profiled "P2" surface). Give the profile depth or Ra, and the plate edge thickness (height of the cylindrical side face).
3. Lower plate of the MRD: material (ferromagnetic steel?) and surface finish (smooth or profiled).
4. Ring: inner diameter, outer diameter, height, radial clearance to the 20 mm plate, the print material (name of the resin; confirm it is non-magnetic), how it sits on the lower plate, and how the 400 µL sample is filled and trimmed relative to the plate edge. Please send a simple dimensioned sketch and the photos from the 5 June deck. The response draft has placeholders for exactly these numbers, so send them as a list and I will insert them.
5. Sample handling: the mixing protocol (mixer type, speed, duration) and from which date it was used; loading method; whether a **fresh sample was used at each temperature or the same sample throughout**; and the exact sequence of temperatures and fields with dates.
5a. Ring validation runs (5 June deck, slides 16–20): one version says 40 °C and the 3D-printing deck says 25 °C. Which is correct? Also state the shear-rate range, dwell time and the number of points used in those runs, and how the yield stress in the data-sheet comparison (slides 24–25) was defined (which fit, which shear-rate range).
6. Off-state pre-shear before each field-on sweep (rate, duration) and the equilibration time at each temperature before the field was applied.
7. Sweep definition: confirm 30 points from 100 to 3000 rpm in 100 rpm steps (linear), ascending only; **dwell time per point** (and whether it was fixed or "steady-state" controlled); total time per sweep. Note: Figures 8–12 show data only to about 2000 s⁻¹ while the text says 3.14×10³ s⁻¹; please confirm what was measured and what was plotted.
8. Number of repeats per condition, and the run-to-run deviation with the ring (restore the figures and tables from our 29 July reply: Fig. A–D, Table A–C, with n stated).
9. Temperature: sensor location (lower plate Pt100?), whether the hood/upper temperature control was used, and whether RheoCompass logged the plate temperature per point (if yes, export the logs for the 3000 rpm points at 10 °C and 90 °C, 472 mT).
10. Magnetic field: where the Hall probe sits, and whether 166/319/472 mT were read **with the sample in the gap or in the empty gap**, at which temperature, and whether the software permeability correction was used. Figure 2 is a perfect straight line through the origin, which usually means an empty-gap or yoke calibration. Also state how the H values in the 5 June deck (18.18 / 45.88 / 79.65 kA/m for MRF-132DG) were obtained from B.
11. How m_p(B) was identified: from which data set, at which temperature(s), fitted jointly with τ_y or separately. This is not stated in the manuscript.
12. Why the MRF-140CG tests stopped at about 1151 s⁻¹ and 70 °C (torque limit, normal force, expulsion, heating?).
13. Normal force readings at 472 mT and 3000 rpm, if logged, and the instrument's normal-force limit.
14. Thermal gap compensation: was TruGap or a thermal expansion correction used?

---

## Deliverables

- One table (Excel or Word) with the 16 rows above, each with its source, plus the ring sketch and photos, and the restored 29 July ring figures and tables.
- Please send items 0, 4, 5 and 5a first, as soon as they are ready, since they go straight into the response letter and the new Section 2.2 text. The rest can follow by Tuesday.
- A short note on Friday 3 October saying what is still missing and why.

I know this comes on top of the other revision work. The reviewer's comment is answerable, and the fastest way to answer it is to show, with our own records, that we understand our instrument. Thank you for your careful work on this.

Best regards,
Jong-Seok Oh
