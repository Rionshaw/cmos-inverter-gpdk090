# cmos-inverter-gpdk090
CMOS inverter implemented in gpdk090 technology with full design flow: schematic, layout, DC and Transient simulation, delay and power analysis using Cadence Virtuoso.<br>
## Objectives
<ul>
  <li>Design a CMOS inverter using gpdk090 technology.</li>
  <li>Perform schematic and layout design in Cadence Virtuoso.</li>
  <li>Analyze -
    <ul>
      <li>Voltage Transfer Characteristics (VTC).</li>
      <li>Transient response.</li>
      <li>Propagation delay (tpdr, tpdf).</li>
      <li>Energy consumption.</li>
    </ul>
  </li>
</ul>

## Tools and Technology

<ul>
<li>Cadence Virtuoso (Schematic Editor, Layout Suite).</li>
<li>ADE L / ADE XL.</li>
<li>Technology Library - gpdk090.</li>
</ul>

## Circuit Description

The CMOS inverter consists of - <br>
<ul>
PMOS transistor (pull-up network)<br>
NMOS transistor (pull-down network)<br>
</ul>

Operation - <br>
<ul>
<p>Vin = 0 → PMOS ON,        NMOS OFF → Vout = VDD.</p>
<p>Vin = VDD → PMOS OFF,     NMOS ON → Vout = 0.</p>
</ul>
This complementary behavior ensures <b>Low Static Power Consumption<b>.<br>

## Schematic
![Schematic of CMOS Inverter](https://github.com/Rionshaw/cmos-inverter-gpdk090/blob/c4cf65469381b9b8f16f16526f3a0ae553a3ab93/Screenshot-1.png)

## Layout
![Layout of CMOS Inverter](https://github.com/Rionshaw/cmos-inverter-gpdk090/blob/b66f2db9a19674d30903651d49884bc80d665208/Screenshot-7.png)

<h3> Layout Features</h3>

<ul>
  <li><b>N-well (PMOS region) -</b> Provides body biasing and isolation for PMOS operation</li>
  <li><b>Polysilicon gate -</b> Forms the control terminal for channel switching</li>
  <li><b>Metal interconnects -</b> Used for routing signals and power with low resistance</li>
  <li><b>VDD/VSS rails -</b> Ensure stable power supply and ground distribution</li>
  <li><b>Source/Drain contacts -</b> Enable reliable connection between diffusion and metal layers</li>
</ul>

 ## Simulation Setup

<h3>🔹 Transient Analysis</h3>
<ul>
  <li><b>Input Signal -</b> Pulse waveform applied at Vin</li>
  <li><b>Supply Voltage (VDD) -</b> 1.2V / 1.8V</li>
  <li><b>Rise/Fall Time -</b> Defined to observe realistic switching behavior</li>
  <li><b>Simulation Time -</b> ~200 ns to capture multiple switching cycles</li>
  <li><b>Objective -</b> Analyze dynamic response, switching characteristics, and propagation delay (tpdr, tpdf)</li>
</ul>

<h3>🔹 DC Analysis</h3>
<ul>
  <li><b>Input Sweep -</b> Vin varied from 0 to VDD</li>
  <li><b>Output Measurement -</b> Vout recorded for each Vin</li>
  <li><b>Result -</b> Voltage Transfer Characteristic (VTC) curve (Vout vs Vin)</li>
  <li><b>Objective -</b> Evaluate switching threshold, gain, and noise margin</li>
</ul>

## Results

<h3>🔹 Transient Response</h3>
<p>
The transient analysis shows the dynamic switching behavior of the CMOS inverter.
The output (Vout) transitions between logic levels in response to the input pulse (Vin),
allowing evaluation of switching characteristics and propagation delay.
</p>

<img src="https://github.com/Rionshaw/cmos-inverter-gpdk090/blob/bf3653e3debf6f5d914466718e5231e553d66ca0/Screenshot-9.png" alt="Transient Response" width="500">

<h3>🔹 DC Response (VTC)</h3>
<p>
The DC sweep generates the Voltage Transfer Characteristic (VTC) curve,
which represents the relationship between input voltage (Vin) and output voltage (Vout).
This curve is used to analyze switching threshold, gain, and noise margins.
</p>
<img src="https://github.com/Rionshaw/cmos-inverter-gpdk090/blob/49e1fb7ab873df115df0fef4dcf0e3a5c4e42bf8/Screenshot-13.png" alt="VTC Curve" width="500">
