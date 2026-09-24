---
layout: default
title: CV
active_page: cv
---

## Alexander — C++ Software Developer

Moscow, Russia &nbsp;·&nbsp; [linkedin.com/in/masteraler](https://www.linkedin.com/in/masteraler)

---

### Skills

`C++` `Qt` `OpenCV` `FFmpeg` `Python` `Go` `Docker` `Lua`
`PostgreSQL` `Tarantool` `ZeroMQ` `OpenSSL` `OpenGL` `RTSP` `ONVIF`

---

### Experience

**Senior C++ Software Developer** — [DSSL](https://dssl.ru)  
*Apr 2024 – present · Moscow*

Development and support of video analytics modules and corresponding VMS subsystems.

- Key role in implementing inter-camera person tracking
- Fixed a critical flickering bug reproducible only on a VIP-client's production hardware
- Feature lead on a neural-network abandoned object detector
- Solo migration of the 500+k LOC video analytics codebase from OpenCV 2.4.9 → 4.12.0

---

**Senior C++ Software Developer** — [NtechLab](https://ntechlab.com)  
*Apr 2020 – Apr 2024 · 4 years · Moscow*

Core team member developing the microservice backend of the *FindFace Multi* video-analytics platform. Primarily C++ on Linux and Docker, with production work in Go and Python.

- Developed and optimized core C++ services: tracking algorithms, inference pipelines, memory usage, and throughput under high load
- Improved multithreaded performance through profiling, processing-queue design, lock-granularity tuning, and reduced contention
- Maintained and enhanced a distributed face-vector search service built on Tarantool, including its custom C index and HNSW-based search
- Reduced serialization overhead by migrating communication between the Go API layer and C++ services from JSON to MessagePack
- Designed a disk-backed HTTP restreaming service for lower-priority H.264/H.265 video, buffering excess live input so the ML pipeline could consume each stream at its own pace without disconnecting under load
- Added hardware inference support for Huawei Atlas / Ascend NPUs
- Designed and implemented a resource-constrained VMS integration for a major international customer, including architecture, capacity planning, and deployment sizing
- Developed a licensing-service backend in Python and Go, with minor contributions to its Vue.js frontend

---

**Senior C++ Software Developer** — [Kraftway Corporation PLC](https://kraftway.ru/)
*Jun 2018 – Apr 2020 · 1 yr 11 mo · Moscow*

Cross-platform VMS with SCADA capabilities and video analytics (Windows / Ubuntu / Astra Linux).  
Deployed by *Gormost* (Moscow government contractor) for bridge and pedestrian infrastructure surveillance.

- Migrated legacy codebase to MSVC 2015
- Full redesign & heavy refactoring of the operator client (C++ / Qt)
- Video rendering performance improvements (OpenGL)
- Video analytics upgrades via modern OpenCV (incl. custom Astra Linux build)
- Video decoding stability & performance improvements (ffmpeg)
- PostgreSQL query profiling & optimization
- Client–server layer migrated to REST-like API over a custom ZeroMQ broker (REQ-REP, PUB-SUB) with session-key authentication (OpenSSL)

---

**C++/Qt Developer** — [VIPole CIS](https://www.vipole.com/)  
*Oct 2015 – Apr 2018 · 2 yrs 7 mo · Moscow*

Desktop client of a cross-platform messenger (Windows / Linux / macOS).  
Qt Widgets & QML UI; Boost for the network layer.

---

**Software Engineer** — Sukhoi Design Bureau (ОКБ Сухого)  
*May 2013 – Oct 2015 · 2 yrs 6 mo · Moscow*

Educational computer system for military pilots with a built-in document management system (C++ / Qt, Windows / Astra Linux).

- Designed and implemented database architecture (PostgreSQL)
- Built a small server-side API in Python over ZeroMQ
- Coordinated tasks directly with customers on-site

---

**Web Software Developer** — [RBC](https://www.rbc.ru/) (РБК)  
*Sep 2012 – Apr 2013 · 8 mo · Moscow*

Junior backend developer supporting the qip.ru portal. PHP · JavaScript · MySQL · HTML/CSS.

---

### Education

**Lomonosov Moscow State University (MSU)**  
Specialist degree · Engineering Physics
