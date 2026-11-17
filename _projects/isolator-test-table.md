---
title: Isolator Fatigue Test Table
slug: isolator-test-table
section: engineering
hook: Benchtop vibration table for fatigue testing eVTOL isolators. Counter-rotating eccentric masses, pressure-tuned air springs, confirmed 30 Hz at 3.5 g, built for $3,021.
role: Team lead, team of 6
timeframe: Sep 2025 to Apr 2026, still in use
skills: [Design and CAD, Analysis and simulation, Leadership]
tools: [Autodesk Inventor, Ansys, MATLAB, Python, Arduino]
hero: /assets/projects/isolator-test-table/hero-poster.jpg
hero_video: /assets/projects/isolator-test-table/hero.mp4
hero_alt: The vibration table running on a lab bench, with the two eccentric mass assemblies spinning between the aluminum supports.
docs_on_request:
  - "Final report (30 pages)"
  - "Design review decks (ADR, PDR, CDR)"
  - "ERM fabrication drawing"
  - "Bill of materials"
featured: true
order: 1
updated: 2026-11-17          # shows as "(updated ...)" next to the title
published: true
---

{% assign img = '/assets/projects/isolator-test-table/' | relative_url %}

## Overview

Senior design project at Widener University, sponsored by Boeing and Parker Lord. The goal was a benchtop stand that can fatigue test vibration isolators for eVTOL aircraft at a fraction of the cost of a commercial shaker. Commercial electrodynamic shakers with this low-frequency force capacity typically cost more than $10,000. The table uses two counter-rotating eccentric rotating masses (ERMs) for vertical excitation and four air springs whose pressure sets the suspension stiffness. It ran at 30 Hz and 3.5 g and was built for $3,021.31 against a $5,000 budget. It is now used to test new isolator designs.

## Requirements

Table 1. Design requirements set with the sponsors.

| Requirement | Specification |
|---|---|
| Frequency | 5 to 30 Hz, 60 Hz stretch goal |
| Acceleration | Up to 35,500 mm/s² (about 3.5 g) |
| Specimen | Up to 18 × 18 in and 5 lb |
| Fatigue life | 5 × 10⁸ cycles before maintenance |
| Size | Benchtop, fits through a standard doorway |
| Budget | $5,000 |

## Actuation selection

Seven actuation methods were scored on frequency range, achievable acceleration, cost, control complexity, maintenance, and life (Figure 1). Linear resonant and piezoelectric actuators cannot produce the displacement needed to move a multi-pound specimen at 1 to 30 Hz. Hydraulic and electrodynamic shakers meet the performance targets but exceed the budget once pumps, cooling, and amplifiers are counted. A crank-slider is cheap, but its bearings and linkages wear under high-cycle fatigue loading. A pneumatic vibrator needs a compressor running for the whole test and builds heat over long runs. ERMs were selected for variable frequency through motor speed, acceleration that scales with the mass offset, and low cost. Their limitation is that frequency and amplitude are coupled, which is acceptable for fatigue testing at discrete frequencies.

<figure>
  <img src="{{ img }}doc-trade-study-slide.jpg" alt="Final presentation slide summarizing the seven actuation methods considered and why ERM actuation was chosen." loading="lazy">
  <figcaption>Figure 1. Actuation trade study as presented at the final review.</figcaption>
</figure>

## Eccentric rotating mass design

Each ERM produces a rotating force F = mrω². Two identical assemblies spin in opposite directions at the same speed, so the horizontal components cancel and the vertical components add. The result is single-axis excitation with no lateral load on the specimen (Figure 2).

<figure>
  <img src="{{ img }}cad-exploded.png" alt="Exploded CAD view showing the top plate, two motor and eccentric mass assemblies, air springs, U-bracket supports, and base plate." loading="lazy">
  <figcaption>Figure 2. Exploded view of the table: vibrating plate, counter-rotating ERM drive, air springs, and base supports.</figcaption>
</figure>

Each ERM is a pair of 1/4 in A36 steel half-discs. One is fixed to the shaft. The other indexes around it on a ring of equally spaced holes, which moves the pair's center of gravity. Eleven discrete settings give an amplitude moment from 0.473 lbf·in, where the plates nearly form a full circle, to 2.536 lbf·in, where they align (Figure 3). Changing the test amplitude is a bolt move, not a new part.

<figure>
  <img src="{{ img }}erm-min-max.jpg" alt="CAD renders of the eccentric mass pair at its minimum setting, nearly a full disc, and at its maximum setting, with both plates aligned." loading="lazy">
  <figcaption>Figure 3. ERM pair at the minimum (left) and maximum (right) amplitude settings.</figcaption>
