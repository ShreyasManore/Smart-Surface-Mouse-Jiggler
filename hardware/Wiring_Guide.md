# Wiring Guide

## Wiring Overview

This is a simple two-wire-per-connection series circuit. No polarity-sensitive logic components are present, but correct polarity is still recommended for predictable motor rotation direction.

## Connection Table

| From | To | Wire Color (Suggested) |
|---|---|---|
| Battery Holder (+) | Switch Terminal A | Red |
| Switch Terminal B | Motor Terminal (+) | Red |
| Motor Terminal (-) | Battery Holder (-) | Black |

## Step-by-Step Wiring

1. Cut two lengths of hookup wire, approximately 8–10 cm each, one red and one black.
2. Strip approximately 5mm of insulation from each end of both wires.
3. Solder the red wire between the battery holder's positive terminal and one terminal of the switch.
4. Solder a second red wire segment from the switch's remaining terminal to the motor's positive lead.
5. Solder the black wire directly between the motor's negative lead and the battery holder's negative terminal.
6. Cover all exposed solder joints with heat-shrink tubing and apply heat evenly to seal.
7. Perform a continuity check with a multimeter before inserting the battery, to confirm no shorts are present.

## Pre-Power Checklist

- [ ] No exposed conductor at any joint
- [ ] Switch toggles cleanly between open and closed circuit states
- [ ] Continuity confirmed end-to-end when switch is ON
- [ ] No continuity when switch is OFF
- [ ] Battery holder polarity matches wiring polarity

## First Power-On

1. Insert the battery with correct polarity.
2. Flip the switch ON briefly and confirm smooth motor rotation.
3. Flip OFF and inspect all joints for excessive heat before proceeding to enclosure assembly.

For the full mechanical build process, return to [`docs/Assembly_Guide.md`](../docs/Assembly_Guide.md).
