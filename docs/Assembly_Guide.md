# Assembly Guide

This guide walks through assembling the Smart Surface Mouse Jiggler from individual components to a finished, working unit.

## Prerequisites

- All components listed in [`hardware/Bill_of_Materials.md`](../hardware/Bill_of_Materials.md)
- Basic tools: soldering iron, wire strippers, hot glue gun or small screws, screwdriver
- A well-ventilated workspace with a non-conductive work surface

## Safety First

- Ensure the battery is not connected while soldering any wiring
- Double-check polarity before making any solder joints
- Work in a well-lit area with the enclosure secured, not held in your hand, while cutting or drilling

## Step 1 — Prepare the Enclosure

1. Mark and cut/drill the mounting points for the motor shaft, switch, and battery holder inside the enclosure base.
2. Dry-fit all components before permanently securing anything.

## Step 2 — Mount the Motor

1. Secure the DC gear motor to the internal mounting bracket, ensuring the output shaft is centered and perpendicular to the top surface cutout.
2. Confirm the shaft can rotate freely with no obstruction.

## Step 3 — Attach the Rotating Disc

1. Press-fit or secure the textured disc onto the motor shaft.
2. Verify the disc sits flush with (or very slightly recessed from) the enclosure's top surface, with no wobble during manual rotation.

## Step 4 — Wire the Circuit

1. Connect the battery holder's positive terminal to one terminal of the ON/OFF switch.
2. Connect the switch's other terminal to the motor's positive lead.
3. Connect the motor's negative lead directly to the battery holder's negative terminal.
4. Insulate all solder joints with heat-shrink tubing or electrical tape.

Refer to [`hardware/Wiring_Guide.md`](../hardware/Wiring_Guide.md) for the annotated wiring diagram.

## Step 5 — Mount the Switch

1. Secure the switch into its enclosure cutout so it is accessible from the outside.
2. Confirm it toggles smoothly and makes reliable contact in both positions.

## Step 6 — Insert the Battery

1. Insert the 18650 cell into the battery holder, observing correct polarity.
2. Confirm the holder retains the cell securely with no rattling.

## Step 7 — Close and Secure the Enclosure

1. Route all wiring neatly to avoid contact with the rotating disc or motor shaft.
2. Close the enclosure and secure with screws or fasteners as designed.

## Step 8 — Functional Test

1. Flip the switch ON and confirm the disc rotates smoothly at a steady speed.
2. Place an optical mouse on the disc and confirm on-screen cursor movement is registered.
3. Flip the switch OFF and confirm the motor stops immediately.

## Step 9 — Final Inspection

- Check for any exposed wiring or sharp edges
- Confirm the enclosure sits flat and stable on a desk surface
- Re-test for at least 10 minutes of continuous operation before regular use

Assembly complete. Proceed to [`Testing_Report.md`](Testing_Report.md) for the full validation methodology used on the reference build.
