---
aliases:
  - Power Subsystem
tags:
  - 
file-created: 2023-03-25
file-modified: 2023-09-02
note-type: general
description: 
linter-yaml-title-alias: Power Subsystem
---

# Power Subsystem

#status/postponed

Related to [[Top hardware level]]

---

- Battery:  Adafruit 2011, https://www.adafruit.com/product/2011
  - 4.2 charge, 3.7v nominal, 3.0 end of discharge
  - 2000mAh
  - Max 1A discharge
- Battery Charger: BQ25792
- Battery Protection / Balancer: N/A (Integrated protection, no balancing)
- USB PD Controller: TPS25750
- USB VBUS TVS Protection: TVS2200
- USB Data TVS Protection
- 5V Regulator:
- 3.3V Regulator:
- Power Rails:
  - VBUS_PD: VBUS exposed directly from the USB-C port. 5v - 20v
  - VSYS: Switched Batt
