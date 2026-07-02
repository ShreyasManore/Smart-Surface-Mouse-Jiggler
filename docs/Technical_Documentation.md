# Technical Documentation

This document consolidates the core technical details of the Smart Surface Mouse Jiggler: circuit design, hardware design, working principle, specifications, power characteristics, performance, limitations, and safety notes.

## 1. Circuit Design

The electrical design is intentionally minimal: a single-cell 18650 Li-ion battery, a mechanical SPST ON/OFF switch, and a low-RPM DC gear motor wired in series. There is no onboard regulation, microcontroller, or PWM circuitry in the baseline (v1.0) design — the motor runs directly from battery voltage when the switch is closed.

```
[18650 Battery +] --- [SPST Switch] --- [DC Gear Motor +]
[18650 Battery -] ------------------------ [DC Gear Motor -]
```

See [`hardware/Circuit_Diagram.md`](../hardware/Circuit_Diagram.md) for the full schematic breakdown.

## 2. Hardware Design

The mechanical assembly consists of:
- A rigid base enclosure housing the battery and motor
- A shaft-mounted textured disc positioned flush with the enclosure's top surface
- A cutout or raised lip that keeps the placed mouse centered over the disc

Design priorities were: minimal footprint, motor vibration isolation, and a disc surface with enough texture to register as continuous motion to an optical sensor without being so aggressive that it destabilizes the mouse.

## 3. Working Principle

Refer to [`hardware/Working_Principle.md`](../hardware/Working_Principle.md) for the full operational theory, including why optical sensors register the rotating disc as valid movement.

## 4. Assembly

Refer to [`Assembly_Guide.md`](Assembly_Guide.md) for the complete step-by-step build process.

## 5. Testing

Refer to [`Testing_Report.md`](Testing_Report.md) for full test methodology, environments, and results.

## 6. Specifications

| Parameter | Value |
|---|---|
| Operating Voltage | 3.7 V (nominal, single 18650 cell) |
| Motor Type | Low-RPM DC gear motor |
| Motor Speed | 10–30 RPM (gear-reduced) |
| Current Draw | ~80–150 mA under load (motor-dependent) |
| Enclosure Footprint | ~90 mm x 90 mm x 30 mm (baseline design) |
| Disc Diameter | ~70 mm |
| Switch Type | SPST toggle/slide |

Full specification breakdown in [`hardware/Specifications.md`](../hardware/Specifications.md).

## 7. Power Consumption

At steady-state operation, the motor draws approximately 80–150 mA depending on load and disc friction. With no regulation circuitry, current draw scales directly with battery voltage as it discharges.

## 8. Battery Runtime

A typical 2500–3000 mAh 18650 cell provides an estimated **16–30 hours** of continuous runtime at the measured current draw, before voltage sag begins to noticeably reduce motor RPM. Exact runtime depends on the specific cell capacity and motor selected. See [`Testing_Report.md`](Testing_Report.md) for measured figures.

## 9. Performance

The device reliably prevented OS-level sleep/idle activation across all tested configurations once disc texture and rotation speed were tuned to produce sensor-detectable motion. Performance is sensor-dependent — higher-DPI optical sensors detect the motion more reliably than very low-DPI legacy sensors.

## 10. Limitations

- Requires an optical or laser mouse; purely mechanical (ball) mice are not compatible in the same way
- No speed regulation in the baseline design — motor runs at a fixed RPM set by battery voltage
- Battery life is finite and not user-monitorable without an added indicator (see Future Scope)
- Device does not address keyboard-only inactivity locks in isolation

## 11. Safety Notes

- Use only protected 18650 cells with appropriate holders to prevent short circuits
- Do not leave the device running unattended for multi-day periods without periodic inspection
- Keep the motor and moving disc clear of loose cables or fingers during operation
- Avoid exposing the battery to excessive heat or physical damage
- This device is intended for legitimate productivity use in environments where the user has authority to keep their own workstation active; it should not be used to circumvent monitoring policies without appropriate authorization from the relevant organization
