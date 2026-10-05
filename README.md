▄▄▄▀▀▀█                        ▄▄▄▀▀▀█ ▄▄▄▀▀▀█              
 █   █                          █   █   █   █               
 █ ░ █            ▄▀▀█▀▀█▀▄▄    █ ░ █   █ ░ █    ▀▄▄▄▄▄▄▄▀  
 █░▒░█           █ ░▒█  ▒█▓█░   █░▒░█   █░▒░█   ██▓██▀██▓██ 
 █▒▓▒▄▀▀▓▄▄▄■▄  █▒░▒░   ░▓▀▀▀   █▒▓▒█   █▒▓▒█  █▓▒▓     ▓▒▓█
 █▓█▓░  ▐▐░▓█▌▌ █▒▓▒█▀■▀▀▀      █▓█▓░   █▓█▓░  █▒░▒▓   ▓▒░▒█
 █ ░ ▒   █▓▒▓█░ █▓█▓░    ▄▄■▄   █ ░ ▒   █ ░ ▒  █░ ░▓   ▓░ ░█
 █░▒░▓   █▒░░▒▒  █ ░▒▄ ▄▒░░▒▓▌  █░▒░▓   █░▒░▓   █ ░▒ ▄ ▒░ █ 
 █▀▀▀    █░▄▄▄▓    ▀▄▄▄▄▀▀▀▀    █▀▀▀    █▀▀▀     ▀▄▄▄■▄▄▄▀  
▀▀     ■▀▀▀                    ▀▀      ▀▀                   
# AERIS-1 Tricopter

A very small Y-tricopter built to show the full chain of a robot: **sense, decide, act**.

Two front motors and one rear motor provide lift. The rear motor sits on an SG90 servo that tilts it, which steers yaw. An ESP32 runs flight code written from scratch.

Live site: `https://ahnafftahmidd-spec.github.io/AERIS-1/`

## How it works

- **Sense:** MPU6500 (motion) and BMP280 (air pressure, for a relative altitude estimate).
- **Decide:** custom flight code on an ESP32 DevKit V1.
- **Act:** three coreless 8x20 mm motors driven through two TB6612FNG drivers, plus an SG90 servo that tilts the rear motor for yaw.
- **Command link:** laptop (typed commands) to Arduino Uno ground station to nRF24L01+ radio to the ESP32.
- **Power:** a single 1S LiPo, with an MT3608 boost module for the logic supply.

## Airframe and mass

- Y-layout, open central body 60 x 60 x 35 mm, 8.6 mm motor seats, 3D printed.
- Measured weight of all parts, excluding the frame: 95 g.
- Frame limit: 15 g. Target total: about 110 g.

## Status

| Item | Status |
|---|---|
| MPU6500 readings | Verified |
| BMP280 pressure sensing | Verified |
| Flight control and radio control | In build |
| Autonomous climb, hold and return | Planned |
| Hover time, thrust margin, altitude response | To demonstrate |

## Test ladder

Each height is only attempted after the previous one passes: 2 m, 5 m, 10 m, 15 m, then 20-30 m.

## Repository layout

```
index.html      the project website (single file)
docs/           design log, parts list, test plan
firmware/       flight code
cad/            3D models (STL and source files)
media/          photos and videos of the build
LICENSE         copyright notice
```

## Copyright

Copyright (c) 2026 Ahnaf Tahmid. All rights reserved. See `LICENSE`.
