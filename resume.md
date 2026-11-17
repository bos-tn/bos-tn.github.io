---
title: Resume
permalink: /resume/
---
<div class="resume">

<p class="section-title"><b>RESUME</b></p>

<p class="center">{{ site.title }} &middot; {{ site.tagline }}<br>
Chester, PA &middot; <a href="mailto:{{ site.email }}">{{ site.email }}</a> &middot; <a href="{{ site.linkedin }}">LinkedIn</a><br>
<a href="{{ '/assets/docs/resume.pdf' | relative_url }}">Printable one-page version</a> <small>(PDF)</small> &middot; <small>Updated November 17, 2026</small></p>

<p class="center small">This is the full version, with every project and its details. The PDF is the short general resume.</p>

<h2>Summary</h2>

<p>M.S. mechanical engineering student (GPA 3.58) seeking a full-time R&amp;D, test, or prototype engineering role from May 2027, and part-time work now. Hands-on experience taking mechatronic and thermal prototypes from concept through fabrication, testing, and validation. Cut high-temperature 3D printer failures 40% by tracing them to chamber temperature and applying CFD-informed changes. Led a 6-person team that built and tested a vibration test table for Boeing and Parker Lord. First author of a peer-reviewed paper cited 16 times.</p>

<h2>Education</h2>

<table class="entry"><tr><td><b>M.S. in Mechanical Engineering</b>, Widener University, Chester, PA. GPA 3.58.</td><td class="date">Expected May 2027</td></tr></table>
<p class="meta">Graduate coursework: Finite Element Analysis; Nanotechnology and Nanomaterials; Probability and Statistics in Engineering; Technical Communications. Fall 2026: Mechanical Behavior of Materials; Project Management in Engineering; Thesis I.</p>
<table class="entry"><tr><td><b>B.S. in Mechanical Engineering</b>, Widener University, Chester, PA.</td><td class="date">Aug 2023 to May 2026</td></tr></table>
<p class="meta">Undergraduate coursework: Fluid Mechanics; Heat Transfer; Thermodynamics II; Controls I; Mechanical Measurements I and II; Electric Circuits and Lab; Kinematics; Statics; Dynamics; Mechanics of Deformable Bodies; Fundamentals of Engineering Materials and Design; Engineering Graphics and CAD; Engineering Economics; Introduction to Computer Programming; General Chemistry for Engineers.</p>

<h2>Honors and Certifications</h2>

<ul>
<li>ASTM Philadelphia chapter: $500 grant for the Isolator Fatigue Test Table proposal (2025-26), and $300 for best poster design at the chapter poster presentation.</li>
<li>Dean's List, Fall 2023. Academic Honors, Fall 2024, Fall 2025, and Spring 2026.</li>
<li>AutoCAD certification through SolidProfessor.</li>
</ul>

<h2>Experience</h2>

<table class="entry"><tr><td><b>Research Assistant, Widener University</b></td><td class="date">Dec 2023 to Present</td></tr></table>
<p class="meta">Chester, PA. Advisor: Dr. Babak Eslami.</p>
<ul>
<li>Design, build, and test prototype systems and test fixtures from concept through fabrication and validation.</li>
<li>Performed CFD analysis of the heated chamber of a Creatbot PEEK-300 high-temperature FDM printer. Traced print failures to the chamber's temperature distribution; the CFD-informed changes cut print failures 40%.</li>
<li>Lead thermal characterization studies and implement CFD-informed modifications to high-temperature polymer printing systems.</li>
<li>Ran part-orientation and bed-location trials to improve part strength, surface quality, and manufacturing reliability.</li>
<li>Run the department additive manufacturing lab: 13 printers (10 FDM, 2 SLA, 1 SLS). Run the printers' local network and set up VPN access through custom Raspberry Pi builds for remote use. Provide technical support and process optimization for student and faculty research.</li>
<li>Built standardized mechanical testing and data-analysis workflows in Python and MATLAB. Used on over 200 specimens, they made characterization 5x faster and more repeatable.</li>
<li>Work with hydraulically actuated tensile testing machines and diagnose problems with them.</li>
<li>Led testing on the Onexia production-line collaboration (see Projects).</li>
<li>Collaborate with industry partners and academic researchers to standardize test procedures, collect data, and write concise reports for design decisions.</li>
</ul>

<table class="entry"><tr><td><b>Esports Arena Technical Manager, Widener Esports, Widener University</b></td><td class="date">Jun 2026 to Present</td></tr></table>
<ul>
<li>Manage IT infrastructure and streaming for the esports arena: PC fleet imaging and deployment, game servers, and streaming and AV systems. About 40 PCs and about 80 people supported.</li>
<li>Install and set up Linux servers on Ubuntu Server, including the arena's game server.</li>
<li>Configure BIOS/UEFI on fleet PCs to network boot to the FOG imaging server and to set storage options such as RAID, so machines can be imaged and redeployed.</li>
<li>Use scripts to run mass driver updates and to configure each PC at boot after an image wipe.</li>
<li>Troubleshoot PCs: performance bottlenecks, broken cables, and failed components.</li>
<li>Set up the arena network: switches, DNS, DHCP, and PXE boot. Manage network devices such as wireless cameras and displays for streams and hosted events, including addressing and network layouts.</li>
<li>Developed the arena's stream control app, using Git for version control and to distribute it to the arena PCs. Have built similar apps for other universities as side contract work.</li>
</ul>

