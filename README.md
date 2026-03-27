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

<h4>🧱 Layout Features</h4>

<ul>
  <li><b>N-well (PMOS region):</b> Provides body biasing and isolation for PMOS operation</li>
  <li><b>Polysilicon gate:</b> Forms the control terminal for channel switching</li>
  <li><b>Metal interconnects:</b> Used for routing signals and power with low resistance</li>
  <li><b>VDD/VSS rails:</b> Ensure stable power supply and ground distribution</li>
  <li><b>Source/Drain contacts:</b> Enable reliable connection between diffusion and metal layers</li>
</ul>
