# G-Force Space: Complete Reference - Key Concepts Explained

> Based on the G-Force Space founding document prepared for Goncalo Esteves, March 2026.

---

## 1. The OODA Loop - The Intellectual Spine

The single most important concept in the entire G-Force Space platform. OODA stands for:

- **Observe** - Collect raw space/satellite data (what the satellites see)
- **Orient** - Apply a systems engineering lens to interpret that data
- **Decide** - Determine what it means for real humans on the ground
- **Act** - Train, prepare, and improve (bridging to GeForce performance programs)

This military decision-making framework (originally from fighter pilot John Boyd) serves triple duty:
1. **Editorial framework** - structures every episode
2. **Brand differentiator** - transforms "war news" into skill-building content
3. **Monetization bridge** - connects free space intelligence content to paid GeForce human performance training

---

## 2. Brand Voice Principles

G-Force Space is NOT a news channel. It is a **space intelligence platform**. Five core principles govern all content:

| Principle | Meaning |
|-----------|---------|
| **Truth Without Weaponization** | Show data honestly, never celebrate destruction. The satellite is an "honest witness" |
| **Engineer's Precision, Human's Heart** | Rigorous analysis delivered with empathy, not cold detachment |
| **Space for Good** | Every episode redirects: this tech could track famine, refugees, climate - not just war |
| **Naive and Proud** | Openly believing space should teach us to do good on Earth is the mission, not a weakness |
| **No Sides, No Regimes** | Opposition to systems that harm innocents, never against any people or nation |

---

## 3. Space Data Intelligence Stack (5 Tiers)

The document catalogs a complete toolkit of satellite and geospatial data sources organized by cost and accessibility:

### Tier 1: Free, Open, Daily (Core Operations)
- **NASA FIRMS** - Real-time fire/thermal anomaly detection. First thing checked every morning. Detects strikes, explosions, burning infrastructure
- **NASA Earthdata / Worldview** - 1,200+ imagery layers, many updated within 3 hours of satellite pass. Primary daily data pull
- **Copernicus / Sentinel (ESA)** - SAR radar that sees through clouds (day/night), multispectral optical, atmospheric data. Weather-independent backup
- **USGS Landsat Archive** - 40+ years of historical imagery for baseline comparison
- **Google Earth Engine** - Cloud-based processing of massive datasets without downloading. Runs change detection algorithms
- **NOAA / GOES** - Weather overlay to explain gaps in optical imagery

### Tier 2: Freemium / Low Cost
- **ACLED** - Ground truth conflict event database (who, what, where, when, how many casualties)
- **Sentinel Hub** - Cleaner API to Sentinel data (~$25/month)
- **OpenStreetMap** - Building footprints, roads, infrastructure labels for geographic context
- **CSIS Missile Threat Database** - Known military assets mapped as GeoJSON overlay

### Tier 3: Paid Commercial (When Revenue Begins)
- **Planet Labs** (3-5m, ~$150-500/mo) - Daily passes, damage assessment
- **Maxar** (30cm) - Ultra high-res confirmation of specific sites
- **ICEYE** (sub-1m SAR) - All-weather persistent monitoring

### Tier 4: ArcGIS / Esri
Professional GIS platform for visualization, spatial analysis, and dashboard creation.

### Tier 5: Conflict Intelligence (OSINT)
- Bellingcat, OSINT analysts on X, UN OCHA humanitarian data, FlightRadar24, MarineTraffic

---

## 4. The 6-Agent Architecture (Claude Code)

The core automation system. The founder spends only **15 minutes reviewing + 10 minutes recording**. Everything else is automated by 6 AI agents:

```
6:00 AM  [Scout]           -> Flagged coordinates (FIRMS, ACLED, FlightRadar24)
6:15 AM  [Change Detector]  -> Before/after imagery, change scores 0-100
6:30 AM  [Context Linker]   -> Site identification, strategic significance
6:45 AM  [OODA Bridge]      -> Human impact analysis ("so what for you")
7:00 AM  [Narrator]         -> Complete episode script + social posts
7:15 AM  [YOU]              -> Review, approve, record voice
Post     [Distributor]      -> Scheduled push to YouTube, Substack, social
```

### Key Agent Details

**Agent 1 - The Scout:** Simple Python + cron job. Calls NASA FIRMS and ACLED APIs for a defined geographic bounding box (Iran: 24N-40N, 44E-64E). No ML needed.

**Agent 2 - Change Detector:** Most complex agent. Uses Google Earth Engine Python API to run pixel-level diffs between current imagery and 30-day baselines. Generates before/after image pairs.

**Agent 3 - Context Linker:** Queries CSIS, OpenStreetMap, ACLED, Wikipedia to answer "what is this site and why does it matter?"

**Agent 4 - OODA Bridge:** The unique intellectual layer. Translates conflict observations into human preparedness insights. Example: strait blockade -> oil disruption -> civilian energy costs -> astronaut training principles for managing scarcity.

**Agent 5 - The Narrator:** Claude Sonnet with brand voice encoded in system prompt. Produces 90-second scripts, social posts, YouTube descriptions.

**Agent 6 - The Distributor:** Post-approval automation via Buffer API, ConvertKit, YouTube Data API.

---

## 5. Build Sequence (Phased Approach)

The document prescribes a deliberate build order, each step usable before the next:

| Phase | What to Build | Time | Cost |
|-------|--------------|------|------|
| **Week 1** | Scout Agent only (FIRMS + ACLED -> email brief) | Half day | Free |
| **Week 2** | Add Context Linker (skip Change Detector - needs GEE setup) | Days | Free |
| **Week 3** | Add OODA Bridge + Narrator (Claude-powered agents) | Days | API costs |
| **Month 2** | Add Change Detector (Google Earth Engine) | Week | Free |
| **Month 3** | Add commercial satellite data (Planet Labs) | Ongoing | $150-500/mo |

**First sprint = one Python script:** call FIRMS API + ACLED API -> format as plain text -> email at 7 AM. Two APIs, one script, one email.

---

## 6. Monetization Funnel

The business model bridges free space content to paid performance training:

```
Free content (YouTube/Substack)
  -> Audience develops "OODA skill" feeling
    -> Paid morning brief ($9/mo Substack)
      -> Sponsorships ($2-5K/mo by month 4)
        -> GeForce training programs ($297 webinar -> $5-15K full program)
```

**The critical bridge statement:**
> "G-Force Space shows you how to observe the world like a systems engineer. GeForce teaches you to act on it like an astronaut. The observation without the action is just news. The action without the observation is just training. Together, it's the complete system."

---

## 7. What Only the Human Does

The architecture is designed so the founder's irreplaceable contributions are:
1. **Review** the morning brief (15 min)
2. **Record** voice/video (10 min)
3. **Make ethical judgment calls** on framing
4. **Be the face** on camera
5. **Maintain** astronaut network relationships

Everything else is automated.

---

## 8. Editorial Filter

One question gates all publishing:

> "Does this help someone understand the world better so they can prepare for a better future?"

If yes -> ship it. If "this is just war coverage for clicks" -> reframe it.

---

## Summary

G-Force Space is a **space data intelligence platform** that uses free/commercial satellite data, automated AI agents (Claude Code), and the OODA decision framework to produce daily conflict analysis content. It differentiates through a "space for good" ethical stance and bridges to revenue via the GeForce human performance training system. The entire system is designed so one person can run it with 25 minutes of daily effort.
