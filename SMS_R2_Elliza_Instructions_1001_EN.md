# Email to Elliza — work plan for the Reviewer 4 measurement-cell comment (2026-10-01)

> 발송용 영문 메일. 배경은 `SMS_R2_Response_R4-2_Draft_1001.md` §0 참조. 오전에 보낸 상의 메일(전이 시험)과 별도로, 이번 건은 **지시** 메일임. 날짜는 10/1(목) 기준.

**Subject: SMS-120630 R2 — Reviewer 4 (measurement cell): data checks by Tue 6 Oct, control runs 7–14 Oct**

Dear Elliza,

Following my message this morning, this email sets out the work I need for the second-round revision on one specific point: Reviewer 4's comment that our MRD cell is a "black box" and that the model may be fitting the cell rather than the fluid. Together with Reviewer 1's point 6 on centrifugal migration, this is now the critical path for the revision, so please give it priority over the transfer-test idea from my earlier email (that remains useful, but it comes after this).

I have gone through the manuscript, Table 2 and your instrument decks (12 March, 28 April, 5 June, and the 3D-printing deck) in detail. The ring validation, the data-sheet comparison and the mixing observation in those decks are exactly what the response needs, and they will go into the supplement. My conclusion is that the reviewer is more right than we would like: Section 2.2 gives none of the protocol details a rheologist needs, the ring is not even mentioned in the current text, and our own Table 2 contains features that a careful reader will question (the 71–79 % drop of τ_y from 10 to 90 °C, the single large step between 50 and 70 °C, and a field dependence that becomes much weaker at high temperature). The right answer is not to argue, but to (1) document the protocol completely, (2) put numbers on every cell effect, (3) run a few control measurements on our own instrument, and (4) tone down the "physics" claims. None of this needs a different cell.

I will ask the editor today for a two-week extension (to about 27 October). Please plan on the dates below. If the extension is refused I will tell you at once and we will do Part A only.

**One rule for everything below: report exactly what you find.** If a check comes out against us, that is important information, not a problem to be fixed, and we will state it honestly in the response. Do not adjust, smooth or drop points.

---

## Part A — by Tuesday 6 October (existing data and records only, no instrument time)

### A1. Protocol fact sheet

Please fill in a table with the following, one row each, with the source of each entry (lab notebook, RheoCompass file name, order sheet, manual page):

