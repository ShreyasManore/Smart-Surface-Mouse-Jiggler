# Future Improvements

This document outlines the planned roadmap for future hardware revisions beyond the current v1.0 baseline.

## 1. PWM Speed Controller

Add a small potentiometer-controlled PWM circuit to allow users to tune disc rotation speed, compensating for different mouse DPI sensitivities and reducing unnecessary power draw when a slower speed is sufficient.

## 2. TP4056 Charging Module

Integrate a TP4056-based Li-ion charging module with USB-C input to allow safe in-place charging without removing the battery, along with built-in overcharge/overdischarge protection.

## 3. 3D-Printed Enclosure

Replace the baseline enclosure with a designed, 3D-printable housing for a cleaner, more production-like appearance, including snap-fit assembly and a recessed switch guard.

## 4. LED Status Indicators

Add a simple LED to indicate power-on state, and optionally a second LED tied to charging status once the TP4056 module is integrated.

## 5. Battery Percentage Indicator

Add a basic voltage-divider-based battery level indicator (e.g., 3-LED bar graph) to give users visibility into remaining charge without needing a multimeter.

## 6. Adjustable Rotation Speed

Beyond basic PWM control, implement discrete speed presets (Low / Medium / High) selectable via a rotary switch for quick adjustment without fine-tuning a potentiometer.

## 7. Automatic Mouse Detection

Explore a lightweight sensor (e.g., IR proximity or microswitch) to automatically power the motor only when a mouse is detected on the disc, further extending battery life during idle-but-unattended periods.

## 8. Rubber Anti-Slip Surface

Add a rubberized base pad to prevent the enclosure itself from sliding on smooth desk surfaces during motor operation.

## Prioritization

| Improvement | Priority | Complexity |
|---|---|---|
| TP4056 Charging Module | High | Low |
| Rubber Anti-Slip Surface | High | Low |
| LED Status Indicators | Medium | Low |
| PWM Speed Controller | Medium | Medium |
| 3D-Printed Enclosure | Medium | Medium |
| Adjustable Rotation Speed | Low | Medium |
| Battery Percentage Indicator | Low | Medium |
| Automatic Mouse Detection | Low | High |

Contributions toward any of these items are welcome — see [`CONTRIBUTING.md`](../CONTRIBUTING.md).
