# Design Explanation

## Design Philosophy

The core design constraint driving this project was **zero software footprint**. Any solution requiring drivers, USB HID emulation, or background processes can be blocked by IT security policy or flagged as an unauthorized device. A purely mechanical approach sidesteps this entirely: from the host computer's perspective, the input is indistinguishable from a person nudging the mouse.

## Why a Rotating Disc?

Several actuation methods were considered before settling on a rotating textured disc:

| Method | Verdict |
|---|---|
| Linear cam/lever nudging the mouse directly | Rejected — larger footprint, more mechanical wear on the mouse itself |
| Vibration motor under the mouse | Rejected — inconsistent sensor detection, mouse can "walk" off position |
| **Rotating textured disc under the mouse** | **Selected** — compact, contained motion, reliable optical detection |
| Servo-driven mouse-arm actuator | Rejected — higher complexity and cost for no functional benefit |

The rotating disc keeps all motion contained within a small, fixed radius, so the mouse never physically drifts away from its working position — a common failure mode of vibration-based approaches.

## Disc Texture Selection

Optical mouse sensors track relative motion by comparing successive frames of the surface beneath them. A perfectly smooth, glossy, or uniformly patterned disc can under-trigger the sensor. Testing showed that a **light matte texture with subtle non-repeating variation** (e.g., fine sandpaper-grade texture or a printed low-contrast speckle pattern) produced the most consistent tracking across different mouse DPI settings.

## Motor Selection Rationale

A low-RPM DC gear motor was chosen over a standard high-speed DC motor because:
- Lower RPM reduces vibration and audible noise
- Gear reduction provides adequate torque at low current draw
- Slower disc rotation is sufficient to register as continuous motion — high speed is unnecessary and wastes battery capacity

## Simulation and Validation Notes

Prior to final assembly, motor speed and disc diameter combinations were evaluated to identify the RPM range that reliably registered as sustained motion across multiple optical mouse models, without causing erratic or unrealistically fast cursor jumps that some anti-cheat or activity-monitoring software might flag as non-human input.

![Simulation](../images/simulation.png)

## Enclosure Design Considerations

The enclosure was designed to:
- Fully contain the motor and battery, exposing only the disc surface and switch
- Provide a stable, non-slip base
- Allow the mouse to sit flush and centered over the disc without additional alignment aids

Future enclosure iterations (3D-printed) are discussed in [`Future_Improvements.md`](Future_Improvements.md).