0. **First, before anything else.** For the 18 flow curves of MRF-132DG in the paper (Table 2, Figures 8–12) and for the MRF-140CG set: were they all measured with the ring in place, and after the mechanical-mixing step was introduced? Give the measurement date for each temperature and field. If any of the published curves were measured without the ring or before the mixing step, tell me the same day, because the response letter rests on this.
1. Rheometer and cell: MCR302 firmware/software version; MRD 170/1T serial; the **rated sample-temperature range of our MRD 170/1T with the Julabo circulator** (check the manual: Peruzzi et al. report a 70 °C limit for their magnetocell; if ours is similar we must justify 80 and 90 °C).
2. Upper plate: confirm the exact geometry code from the order sheet or calibration certificate (the manuscript says "PP20/MRD/T1/P2"; I believe it is "PP20/MRD/TI/P2", titanium with a profiled "P2" surface). Give the profile depth or Ra, and the plate edge thickness (height of the cylindrical side face).
3. Lower plate of the MRD: material (ferromagnetic steel?) and surface finish (smooth or profiled).
4. Ring: inner diameter, outer diameter, height, radial clearance to the 20 mm plate, the print material (name of the resin; confirm it is non-magnetic), how it sits on the lower plate, and how the 400 µL sample is filled and trimmed relative to the plate edge. Please send a simple dimensioned sketch and the photos from the 5 June deck. The response draft has placeholders for exactly these numbers, so send them as a list and I will insert them.
5. Sample handling: the mixing protocol (mixer type, speed, duration) and from which date it was used; loading method; whether a **fresh sample was used at each temperature or the same sample throughout**; and the exact sequence of temperatures and fields with dates.
5a. Ring validation runs (5 June deck, slides 16–20): one version says 40 °C and the 3D-printing deck says 25 °C. Which is correct? Also state the shear-rate range, dwell time and the number of points used in those runs.
6. Off-state pre-shear before each field-on sweep (rate, duration) and the equilibration time at each temperature before the field was applied.
7. Sweep definition: confirm 30 points from 100 to 3000 rpm in 100 rpm steps (linear), ascending only; **dwell time per point** (and whether it was fixed or "steady-state" controlled); total time per sweep. Note: Figures 8–12 show data only to about 2000 s⁻¹ while the text says 3.14×10³ s⁻¹; please confirm what was measured and what was plotted.
8. Number of repeats per condition, and the run-to-run deviation with the ring (restore the figures and tables from our 29 July reply: Fig. A–D, Table A–C, with n stated).
9. Temperature: sensor location (lower plate Pt100?), whether the hood/upper temperature control was used, and whether RheoCompass logged the plate temperature per point (if yes, export the logs for the 3000 rpm points at 10 °C and 90 °C, 472 mT).
10. Magnetic field: where the Hall probe sits, and whether 166/319/472 mT were read **with the sample in the gap or in the empty gap**, at which temperature, and whether the software permeability correction was used. Figure 2 is a perfect straight line through the origin, which usually means an empty-gap or yoke calibration.
11. How m_p(B) was identified: from which data set, at which temperature(s), fitted jointly with τ_y or separately. This is not stated in the manuscript.
12. Why the MRF-140CG tests stopped at about 1151 s⁻¹ and 70 °C (torque limit, normal force, expulsion, heating?).
13. Normal force readings at 472 mT and 3000 rpm, if logged, and the instrument's normal-force limit.
14. Thermal gap compensation: was TruGap or a thermal expansion correction used?

### A2. Diagnostics from the existing raw data

Please compute the following from the raw torque–speed data (not from the WRM-corrected curves) and put each in its own sheet of one Excel workbook, with a short PDF of plots.

a. **n′ for all 18 flow curves**: n′ = d(log M)/d(log γ̇_R) by central differences in log–log, plotted against γ̇_R. Report the minimum value of n′ in each curve and the overall minimum. Then report the actual range of the correction factor (3+n′)/4. The manuscript says "0.7 to 0.8", and 0.7 would mean n′ = −0.2, i.e. torque falling with speed, which a reviewer will read as heating, slip or sample loss. I expect the true range is about 0.75–0.80; please confirm. Also confirm that (3+n′)/4 was applied once, not twice, in the stress calculation.

b. **Field exponent per temperature**: n_B = ln[τ_y(472)/τ_y(319)] / ln(472/319) and the same for 166→319 mT, from Table 2. My values are 0.73 / 0.76 / 0.55 / 0.37 / 0.39 / 0.34 (319→472) and 1.04 / 1.24 / 1.18 / 0.87 / 0.83 / 0.77 (166→319) for 10 / 25 / 50 / 70 / 80 / 90 °C. Please confirm and plot τ_y versus B for each temperature on one graph.

c. **Normalised decay** τ_y(T)/τ_y(25 °C) for each field (my values at 472 mT: 1.08 / 1 / 0.69 / 0.34 / 0.29 / 0.23) and the same for **MRF-140CG** from your re-identification. Put both fluids on one plot. Also send the Doolittle a and b you obtained for 140CG (this was one of the two checks in my morning email).

d. **RMSE by shear-rate window** for all three models (modified BP, Bingham-T, HB-T), pooled over the 18 conditions: 100–500, 500–1150 and 1150–3140 s⁻¹. Also reconcile Table 5 (733 Pa for 132DG at ≤1151 s⁻¹, 10–70 °C) with Table 3 (483 Pa). My reading is that essentially all of the modified BP's advantage over Bingham-T comes from the 100–500 s⁻¹ window; please check.

