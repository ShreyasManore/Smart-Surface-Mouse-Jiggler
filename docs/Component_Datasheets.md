# Component Datasheets

Summarized key specifications for the core components used in this project. Consult manufacturer datasheets for the specific part numbers you source, as parameters vary between suppliers.

## 18650 Li-ion Battery

| Parameter | Typical Value |
|---|---|
| Nominal Voltage | 3.7 V |
| Capacity | 2200–3500 mAh (model-dependent) |
| Max Continuous Discharge | 2A–10A (model-dependent) |
| Chemistry | Lithium-ion (Li-ion) |
| Charge Cutoff Voltage | 4.2 V |
| Discharge Cutoff Voltage | 2.5–3.0 V |

**Note:** Always use a protected cell with built-in overcurrent/overvoltage protection for hobbyist builds.

## DC Gear Motor (Low RPM)

| Parameter | Typical Value |
|---|---|
| Rated Voltage | 3–6 V DC |
| No-Load Speed | 10–60 RPM (gear ratio dependent) |
| Stall Current | 200–400 mA (model-dependent) |
| Gear Ratio | Commonly 1:48 to 1:100 for this application |
| Shaft Type | D-shaft or round, 3–5 mm diameter |

## SPST ON/OFF Switch

| Parameter | Typical Value |
|---|---|
| Type | Single Pole Single Throw (toggle or slide) |
| Rated Current | 1–3 A at low voltage |
| Rated Voltage | Up to 12–24 V DC (well above project requirement) |

## Battery Holder

| Parameter | Typical Value |
|---|---|
| Cell Compatibility | Single 18650 |
| Contact Material | Nickel-plated spring contacts |
| Mounting | Screw-mount or adhesive-back, model-dependent |

## Connecting Wire

| Parameter | Typical Value |
|---|---|
| Gauge | 22–26 AWG hookup wire |
| Insulation | PVC, rated for at least 30V |

## Rotating Disc (Custom / Fabricated)

Not a standard off-the-shelf part — fabricated from a rigid, lightweight material (e.g., ABS, acrylic, or dense cardboard for prototyping) with a matte, low-contrast textured top surface. See [`Design_Explanation.md`](Design_Explanation.md) for texture selection rationale.

## Enclosure

Fabricated or 3D-printed housing; refer to [`Future_Improvements.md`](Future_Improvements.md) for the planned 3D-printable revision.
