# DEEPSTILL™ MAXILLA · Safety Analysis

**This document is the complete record of health concerns identified for DEEPSTILL™ MAXILLA v0.1, ranked by severity. It is not a regulatory submission. It is the honest internal map of what must be solved before any human ever wears this.**

---

## CATASTROPHIC · must be engineered out before human wear

### 1. Battery in the mouth
LiPo rupture inside the oral cavity is a chemical burn, fire, and aspiration event simultaneously.

**Mitigations:**
- Solid-state battery only (no liquid electrolyte) OR
- Pouch cell in fully hermetic medical-grade housing with redundant thermal cutoffs OR
- Inductive power through the cheek (no on-board battery)

The Apollo Neuro / Sensate playbook does not apply here — those sit on skin, not mucosa, and are not swallowable.

### 2. Aspiration / choking
Any piece that dislodges during sleep could enter the airway.

**Mitigations:**
- Mandatory custom fit (no one-size-fits-all)
- Tethers or fail-safe geometry that cannot enter the trachea
- "Component shed test" — if this falls off at 3 a.m. while supine, what happens?

### 3. Vagal cardiac event
The pharyngeal vagal stim pad (AMBER subsystem) sits near nerves controlling heart rate. Inappropriate stim may cause bradycardia, syncope, asystole.

**Mitigations:**
- Hardware-locked OFF in v0.1
- Absolute contraindications: pacemaker, ICD, history of arrhythmia, vasovagal syncope
- Enabling requires v0.2+ with cardiac co-monitoring on the same device and physician oversight

---

## MODERATE · standard medical-device territory

### 4. Biocompatibility / leaching
Oral mucosa absorbs faster than skin. Solder flux residue, plasticizers, resin monomers are in the bloodstream within minutes.

**Mitigation:** Full ISO 10993-1 panel — cytotoxicity, sensitization, irritation, sub-chronic toxicity, genotoxicity. All wet-zone components encapsulated in medical-grade silicone or PEEK.

### 5. Microbial colonization
Mouth bacteria + device crevices = biofilm → gingivitis, periodontitis, candidiasis, halitosis, bacteremia in immunocompromised users.

**Mitigations:**
- Daily ultrasonic-bath compatible cleaning
- Full disassembly or zero-crevice design
- Antimicrobial silver-ion silicone surfaces

### 6. Occlusal force damage
Nocturnal grinders generate 200–300+ lbs of force. Brittle components in the bite path will be crushed.

**Mitigation:** Nothing fragile in the occlusal plane. Sensors in palate vault and lingual surfaces only.

### 7. Sleep-disordered breathing
A foreign body in the mouth alters airway dynamics. May exacerbate or trigger OSA in users with thick necks, retrognathia, or borderline OSA.

**Mitigation:** Pre-screening home sleep test for any user above moderate risk profile.

### 8. Bone-conduction overexposure
Bone-conducted audio can cause sensorineural hearing damage at high amplitudes. Long-duration low-frequency bone vibration (THETA-6, HEART-256) is not characterized at the dose levels and frequencies the protocol stack uses.

**Mitigations:**
- Hard firmware amplitude ceiling
- Vestibular-symptom auto-stop logic
- NIOSH-style dose limits

### 9. Galvanic / electrochemical
Wet conductive environment + dissimilar metals + electronics = galvanic currents through tissue. Patients with metal restorations may develop oral galvanism — burning, metallic taste, mucosal irritation.

**Mitigation:** All metallic contacts gold-plated or titanium. No exposed copper, nickel, or steel.

---

## LONG-TERM UNKNOWNS · honest about what we don't know

### 10. Years of nightly bone-conducted entrainment
Decades of 8-hours-per-night low-amplitude vibration through the skull. No human dataset exists. The vestibular system is mechanically coupled. Sub-clinical chronic exposure effects on balance, hearing thresholds, sleep architecture are unstudied.

### 11. Years of mouth-cavity BLE radio
SAR limits are designed for phone-against-head exposure. 8 hours nightly at the palate is a different exposure profile.

**Mitigation:** Minimize transmit duty cycle. Prefer offline data with morning sync only.

### 12. Orthodontic / dentoalveolar drift
Anything worn against teeth 8 hours nightly applies force. Even sub-orthodontic forces over years cause drift.

**Mitigation:** Periodic dental check-ups required. Device fit re-verified at 6-month intervals.

---

## CONTRAINDICATED POPULATIONS · the device's NEVER-FOR list

Add to v0.2 artifact:

- Anyone under 18 (developing palate, dentition still erupting)
- Pacemaker, ICD, or implanted neurostimulator
- History of cardiac arrhythmia or vasovagal syncope
- Severe periodontitis or active oral infection
- Untreated moderate-to-severe sleep apnea
- Diabetics with peripheral neuropathy (cannot feel pressure damage)
- Pregnancy (no fetal safety data)
- Active anticoagulation therapy with mucosal bleeding risk
- Recent oral surgery or implants (< 6 months)
- Immunocompromised states (transplant, chemo, advanced HIV)
- Known allergy to silicone, methacrylate resin, or device materials

---

## v0.2 update requirements

Three concrete updates the artifact must carry by v0.2:

1. **Hardware-lock the AMBER pad.** Pharyngeal vagal stim is firmware-disabled in v0.1, hardware-disconnected in v0.2 unless cardiac co-monitoring lands.
2. **Expand the LEDGER tab** with a SAFETY section parallel to GREEN/AMBER/NEVER — every hazard above with its mitigation beside it.
3. **Add a SCREENING tab** with pre-fitting questionnaire flagging contraindications. No fitting without it.

---

*v0.1 safety record · May 15, 2026 · honest record of what must be solved*