</figure>

The plates and shafts were checked at the maximum-radius setting at 60 Hz. Static FEA in Ansys and hand calculations against the 250 MPa yield strength of A36 gave a factor of safety of 11.4 for the ERM plate and 2.5 for the shaft (Figures 4 and 5). A lug check on the plate's shaft bore gave a factor of safety of 5.20. The plates were machined by Xometry to a drawing with ±0.010 in on the outer profile and ±0.005 in on the bore, keyway, and adjustment holes, so paired plates stay balanced (Figure 6).

<figure>
  <img src="{{ img }}fea-erm-60hz.png" alt="Ansys equivalent stress contour on the eccentric mass plate at 60 Hz, peak stress concentrated at the shaft bore." loading="lazy">
  <figcaption>Figure 4. Equivalent stress in the ERM plate at 60 Hz, maximum-radius setting.</figcaption>
</figure>

<figure>
  <img src="{{ img }}doc-erm-shaft-sf.jpg" alt="Critical design review slide with the factor of safety calculations for the ERM plate and the drive shaft." loading="lazy">
  <figcaption>Figure 5. ERM and shaft factor of safety from the critical design review.</figcaption>
</figure>

<figure>
  <img src="{{ img }}erm-drawing.png" alt="Fabrication drawing of the ERM plate with GD&T callouts and hole tolerances." loading="lazy">
  <figcaption>Figure 6. ERM fabrication drawing sent to Xometry.</figcaption>
</figure>

Two 400 W AC servo motors drive the ERMs through pillow-block-supported shafts. A direct motor mount was limited by radial load on the motor bearing. The pillow blocks move that load off the motor and keep operation near 60% of peak torque (about 6.80 lbf·in), which preserves bearing and thermal margin over a 5 × 10⁸ cycle run.

## Air spring suspension

Four Continental SK 19-4 sleeve air springs carry the vibrating plate. They share a four-way manifold with a pressure transducer and shutoff solenoids, and the Arduino holds pressure to within ±1% of setpoint. Pressure sets stiffness, so the suspension resonance can be moved away from the test frequency.

The springs were compression tested at 0, 20, and 30 psi on a universal testing machine (Figure 7). At 20 psi, 1/2 in above design height, measured stiffness was 153.51 lbf/in against 167.96 lbf/in calculated (8.90% difference). Natural frequency was 8.74 Hz against 9.11 Hz calculated (4.15%). Across 10 to 20 psi, stiffness ranges from 110 to 309 lbf/in.

<figure>
  <img src="{{ img }}airspring-force-displacement.png" alt="Plot of force versus compression for the air spring at 0, 20, and 30 psi. Stiffness rises with pressure." loading="lazy">
  <figcaption>Figure 7. Air spring force versus compression at three gauge pressures. Re-plotted from the compression test data.</figcaption>
</figure>

A MATLAB time-response model used the measured stiffness and the moving mass to predict displacement across the frequency range for every ERM setting (Figure 8). At 153.51 lbf/in and about 38 lb of moving mass, resonance falls near 6 Hz. Operators avoid 5 to 7 Hz at that pressure, or move the resonance by changing pressure or adding mass to the plate.

<figure>
  <img src="{{ img }}plot-displacement-k153.jpg" alt="MATLAB plot of predicted maximum displacement versus frequency for each of the eleven ERM settings, with a resonance peak near 6 Hz." loading="lazy">
  <figcaption>Figure 8. Predicted plate displacement versus frequency at k = 153.51 lbf/in for each ERM setting.</figcaption>
</figure>

## Structure and shielding

The vibrating and base plates are 1/4 in steel, 18 × 18 in and 21 × 21 in. Modal FEA put the first plate mode near 209 Hz, well above the operating band. Thinner plate placed several modes inside 1 to 30 Hz and was rejected (Figure 9). Supports, motor mounts, and pillow block supports are 6061 aluminum.

<figure>
  <img src="{{ img }}fea-plate-modal.jpg" alt="Modal FEA mode shape of the top plate on its four supports." loading="lazy">
  <figcaption>Figure 9. Top plate modal analysis.</figcaption>
</figure>

A removable enclosure surrounds the rotating parts. The two sides in the plane of ERM rotation are 1/8 in A36 steel, since a released mass would travel that way. The other two are 3/8 in polycarbonate for line of sight. A worst-case thrown mass was estimated at about 18,434 lbf of impact force, using the plate thickness as a conservative stopping distance. FEA of the steel panel gave a maximum transverse shear stress of about 15,229 psi against an estimated ultimate shear strength of 33,504 psi, a factor of safety of about 2.2 (Figure 10). Physical impact testing is still recommended.

