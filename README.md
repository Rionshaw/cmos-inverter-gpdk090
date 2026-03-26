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
Operation -
<br>
<ul>
Vin = 0 → PMOS ON,        NMOS OFF → Vout = VDD <br>
Vin = VDD → PMOS OFF,     NMOS ON → Vout = 0<br>
</ul>
This complementary behavior ensures <b>Low Static Power Consumption<b>.<br>
