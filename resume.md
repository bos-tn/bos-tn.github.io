---
title: Resume
permalink: /resume/
---
<div class="resume">

<p class="section-title"><b>RESUME</b></p>

<p class="center">{{ site.title }} &middot; {{ site.tagline }}<br>
Chester, PA &middot; <a href="mailto:{{ site.email }}">{{ site.email }}</a> &middot; <a href="{{ site.linkedin }}">LinkedIn</a><br>
<a href="{{ '/assets/docs/resume.pdf' | relative_url }}">Printable one-page version</a> <small>(PDF)</small> &middot; <small>Updated November 17, 2026</small></p>

<h2>Summary</h2>

<p>M.S. mechanical engineering student (GPA 3.58) seeking a full-time R&amp;D, test, or prototype engineering role from May 2027, and part-time work now. Cut high-temperature 3D printer failures 40% by tracing them to chamber temperature and applying CFD-informed changes. Led a 6-person team that built and tested a vibration test table for Boeing and Parker Lord. First author of a peer-reviewed paper cited 16 times.</p>

<h2>Education</h2>

<table class="entry"><tr><td><b>M.S. in Mechanical Engineering</b>, Widener University, Chester, PA. GPA 3.58.</td><td class="date">Expected May 2027</td></tr></table>
<table class="entry"><tr><td><b>B.S. in Mechanical Engineering</b>, Widener University, Chester, PA.</td><td class="date">May 2026</td></tr></table>
<p class="meta">Relevant coursework: Finite Element Analysis; Mechanical Behavior of Materials; Heat Transfer; Fluid Mechanics; Controls I.</p>
<p class="meta">Honors: ASTM Philadelphia chapter $500 grant and $300 best poster award; Dean's List (Fall 2023); Academic Honors (3 terms).</p>

<h2>Experience</h2>

<table class="entry"><tr><td><b>Research Assistant, Widener University</b></td><td class="date">Dec 2023 to Present</td></tr></table>
<p class="meta">Chester, PA. Advisor: Dr. Babak Eslami.</p>
<ul>
<li>Traced PEEK-300 printer failures to the heated chamber's temperature distribution; CFD-informed changes cut failures 40%.</li>
<li>Built Python and MATLAB test workflows that made characterization of over 200 specimens 5x faster and more repeatable.</li>
<li>Run the additive manufacturing lab: 13 printers (10 FDM, 2 SLA, 1 SLS), its local network, and Raspberry Pi VPN builds.</li>
<li>Ran part-orientation and bed-location trials to improve part strength, surface quality, and manufacturing reliability.</li>
<li>Diagnose problems on hydraulically actuated tensile testing machines.</li>
<li>Standardize test procedures, collect data, and write reports for design decisions with industry partners such as Onexia.</li>
</ul>

<table class="entry"><tr><td><b>Esports Arena Technical Manager, Widener Esports, Widener University</b></td><td class="date">Jun 2026 to Present</td></tr></table>
<ul>
<li>Run IT and streaming for the arena: about 40 PCs, game servers, and AV systems for about 80 people.</li>
<li>Set up the arena network (switches, DNS, DHCP, PXE boot) and its Linux servers.</li>
<li>Developed the arena's stream control app with Git, and have built similar apps for other universities as side contract work.</li>
</ul>

<table class="entry"><tr><td><b>Teaching Assistant, Fluid Mechanics, Widener University</b></td><td class="date">Jun 2026 to Present</td></tr></table>
<ul>
<li>Support about 20 students per term, 12 hours a week, including tutoring across the mechanical engineering curriculum.</li>
</ul>

<h2>Projects</h2>

<table class="entry"><tr><td><b><a href="{{ '/projects/isolator-test-table/' | relative_url }}">Isolator Fatigue Test Table</a>, Boeing &amp; Parker Lord (Team Lead)</b></td><td class="date">Sep 2025 to Apr 2026</td></tr></table>
<ul>
<li>Led a 6-person team that built a $3,021 vibration table for eVTOL isolators; confirmed a 30 Hz, 3.5 g run.</li>
<li>Engineered an indexed-weight, adjustable-amplitude eccentric rotating mass (ERM) and produced its GD&amp;T fabrication drawings.</li>
<li>Wrote the Arduino firmware and a Python GUI for motor control, accelerometer readout, live FFT, and logging.</li>
<li>Traced lost motor timing to a drive with a broken feedback loop by swapping motors and controllers.</li>
</ul>

<table class="entry"><tr><td><b>Production-Line Automation Study, Onexia (Industry Collaboration)</b></td><td class="date">Fall 2024</td></tr></table>
<ul>
<li>Designed and ran a custom DOE with a load cell and specified pneumatic actuation; the line ran to spec after handoff.</li>
</ul>

<table class="entry"><tr><td><b>Combat Robot, Local Tournament (First Place)</b></td><td class="date">2023</td></tr></table>
<ul>
<li>Built a battle bot under 5 lb with a microcontroller, a radio control interface, and actuating arms.</li>
</ul>

<h2>Technical Skills</h2>

<table class="skills" border="1" cellpadding="4" cellspacing="0">
<tr><th>Prototyping and fabrication</th><td>Manual machining (mill, lathe); MIG and stick welding; mechanical assembly; soldering; FDM, SLA, and SLS additive manufacturing, including PEEK; 3D scanning</td></tr>
<tr><th>Testing and instrumentation</th><td>ASTM-aligned tensile and 3-point bend testing; design of experiments (DOE); test plans and procedures; data acquisition (DAQ) and LabVIEW; accelerometers; load cells</td></tr>
<tr><th>CAD and drawings</th><td>SolidWorks; Inventor; Onshape; AutoCAD; fabrication drawings; GD&amp;T (ASME Y14.5); tolerance stack-up</td></tr>
<tr><th>Analysis and programming</th><td>Computational fluid dynamics (CFD); finite element analysis (FEA); Python; MATLAB; Excel; Git</td></tr>
<tr><th>Electronics and systems</th><td>Circuit layout; simple custom PCBs; Arduino and ESP32 boards; multimeters and oscilloscopes; pneumatic actuation; Windows and Linux; networking (DNS, DHCP, PXE boot)</td></tr>
</table>

<h2>Publications</h2>

<p class="pub">[1] <b>B. Blake</b>, R. Mendenhall, and B. Eslami, &ldquo;Balancing Strength and Flexibility: Mechanical Characterization of Carbon Fiber-Reinforced PLA Composites in FDM 3D Printing,&rdquo; <i>Journal of Manufacturing and Materials Processing</i>, vol. 9, no. 9, p. 288, 2025. <a href="https://doi.org/10.3390/jmmp9090288">doi.org/10.3390/jmmp9090288</a>. Cited 16 times (Crossref).</p>
<p class="pub">[2] O. Watson, <b>B. Blake</b>, S. Pagano, and B. Eslami, &ldquo;Optimization of Infill Percentage Versus Nozzle Diameter in Fused Deposition Modeling 3D Printing,&rdquo; in <i>Proc. ASME IMECE 2024</i>, vol. 2: Advanced Manufacturing. <a href="https://doi.org/10.1115/IMECE2024-145944">doi.org/10.1115/IMECE2024-145944</a>.</p>

</div>