<table class="entry"><tr><td><b>Teaching Assistant, Fluid Mechanics, Widener University</b></td><td class="date">Jun 2026 to Present</td></tr></table>
<ul>
<li>Selected as the Fluid Mechanics teaching assistant based on performance in the course.</li>
<li>Support about 20 students per term, 12 hours a week, including tutoring across the mechanical engineering curriculum.</li>
</ul>

<h2>Projects</h2>

<table class="entry"><tr><td><b><a href="{{ '/projects/isolator-test-table/' | relative_url }}">Isolator Fatigue Test Table</a>, Boeing &amp; Parker Lord (Team Lead)</b></td><td class="date">Sep 2025 to Apr 2026</td></tr></table>
<p class="meta">Senior design. <a href="{{ '/projects/isolator-test-table/' | relative_url }}">Full case study</a>.</p>
<ul>
<li>Led a 6-person team that designed, built, and tested a benchtop vibration table for fatigue testing eVTOL aircraft isolators. Targets: 5 to 30 Hz with a 60 Hz stretch goal, up to 3.5 g, and specimens up to 18 &times; 18 in and 5 lb.</li>
<li>Confirmed a run at 30 Hz and 3.5 g. Built for $3,021.31 against a $5,000 budget. The table is now used to test new isolator designs.</li>
<li>Designed an adjustable-amplitude eccentric rotating mass (ERM) with indexed movable weights, giving 11 settings from one part set. Tunable output without electronics, which simplified low-frequency testing.</li>
<li>Ran the ERM FEA in Inventor and Ansys and wrote the MATLAB operating envelope.</li>
<li>Produced the GD&amp;T (ASME Y14.5) fabrication drawing for the ERM and did tolerance stack-up mitigation on the table.</li>
<li>Wrote the Arduino control firmware and a Python GUI for motor control, accelerometer readout, live FFT, and logging. Designed the shielding CAD and wrote the user manual.</li>
<li>Root cause analysis: the eccentric masses oscillated and the two motors lost timing. Isolated the fault by swapping motors, swapping Arduinos, and removing the shaft load. One drive had a broken feedback loop; it was replaced and the table returned to synchronized operation.</li>
<li>Re-engineered the frame for stiffness and lower mass.</li>
<li>As team lead, presented every design review to the sponsors, distilled the feedback, and assigned the team its tasks. Ran scheduling, vendor coordination, material procurement, and collaborative system CAD. Brought Trello into the team's workflow.</li>
<li>Won a $500 ASTM Philadelphia chapter grant for the proposal, then $300 for best poster design at the chapter poster presentation.</li>
</ul>

<table class="entry"><tr><td><b>Characterization of CF-Reinforced PLA Composites in FDM 3D Printing</b></td><td class="date">2025</td></tr></table>
<p class="meta">First author. Journal of Manufacturing and Materials Processing. <a href="https://doi.org/10.3390/jmmp9090288">doi.org/10.3390/jmmp9090288</a></p>
<ul>
<li>Mapped the tensile-flexural trade-off across 0 to 100% PLA-CF layer ratios and multiple nozzle diameters. Produced a design chart balancing strength and flexibility for end-use parts.</li>
<li>Standardized ASTM-aligned tensile and 3-point bend workflows with automated data reduction in Python and MATLAB.</li>
<li>Connected AFM and print-path observations to macroscale results to recommend mid-range layer ratios.</li>
</ul>

<table class="entry"><tr><td><b>Infill Percentage vs. Nozzle Diameter in FDM 3D Printing</b></td><td class="date">2024</td></tr></table>
<p class="meta">Second author. ASME IMECE 2024. <a href="https://doi.org/10.1115/IMECE2024-145944">doi.org/10.1115/IMECE2024-145944</a></p>
<ul>
<li>Co-authored a PLA, ABS, and TPU study showing smaller nozzles improve surface quality at the cost of print time. Produced material-specific nozzle-selection guidelines.</li>
<li>Designed trials on adhesion, stringing, and warping against nozzle size. Captured ABS sensitivity at larger diameters and TPU flow limits at small diameters.</li>
<li>Turned the findings into a framework for balancing repeatability, quality, and print time.</li>
</ul>