e. **High-shear slope under field**: fit τ = τ_0 + η_hs γ̇ over 1500–3140 s⁻¹ (or the last 15 points) for all 18 conditions. Tabulate η_hs(B,T) and η_hs(B,T)/η_hs(B,25 °C), and overlay the latter on the Doolittle curve η_p(T)/η_p(25 °C). Report also any condition where η_hs is negative or decreasing with rate.

f. **Sub-100 s⁻¹ data**: for 90 °C / 472 mT (and 70 °C / 472 mT), what is the maximum stress recorded below 100 s⁻¹ in the raw sweep, compared with the identified τ_y of 4147 Pa (and 6273 Pa)?

g. **Off-state viscosity check**: if we have off-state data at high shear rate at 40 °C, give the slope over 800–1200 s⁻¹ and compare with the datasheet value of 0.102 Pa·s. If not, note that we only have the 100 s⁻¹ temperature ramp.

h. **Closed-form Eq. (21) versus Table 2**: tabulate the difference for all 18 conditions (I get RMSE 644 Pa, +23 % at 70 °C/472 mT, −16 % at 90 °C/472 mT), the temperature at which Eq. (21) gives τ_y = 0 (I get 106 / 112 / 120 °C for 472 / 319 / 166 mT), and the coefficients of Eqs. (17), (19) and (20) to at least four significant figures. Please also confirm that the metrics in Table 3 were computed with the 18 per-condition τ_y values, not with Eq. (21).

i. **Datasheet comparison**: the 5 June deck already has this for the validation runs (H = 18.18 / 45.88 / 79.65 kA/m; 5.10 / 13.24 / 21.90 kPa against the datasheet 4.64 / 13.77 / 23.47 kPa for MRF-132DG, and 7.51 / 17.04 / 27.63 against 7.46 / 18.27 / 26.40 kPa for MRF-140CG). Please (1) state exactly how τ_y was defined in that comparison (which fit, which shear-rate range), (2) redo the comparison with the Table 2 values at 25 °C (6073 / 13618 / 18324 Pa) using the same B→H conversion, and (3) explain the difference between the two sets (definition, sample batch, date). I will decide which set goes into the response after seeing both.

j. **Viscous heating estimate sheet**: for each of the 18 conditions, torque M at 3000 rpm, power P = M·ω, mean dissipation P/V with V = 0.314 mL, and the estimate ΔT = q h²/(8k) with k = 0.5 and 1.0 W m⁻¹ K⁻¹. I get about 13 W and 8–16 K for 10 °C / 472 mT. Include the dwell time from A1-7.

### A3. Documents and literature

Please obtain PDFs and send me a half-page note on each (what they measured, which cell, what they found), because I could not access the full texts this week:

- Laun, Schmidt, Gabriel, Kieburg 2008, Rheol. Acta 47:1049 (radial flux-density profile of the single-gap MRD; apparent stress overestimated near the rim).
- Laun, Gabriel, Kieburg 2010, J. Rheol. 54:327 (twin-gap magnetorheometer).
- Laun, Gabriel, Kieburg 2011, Rheol. Acta 50:141 (wall material and roughness; transmissible stress on titanium vs steel plates).
- Morillas, Yang, de Vicente 2018, J. Rheol. 62:1485 (double-gap plate–plate magnetorheology).
- Jönkkäri et al. 2012 [37]: re-read and tell me exactly what they found about (i) smooth vs profiled non-magnetic plates and (ii) gap height 0.25–1.0 mm. We cite this paper, so we must get it right.
- Lv et al. 2023 [29]: which rheometer and cell did they use? If it is an Anton Paar MRD with PP20, we cannot call it a "different instrument".
- Ocalan & McKinley 2013 [50]: their table of temperature sensitivities of the yield stress from the literature and their own value; Zschunke et al. 2005 [23]: the size of the yield-stress drop between 20 and 80–90 °C; McKee et al. 2018 [22]: the statement that yield stress is unchanged with temperature.
- Anton Paar: the MRD 170/1T manual pages on the Hall probe position, the "with sample" flux calibration, the rated temperature range, and the meaning of the "TI" and "P2" codes.

---

## Part B — instrument time, 7–14 October (prepare the procedures now; run only after I confirm the extension)

