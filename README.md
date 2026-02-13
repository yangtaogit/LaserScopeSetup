# UV-TCT Setup @ Lawrence Berkeley National Laboratory (LBNL)

This repository documents the setup of the **Ultraviolet Laser Transient Current Technique (UV-TCT)** system installed at **Lawrence Berkeley National Laboratory (LBNL)**.

FreeCAD flle: ***LaserScope_Setup.FCStd***

## Reference

Related published results:
- DOI: https://doi.org/10.1109/LED.2025.3548509  

## System Layout
![UV-TCT system layout](./LaserScope_Setup.png)

## Bill of Materials
| # | Item | Link | Qty |
|---:|---|---|---:|
| 1 | RC04FC-F003 | https://www.thorlabs.com/item/RC04FC-F01 | 1 |
| 2 | SM1A6FW | https://www.thorlabs.com/item/SM1A6FW | 1 |
| 3 | SM1T1 | https://www.thorlabs.com/item/SM1T1?aID=8fe9f947ca2bc370261e88be81fcf37e&aC=1 | 1 |
| 4 | m30-x-10-to-sm01-adapter | https://www.edmundoptics.com/p/m30-x-10-to-sm01-adapter/34660/ | 1 |
| 5 | 20X UV-VIS Broadband Beam Expander | https://www.edmundoptics.com/p/20x-uv-vis-da-beam-expander/40661/?srsltid=AfmBOooUZ1NCebaOMqTwVyWz5aPaiTJ8EJCvWq-xNx7DOSHp7NH3fJUK | 1 |
| 6 | SM2A25 | https://www.thorlabs.com/item/SM2A25 | 1 |
| 7 | SM2T2 | https://www.thorlabs.com/item/SM2T2 | 1 |
| 8 | LA1401-A-ML | https://www.thorlabs.com/item/LA1401-A-ML?aID=a5d1d315eaed1357058308131b9b24ec&aC=1 | 1 |
| 9 | SM2D25D | https://www.thorlabs.com/item/SM2D25D | 1 |
| 10 | Holder of Beam Expander (Aluminum 6061, CNC) | — | 1 |
| 11 | M5 × 0.8 mm thread, 16 mm long | https://www.mcmaster.com/91290A232/ | 2 |
| 12 | PP110-30XYZ Three Axis Stage | https://www.pdvcn.com/motorized-xyz-combined-stage/1008.html | 1 |
| 13 | TIA Board | — | 1 |
| 14 | Board Holder (resin 3D printing) | — | 1 |
| 15 | MB4545/M Aluminum Breadboard | https://www.thorlabs.com/item/MB4545_M | 1 |
| 16 | AV6 Sorbothane Feet | https://www.thorlabs.com/item/AV6?aID=7fb6b4c209826817b4ef2e30767dd460&aC=1 | 4 |
| 17 | Custom Enclosure | https://www.thorlabs.com/optical-enclosure-accessories?aID=a290e45047dd4bf863d57f1160553fb6&aC=2&tabName=Overview | 1 |

## Picosecond Fiber-Coupled Diode Laser

| Parameter | Specified | Measured | Comment |
|---|---|---|---|
| Wavelength | 375 (± 5) nm | 373.0 nm | @ 20 MHz |
| Pulse width (measured)<sup>1</sup> | — | See table below | Pulse width is frequency dependent |
| Pulse width (after deconvolution)<sup>1</sup> | 30 ps | See table below | — |
| Repetition rate (external Trigger) | 0–20 MHz | 0–20 MHz | — |
| Repetition rate (internal frequency generator) | 1 Hz–20 MHz | 1 Hz–20 MHz | Step 1 Hz |
| Average power (@ 20 MHz)<sup>2</sup> | 600 µW | 655 µW | Measured at fiber output |
| Peak power<sup>3</sup> (up to 20 MHz) | 1000 mW | &gt; 1130 mW | See table below<br>Measured at fiber output |
| Fiber coupling | MM, 200 µm core, UV-resistant, FC/PC | MM, 200 µm core, UV-resistant, FC/PC | Coupling efficiency ~ 90% |
| Fiber connector & mating sleeve | FC/PC | FC/PC | — |
| Delay LASER OUTPUT to TRIG IN | TYP. 50 ns | 43.2 ns | Measured at fiber output |
| Delay LASER OUTPUT to SYNC OUT (TTL) | TYP. 35 ns | 30.5 ns | Measured at fiber output |
| SYNC OUT (TTL) On the front panel | TTL | + 3.3 V into 50 Ω | — |
| Jitter*: Laser Pulse to External trigger | &lt; 4 ps | &lt; 4 ps | External trigger with rise time &lt; 0.2 ns; amplitude 5 V ± 0.5 V |
| Jitter*: Laser Pulse to SYNC OUT (TTL) | &lt; 4 ps | &lt; 4 ps | External trigger with rise time &lt; 0.2 ns; amplitude 5 V ± 0.5 V |
| Jitter*: Laser Pulse to SYNC OUT | &lt; 4 ps | &lt; 4 ps | Internal trigger<br>*These values are valid up-to 20 MHz and amplitude not less than 50% of the maximum one* |
| LASER ON/OFF input | Not specified | &gt; 3 V → ON<br>&lt; 2 V → OFF | Input impedance 1 kΩ |
| Laser class | Not specified | 3R | — |
