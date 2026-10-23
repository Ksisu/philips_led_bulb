# KP18106WPA – datasheet notes (Kiwi Instruments, DS_KP18106WPA_REV1.0_CN)

Original PDF (Chinese): https://datasheet.lcsc.com/datasheet/pdf/bfd6539db46d520cba50adba17558619.pdf?productCode=C2692496
LCSC part: C2692496 – https://www.lcsc.com/product-detail/LED-Drivers_Kiwi-Instruments-KP18106WPA_C2692496.html

High-PF, flicker-free linear constant-current LED driver.

## Features
- PF > 0.7, flicker-free; meets IEC 61000-3-2:2018
- Integrated 800 V bridge rectifier
- Output current settable 5–60 mA, ±4 % chip-to-chip accuracy
- No magnetics, no EMI issues, low system cost
- Over-temperature protection (current foldback, starts ~145 °C)
- Package HSOP-8 (exposed pad = GND)
- Applications: LED filament lamps, LED bulbs, downlights

## Marking
```
KP18106WP
XXXXXX   wafer lot
YWWZZ    year / week (01-52) / serial
```

## Pinout (HSOP-8, pin 1 at the dot, bottom-left)
| Pin | Name | Function |
|-----|------|----------|
| 1, 8 | N / L | AC mains input |
| 2 | VT | Elcap charging-current compensation input; resistor divider from LED pin, tie to GND if unused |
| 3 | RSL | Sets electrolytic-capacitor charging current (resistor to GND) |
| 4 | RCS | Sets LED output current (resistor to GND) |
| 5 | LED | MOSFET drain, to LED string cathode (−) |
| 6 | Cout | MOSFET drain, to electrolytic capacitor (−) |
| 7 | HV | Rectified HV bus, to LED string (+) and capacitor (+) |
| EP | GND | Exposed pad, ground |

## Absolute maximum ratings (TA = 25 °C)
| Parameter | Value |
|-----------|-------|
| N/L, HV pin voltage | −0.5 … 800 V |
| Cout, LED pin voltage | −0.5 … 450 V |
| RSL, RCS, VT pin voltage | −0.5 … 7.5 V |
| RθJA | 65 °C/W |
| PD @ TA = 50 °C | 1.5 W |
| TJ operating | −40 … 150 °C |
| Storage | −55 … 150 °C |
| ESD (HBM) | 2 kV |

## Electrical characteristics (TA = 25 °C)
| Parameter | Condition | Typ | Max |
|-----------|-----------|-----|-----|
| LED / Cout breakdown | – | ≥ 450 V | |
| IOUT | – | 5 … 60 mA | |
| Quiescent current | VLED = 15 V, RCS open | 72 µA | 120 µA |
| VRCS | VLED = 15 V | 600 mV | |
| VRSL | Vcout = 15 V | 600 mV | |
| IOUT chip-to-chip error | – | ±4 % | |
| Thermal foldback start | – | 145 °C | |

Current setting: I = 0.6 V / R  (RCS → LED current, RSL → capacitor charging current)

## This bulb (KT-G22366)
- RCS = 51 Ω ∥ 39 Ω ≈ 22 Ω → I_LED ≈ 27 mA
- RSL = 10 Ω → I_charge ≈ 60 mA
- VT divider: 5.6 MΩ (from LED pin) / 11 kΩ (to GND)
