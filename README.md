# RTCMeasurement

This repository contains the measurement dataset used in our study:

**Where Does My Call Go? Measuring Google Meet, Zoom, and Microsoft Teams on Starlink**

The dataset is collected to study how major real-time communication (RTC) platforms behave over Starlink, with a focus on service-point selection, Starlink Point-of-Presence (PoP) changes, routing paths, and RTT behavior. The measurements cover three widely used browser-based RTC platforms:

- Google Meet
- Zoom
- Microsoft Teams

The dataset includes both stationary Starlink measurements and in-flight Starlink measurements. It is intended to support reproducible analysis of RTC performance over Low-Earth-Orbit (LEO) satellite networks.

## Dataset Overview

The repository is organized into two main measurement categories:

1. **In-flight measurements**
2. **Stationary node measurements**

The in-flight measurements capture RTC behavior during Starlink-enabled commercial flights, where the aircraft movement can cause changes in the active Starlink egress PoP. The stationary measurements provide a baseline using fixed Starlink nodes across Canada.

## In-flight Measurements

The in-flight dataset contains measurements collected during six Starlink-enabled flights across three round-trip routes:

- `yyj-yeg` — Victoria to Edmonton
- `yeg-yyj` — Edmonton to Victoria
- `yeg-yyz` — Edmonton to Toronto
- `yyz-yeg` — Toronto to Edmonton
- `yvr-ogg` — Vancouver to Hawaii
- `ogg-yvr` — Hawaii to Vancouver

Each flight folder is organized by route using airport codes. Inside each route folder, the logs are grouped by RTC platform:

```text
in-flight/
├── yyj-yeg/
│   ├── Google-meet/
│   ├── Microsoft-teams/
│   └── zoom/
├── yeg-yyj/
│   ├── Google-meet/
│   ├── Microsoft-teams/
│   └── zoom/
├── yeg-yyz/
│   ├── Google-meet/
│   ├── Microsoft-teams/
│   └── zoom/
├── yyz-yeg/
│   ├── Google-meet/
│   ├── Microsoft-teams/
│   └── zoom/
├── yvr-ogg/
│   ├── Google-meet/
│   ├── Microsoft-teams/
│   └── zoom/
└── ogg-yvr/
    ├── Google-meet/
    ├── Microsoft-teams/
    └── zoom/
