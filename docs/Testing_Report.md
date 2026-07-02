# Testing Report

## Objective

Validate that the Smart Surface Mouse Jiggler reliably prevents host computer sleep/idle activation across a range of mouse models and operating systems, and characterize its electrical and mechanical performance.

## Test Environment

| Parameter | Detail |
|---|---|
| Host Operating Systems Tested | Windows 11, Windows 10, macOS (Ventura-class), Ubuntu 22.04 LTS |
| Mouse Models Tested | 3 standard optical mice (varying DPI: 800, 1600, 3200) |
| Battery Used | Single-cell 18650, 2600 mAh rated capacity |
| Ambient Conditions | Room temperature, standard indoor lighting |

## Test 1 — Sleep Prevention Reliability

**Method:** Set OS sleep timeout to 2 minutes. Place device under mouse, power on, and monitor for sleep/lock activation over a 6-hour continuous session.

**Result:** No sleep or lock activation occurred across all OS/mouse combinations after disc texture and motor speed were tuned. Prior to tuning, the lowest-DPI mouse (800 DPI) occasionally failed to register motion; this was resolved by adjusting disc texture contrast.

## Test 2 — Cursor Movement Characteristics

**Method:** Record on-screen cursor behavior while the device operates.

**Result:** Cursor exhibited small, continuous, low-amplitude drift consistent with genuine incidental mouse contact — not large erratic jumps.

## Test 3 — Current Draw Measurement

**Method:** Measure steady-state current draw with a multimeter in series with the battery.

**Result:** Measured current draw ranged from **95 mA to 140 mA** depending on motor load and disc friction, consistent with the estimated range in [`Technical_Documentation.md`](Technical_Documentation.md).

## Test 4 — Battery Runtime

**Method:** Full discharge test from a fully charged 2600 mAh cell under continuous operation.

**Result:** Measured runtime was approximately **18.5 hours** of continuous operation before motor speed visibly degraded due to voltage sag.

## Test 5 — Noise and Vibration

**Method:** Subjective assessment in a quiet office environment, plus sound level check at 1 meter distance.

**Result:** Operation was subjectively "quiet" — comparable to a laptop cooling fan at low speed. No perceptible vibration transmitted to the desk surface.

## Test 6 — Long-Duration Stability

**Method:** 48-hour intermittent operation cycle (device power-cycled every 6 hours) to check for thermal or mechanical degradation.

**Result:** No overheating observed. Motor and gearbox showed no audible degradation. Disc mounting remained secure with no wobble developing over the test period.

## Summary of Results

| Test | Result |
|---|---|
| Sleep prevention reliability | Pass (all configurations, post-tuning) |
| Cursor movement realism | Pass |
| Current draw | 95–140 mA |
| Battery runtime | ~18.5 hours (2600 mAh cell) |
| Noise/vibration | Low, office-appropriate |
| Long-duration stability | Pass (48-hour test) |

## Known Failure Modes

- Very low-DPI (600 and below) mice may require additional disc texture contrast tuning
- Reduced motor RPM under low battery voltage can eventually fall below the reliable-detection threshold near end of battery life

See [`Future_Improvements.md`](Future_Improvements.md) for planned mitigations, including PWM speed regulation.