<figure>
  <img src="{{ img }}fea-shield-impact.png" alt="FEA of the steel shield panel under the impact of a released eccentric mass." loading="lazy">
  <figcaption>Figure 10. Shield panel impact simulation.</figcaption>
</figure>

## Controls and software

An Arduino Mega 2560 in a NEMA 4X enclosure commands both motor drives over RS-485, switches the air spring solenoids through relays, and reads the manifold pressure transducer (Figure 11). An Analog Devices ADXL accelerometer on the specimen platform streams acceleration over SPI. A hardwired e-stop contactor is the only safety function. The software can ramp the table down but cannot remove motor torque.

<figure>
  <img src="{{ img }}control-block.png" alt="Block diagram: 120 V AC through main switch and e-stop to two motor drives and ERM motors, with the Arduino linked to the drives over RS-485 and to the ADXL accelerometer." loading="lazy">
  <figcaption>Figure 11. Power and control architecture.</figcaption>
</figure>

The control GUI is written in Python (Figure 12). The first version handled motor commands, live acceleration, and FFT display. A later rewrite added a profile runner for unattended dwell and sweep schedules, CSV logging of every status frame, and a heartbeat watchdog. If the program stops or the USB cable is pulled mid-run, the firmware ramps the table down on its own.

<figure>
  <img src="{{ img }}control-gui.png" alt="Screenshot of the control GUI with live acceleration traces, FFT plots per axis, and manifold pressure readout." loading="lazy">
  <figcaption>Figure 12. Control GUI with live acceleration, per-axis FFT, and manifold pressure.</figcaption>
</figure>

## Build

Procurement and fabrication ran from January to early March 2026, with assembly finished in mid-March. Long-lead parts were ordered first: motors, drives, air springs, bearings, couplings, and steel plate. Aluminum supports and mounts were cut on a band saw, then drilled and tapped on a CNC mill. Steel plates were drilled on a drill press after hole positions were checked. ERM fabrication lead time was the main schedule risk tracked at the design reviews (Figures 13 to 15).

<figure>
  <img src="{{ img }}build-assembled.jpg" alt="The assembled table: steel base plate, aluminum supports, two servo motors and eccentric mass assemblies under the top plate." loading="lazy">
  <figcaption>Figure 13. Assembled table before wiring.</figcaption>
</figure>

<figure>
  <img src="{{ img }}build-wiring.jpg" alt="Bench wiring of the Arduino Mega with relay modules for the air spring solenoids." loading="lazy">
  <figcaption>Figure 14. Controller and relay wiring during integration.</figcaption>
</figure>

<figure>
  <img src="{{ img }}doc-risk-matrix.jpg" alt="Critical design review slide with the technical and schedule risk matrix by subsystem." loading="lazy">
  <figcaption>Figure 15. Technical and schedule risk matrix from the critical design review.</figcaption>
</figure>

## Drive fault diagnosis

During testing the eccentric masses oscillated and the two motors lost timing with each other. Any phase error between the motors adds horizontal force, so the table could not be used until this was fixed. The fault was isolated by swapping the motors, swapping the Arduinos, and running with the shaft load removed. The symptom followed one motor drive, which had a broken feedback loop. That drive was replaced and the table returned to synchronized operation.

## Results

- Confirmed run at 30 Hz and 3.5 g, the top of the required envelope. The full DAQ dataset is still being collected.
- Air spring stiffness within 8.90% and natural frequency within 4.15% of calculated values.
- ERM plate and shaft factors of safety of 11.4 and 2.5 at 60 Hz, maximum radius.
- Final cost $3,021.31, 60% of budget. Frame stock was 38% of cost and the pneumatic system 31%.
- The proposal won a $500 ASTM Philadelphia chapter grant (2025-26). The team then won $300 for best poster design at the chapter poster presentation.

## Limitations and ongoing work

ERM frequency and amplitude are coupled. The table runs sinusoidal dwells and sweeps, not arbitrary waveforms. The shield analysis needs physical impact testing. Planned additions are a second accelerometer on the base to measure transmissibility through the air springs, and automated sweep profiles following ASTM D3580-95 Method A. The table is in use testing new isolator designs.

## My role

I led the six-person team and presented every design review to the sponsors. I designed and analyzed the ERMs, including the Inventor and Ansys FEA, wrote the MATLAB operating envelope, produced the ERM fabrication drawing, designed the shielding CAD, wrote the control firmware and GUI, and wrote the user manual. I ran the drive fault diagnosis. Teammates led the air spring and pneumatic design, the mounting plates, and the shield impact FEA.
