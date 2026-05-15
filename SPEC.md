# DEEPSTILL™ MAXILLA · v0.1 · Full Specification

**Status:** R&D · pre-prototype · paper design only
**Date:** May 15, 2026
**Family:** DEEPSTILL™ (sister to v1.4 LATTICE+HEART)

---

## 0. One-line definition

A removable upper-jaw appliance carrying the DEEPSTILL frequency stack into the oral cavity via palatal bone conduction, with a sensor platform measuring biosignals from the highest signal-density surface on the body.

---

## 1. The thesis

### 1.1 Bone over air
The upper palate (maxilla) is one of the most efficient bone-conduction surfaces on the human body — closer to the cochlea than the mastoid, the wrist, or any external speaker. Frequencies delivered into the maxilla reach the inner ear directly, bypassing the eardrum. This is established physics (SoundBite Hearing System, FDA-cleared 2011).

### 1.2 Sense where it's still
The mouth doesn't swing through the air like a wrist. Sensors mounted in a custom-fit appliance may produce cleaner readings than skin-surface wearables for several modalities:
- **PPG (photoplethysmography)** — dense gingival capillary bed
- **Temperature** — sublingual is the clinical reference for non-invasive core temp
- **Strain (bite force)** — occlusal sensing is standard in dental research
- **IMU (kinematics)** — jaw-mounted accelerometer/gyro for sleep posture, chewing, REM micro-movements

### 1.3 Always there
Eight hours of nightly wear, zero cognitive cost. For the existing denture-wearer or nightguard user, the form factor is already adopted. For the Brotherhood operator running Keyholder V5, it becomes the LAYER_1 and LAYER_2 delivery vector — bone-conducted entrainment that doesn't require headphones.

---

## 2. Who it's for

| Population | Form factor | Adoption barrier |
|---|---|---|
| Existing denture wearers | Full upper denture with embedded module | None — they already wear one |
| Nightguard / retainer users | Custom-fit night appliance | Minimal — replaces what they have |
| Brotherhood / Keyholder V5 operators | Custom retainer-style night appliance | Custom fitting required |

---

## 3. Architecture overview

Five-layer breakdown:

1. **HARDWARE layer** — 8 subsystems (see `HARDWARE.md`)
2. **FIRMWARE layer** — embedded microcontroller, signal processing, BLE radio (off-device data sync)
3. **PROTOCOL layer** — DEEPSTILL frequency stack delivered via palatal BC (see `PROTOCOLS.md`)
4. **ÆSN layer** — symbolic chord emission for KDL/journaling integration (see `AESN.md`)
5. **SAFETY / LEDGER layer** — GREEN/AMBER/NEVER discipline (see `SAFETY.md`, `LEDGER.md`)

---

## 4. The closed-loop killer feature

**HEART-256 + 0.1Hz HRV-resonant AM**, delivered through the maxilla, gated by live PPG from the gum array.

- The gum PPG reads HRV in real time
- The 0.1Hz amplitude modulation of the 256Hz bone-conducted carrier is paced to the user's actual HRV
- Vagal tone increases via respiratory sinus arrhythmia coupling (validated mechanism — HeartMath / McCraty)
- This loop closes inside the mouth, on the body, without external hardware

No other consumer or prosumer device does this. It is the strongest GREEN-lane feature.

---

## 5. The honest limits

This is a paper design. No prototype exists. The path from spec to wearable involves:

1. Component validation on a bench rig (months)
2. Biocompatibility testing per ISO 10993 (months, costly)
3. Custom-fit prosthodontist partnership for fitting (per-user)
4. FDA wellness device positioning (paperwork, not approval)
5. FCC Part 15 modular certification (~$1,500 if using pre-certified BLE module)
6. Long-duration human studies for any AMBER claims

This repo documents the design. It does not promise a product.

---

## 6. Critical safety boundaries (NEVER list)

The device shall NEVER claim to:
- Cure, treat, or prevent any disease
- Reverse aging
- Repair DNA
- Replace medical care for sleep apnea, TMJ, bruxism, or any clinical condition
- Substitute for prescribed CPAP, oral appliance therapy, or dental treatment

See `SAFETY.md` and `LEDGER.md` for the full lane breakdown.

---

## 7. Lineage

| Predecessor | Date | Contribution |
|---|---|---|
| DEEPSTILL™ v1.0 | Apr 23, 2026 | 6-layer frequency stack (EARTH/ALPHA/GAMMA/HEART/PHI/NATURE) |
| DEEPSTILL™ v1.4 | Apr 23, 2026 | LATTICE (Görbitz 2015) + HEART (256Hz + 0.1Hz AM) protocols |
| Nike Protocol v2.2 | Apr 17, 2026 | Three Rings architecture, Keyholder V5, KDL v2.0 |
| DNA Evolution Forge v2.0 | Apr 17, 2026 | Champion SN-DNA-005 WGMC dual-323 keystone |
| Lattice v1.0 | Görbitz 2015 | 323–880 Hz AA crystal frequency fingerprint |

---

*v0.1 · last updated May 15, 2026*