All runs with MRF-132DG from a **fresh bottle shaken as in the original work**, same plate, same ring, same gap of 1 mm, same 30-point sweep, unless stated. Record torque, normal force, plate temperature and Hall reading at every point. Deliver raw files plus one summary sheet per item by **Friday 16 October**.

**B1 (highest priority). Fresh-sample temperature sequence at 472 mT.**
Load a fresh sample. Sequence 25 → 40 → 50 → 60 → 70 → 90 → 25 °C. At each temperature: 60 s off-state pre-shear at 100 s⁻¹, equilibrate for the same time as in the original protocol, field on, ascending sweep, then immediately a descending sweep. Then repeat the 70 and 90 °C points with a second fresh loading. Deliver: τ_y per temperature (same identification as before), ascending/descending difference in % at each temperature, repeat-to-repeat difference, the final 25 °C curve versus the initial one, and whether the drop between 50 and 70 °C is still a single step once 40 and 60 °C are included.

**B2. Field extension at 25 and 90 °C.**
At 4 A and, if the cell and power supply allow it, 5 A (record the Hall reading; check the MRD current limit first), ascending sweep at 25 °C and at 90 °C with fresh samples. Deliver τ_y versus B at both temperatures on one plot together with the 166/319/472 mT values. The question is whether τ_y keeps rising with field at 90 °C or flattens; a flattening at 90 °C but not at 25 °C would indicate a wall-limited stress, which we would then have to say.

**B3. Heating check.**
At 10 °C and at 25 °C, 472 mT: after the normal pre-shear and equilibration, go directly to 3000 rpm and hold for 60 s, logging torque and plate temperature every second. Deliver the torque drift in % over 60 s and the temperature trace. Watch the normal force; stop if it approaches the instrument limit.

**B4. Ring checks.**
(a) Ring on/off at 25 °C, off-state and 166 mT, speeds up to 500 rpm only (the unconfined sample is still retained at these speeds): one sweep with the ring, one without, same filling. Deliver the torque difference in % point by point. This bounds the extra torque from fluid at the plate edge.
(b) Ring retention at the paper's extreme conditions: with the ring, 472 mT, the standard 30-point sweep to 3000 rpm at 25 °C and again at 90 °C, each with a fresh loading. Photograph the cell before and after each sweep, weigh the sample if practical, and note any leakage under or over the ring. This can be combined with the 60 s hold of B3. The validation in the 5 June deck stops at 1000 s⁻¹, and the reviewer will ask about 3000 rpm.

**B5 (only if a smooth PP20/MRD/TI plate is available in the lab).** Smooth versus profiled plate at 25 and 90 °C, 472 mT.

**B6 (optional, if time permits).** Stress-controlled static yield stress (stress ramp) at 25 and 90 °C, 472 mT, to compare with the high-shear intercept.

**Do not run a gap-height variation test.** In the MRD the gap changes the magnetic circuit and the radial field profile (Jönkkäri et al. 2012), so a gap test cannot separate slip from field effects, and proposing it would weaken our response.

Before the 80 and 90 °C runs, please check the cell's rated temperature range (A1-1). If our configuration is rated below 90 °C, tell me before running.

---

## Deliverables and reporting

- One Excel workbook for Part A (sheets A2a–A2j), one for Part B, raw RheoCompass exports, and a short PDF with the plots. File names with the date.
- The ring numbers (item A1-4), the validation conditions (A1-5a) and the mixing protocol (A1-5) go straight into the response letter and the new Section 2.2 text, so please send those three as soon as they are ready, before the rest of Part A.
- A two-line status email at the end of each working day (what was done, what is blocked). If any item is impossible or needs clarification, ask the same day rather than guessing.
- Please keep a lab notebook record for every Part B run (sample loading time, pre-shear, equilibration, field-on time), since this is exactly what the reviewer says is missing.

I know this is a lot in a short time. The reviewer's comment is fixable, and the fastest way to fix it is to show, with our own numbers, that we understand our instrument. Thank you for your careful work on this.

Best regards,
Jong-Seok Oh