<table class="entry"><tr><td><b>In-Situ Electroplating FDM Prototype</b></td><td class="date"></td></tr></table>
<p class="meta">Automation project.</p>
<ul>
<li>Prototyped a bistable mechanism with a copper-sulfate liquid feed to electroplate parts mid-print. Documented custom G-code phases and feasibility on a Bambu A-series printer.</li>
<li>Solved the "don't pause the print" constraint with a deploy/retract path and electrical routing.</li>
<li>Used basic PLC-style control on ESP32 and Arduino boards for tool-change timing.</li>
<li>Set up a repeatable adhesion and conductivity test plan. Wrote build and validation steps for future revisions.</li>
</ul>

<table class="entry"><tr><td><b>Production-Line Automation Study, Onexia (Industry Collaboration)</b></td><td class="date">Fall 2024</td></tr></table>
<p class="meta">About six weeks, through the research lab. Results are confidential to Onexia.</p>
<ul>
<li>Worked with Onexia's research department to automate part of a production line for medical inserts that uses a four-stage stamping tool.</li>
<li>Primary contact for the design of experiments. Designed a custom DOE and test method.</li>
<li>Measured required force, stroke length, and cycle rate on a Tinius Olsen testing machine with a load cell.</li>
<li>Tested and specified the force and method of actuation needed to run the line smoothly. The project ended with pneumatic actuation.</li>
<li>Led the testing specifics and wrote the reports, including a quantitative analysis. The line ran to spec after handoff.</li>
</ul>

<table class="entry"><tr><td><b>Combat Robot, Local Tournament (First Place)</b></td><td class="date">2023</td></tr></table>
<ul>
<li>Built a battle bot under 5 lb with a microcontroller, a radio control interface, and actuating arms. Took first place.</li>
</ul>

<table class="entry"><tr><td><b>Personal Builds</b></td><td class="date"></td></tr></table>
<ul>
<li>Built several gaming PCs from the ground up: selected the hardware, assembled them, and installed the OS.</li>
<li>Built home media servers from multiple recycled PCs.</li>
</ul>

<h2>Technical Skills</h2>

<table class="skills" border="1" cellpadding="4" cellspacing="0">
<tr><th>CAD and drawings</th><td>SolidWorks; Autodesk Inventor; Onshape; AutoCAD; fabrication and assembly drawings; GD&amp;T (ASME Y14.5); tolerance stack-up</td></tr>
<tr><th>Prototyping and fabrication</th><td>Manual machining (mill, lathe); MIG and stick welding; mechanical assembly; soldering; FDM, SLA, and SLS additive manufacturing, including high-temperature polymers such as PEEK; 3D scanning to reconstruct and repair complex geometry</td></tr>
<tr><th>Electronics and instrumentation</th><td>Circuit layout; simple custom PCBs; Arduino and ESP32 boards; solenoids and sensors; data acquisition (DAQ) and LabVIEW; accelerometers; load cells; multimeters and oscilloscopes for signal diagnosis</td></tr>
<tr><th>Analysis and simulation</th><td>Computational fluid dynamics (CFD) for thermal distribution; finite element analysis (FEA) in Inventor; Python; MATLAB; Excel</td></tr>
<tr><th>Testing and methods</th><td>ASTM-aligned tensile and 3-point bend testing; design of experiments (DOE); test-plan and test-method development; Tinius Olsen testing machine with load cell; hydraulically actuated tensile testing machines; data reduction and automation; material characterization; AFM observation tied to macroscale results</td></tr>
<tr><th>Automation</th><td>Pneumatic actuation specification; basic PLC-style control on ESP32 and Arduino boards; custom G-code; automated data reduction in Python and MATLAB</td></tr>
<tr><th>Systems and IT</th><td>Windows and Linux (Ubuntu, Ubuntu Server); Linux server setup; BIOS/UEFI configuration, network boot, and RAID; PC fleet imaging and deployment; networking (switches, DNS, DHCP, PXE boot); hardware troubleshooting; game servers; streaming and AV systems</td></tr>
<tr><th>Software and workflow</th><td>Git; Microsoft Office (Word, Excel, PowerPoint); Trello</td></tr>
</table>

<h2>Publications</h2>

<p class="pub">[1] <b>B. Blake</b>, R. Mendenhall, and B. Eslami, &ldquo;Balancing Strength and Flexibility: Mechanical Characterization of Carbon Fiber-Reinforced PLA Composites in FDM 3D Printing,&rdquo; <i>Journal of Manufacturing and Materials Processing</i>, vol. 9, no. 9, p. 288, 2025. <a href="https://doi.org/10.3390/jmmp9090288">doi.org/10.3390/jmmp9090288</a>. Cited 16 times (Crossref).</p>
<p class="pub">[2] O. Watson, <b>B. Blake</b>, S. Pagano, and B. Eslami, &ldquo;Optimization of Infill Percentage Versus Nozzle Diameter in Fused Deposition Modeling 3D Printing,&rdquo; in <i>Proc. ASME IMECE 2024</i>, vol. 2: Advanced Manufacturing. <a href="https://doi.org/10.1115/IMECE2024-145944">doi.org/10.1115/IMECE2024-145944</a>.</p>

</div>
