<h1 align="center">Hi, I'm Kelsey Saul 👋</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=61DAFB&center=true&vCenter=true&width=600&lines=Lead+UI%2FUX+Designer;Full-Stack+Web+Developer;Figma+%E2%86%92+React+%E2%86%92+NestJS+%E2%86%92+Kotlin;Fleet-tracking+%7C+Fintech+%7C+Payments" alt="Typing SVG" />
  </a>
</p>

<p align="center">
  I design and build products end-to-end — from Figma prototypes to production React, NestJS, and Kotlin apps — with a focus on fleet-tracking, fintech, and payments tools for East African users.
</p>

<p align="center">
  <a href="https://inkwell-sandy.vercel.app/#home">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://www.linkedin.com/in/kelsey-nakitare-72562b1a8/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
</p>

---

### 🛠️ Tech Stack

| Category | Technologies |
| :--- | :--- |
| **Frontend & Design** | ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white) ![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white) |
| **Backend & APIs** | ![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white) ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white) ![M-Pesa Daraja](https://img.shields.io/badge/M--Pesa_Daraja_API-4CAF50?style=for-the-badge&logo=safaricom&logoColor=white) |
| **Databases & Caching** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white) ![PostGIS](https://img.shields.io/badge/PostGIS-336791?style=for-the-badge&logo=postgresql&logoColor=white) ![Supabase](https://img.shields.io/badge/Supabase-1C1C1C?style=for-the-badge&logo=supabase&logoColor=00C485) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white) |
| **Mobile** | ![Kotlin](https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white) ![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=for-the-badge&logo=android&logoColor=white) |
| **Maps & Telematics** | ![Mapbox](https://img.shields.io/badge/Mapbox-000000?style=for-the-badge&logo=mapbox&logoColor=white) ![Traccar](https://img.shields.io/badge/Traccar_Cloud-1E88E5?style=for-the-badge&logo=googlemaps&logoColor=white) |
| **Deployment & Tools** | ![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) |

<p align="center">
  <img src="https://skillicons.dev/icons?i=react,ts,tailwind,figma,nodejs,nestjs,postgres,supabase,redis,kotlin,vercel,git,github&perline=13" alt="Animated tech stack" />
</p>

---

### 📁 Projects

#### 🛰️ [Venus — Fleet Management Platform](https://venus.trackalways.cloud/live-map)

Venus is the customer-facing brand of the Fleetpro fleet management platform: a real-time system for tracking and managing 600+ vehicles, devices, and drivers. I lead the design and development of "Venus OS" — its cross-platform UI — including the live map with geofencing and POIs, fleet KM analytics, fuel/video/driver hubs, and **Venus AI**, an integrated assistant that lets operators query vehicle statuses in natural language. *(Closed source — happy to walk through the architecture.)*

<p align="center">
  <img src="venus-livemap.png" alt="Venus live map tracking 600+ vehicles across Kenya" width="49%" />
  <img src="venus-dashboard.png" alt="Venus dashboard with fleet KM summary and mileage breakdown" width="49%" />
</p>

<details>
<summary><b>🏗️ Architecture Overview</b></summary>

```mermaid
flowchart LR
    subgraph Devices["🚗 Field Layer"]
        GPS["GPS / Telematics<br/>Units (600+)"]
    end

    subgraph Ingest["📡 Ingestion"]
        TRACCAR["Traccar Cloud"]
    end

    subgraph Backend["⚙️ Backend Services"]
        API["NestJS API"]
        AI["Venus AI<br/>NL Query Engine"]
        CACHE["Redis Cache"]
    end

    subgraph Data["🗄️ Data Layer"]
        PG["PostgreSQL"]
        GIS["PostGIS<br/>Geofences / POIs"]
    end

    subgraph Client["🖥️ Venus OS"]
        WEB["Live Map + Analytics<br/>Fuel / Video / Driver Hubs"]
    end

    GPS --> TRACCAR --> API
    API --> CACHE
    API --> PG
    API --> GIS
    API --> AI
    AI --> WEB
    API --> WEB
```

</details>

#### 🚙 Carpool — Internal Ride & Fleet System

A fleet-tracking and internal ride-request system built on a NestJS backend, PostgreSQL with PostGIS for spatial queries, Redis for caching, and Traccar Cloud for telematics — with dedicated web and mobile codebases in a structured monorepo.

**Web dashboard**

<p align="center">
  <img src="carpool (2).png" alt="Carpool fleet vehicles dashboard with live map" width="49%" />
  <img src="carpool (3).png" alt="Carpool requests overview and reports" width="49%" />
</p>

**Mobile app**

<p align="center">
  <img src="carpool (1).png" alt="Carpool trip notifications on mobile" width="28%" height="30%"/>
  <img src="carpool (4).png" alt="Carpool request queue on mobile" width="28%" />
  <img src="carpool (5).png" alt="Carpool user management on mobile" width="28%" />
</p>

<details>
<summary><b>🏗️ Architecture Overview</b></summary>

```mermaid
flowchart TB
    subgraph Clients["📱 Client Apps"]
        WEB["Web Dashboard"]
        MOBILE["Mobile App"]
    end

    subgraph Mono["📦 Monorepo"]
        NEST["NestJS API"]
    end

    subgraph Services["🔧 Services"]
        REDIS["Redis<br/>Caching"]
        TRACCAR["Traccar Cloud<br/>Telematics"]
    end

    subgraph Store["🗄️ PostgreSQL + PostGIS"]
        RIDES["Ride Requests"]
        SPATIAL["Spatial Queries"]
    end

    WEB --> NEST
    MOBILE --> NEST
    NEST --> REDIS
    NEST --> TRACCAR
    NEST --> RIDES
    NEST --> SPATIAL
```

</details>

#### 🌍 [Trackalways Africa](https://trackalwaysafrica.com/)

Official web presence and digital branding for Trackalways Africa. Designed and developed to showcase enterprise fleet telematics, fuel management, and AI-driven tracking solutions across East Africa with a sleek, high-conversion UI and responsive performance.

<p align="center">
  <img src="Screenshot 2026-07-29 150206.png" alt="Trackalways Africa Web Showcase 1" width="49%" />
  <img src="Screenshot 2026-07-29 150309.png" alt="Trackalways Africa Web Showcase 2" width="49%" />
</p>

#### 🔵 [Cirqle Labs](https://cirqlelabs.vercel.app/)

Modern design studio and software venture landing page built with high-impact micro-interactions, responsive layout systems, and modern UI engineering standards to showcase product design and full-stack development capabilities.

<p align="center">
  <img src="Screenshot 2026-07-29 150519.png" alt="Cirqle Labs Landing Showcase 1" width="49%" />
  <img src="Screenshot 2026-07-29 150546.png" alt="Cirqle Labs Landing Showcase 2" width="49%" />
</p>

#### ⚡ Zipp — Payments Super App

A Kenyan payments super app concept with a bold yellow/black/deep-blue brand: send to Zipp users or M-Pesa, Paybill/Till, QR payments, bills, travel booking, and **Palm Pay** palm-vein biometric authentication as its core differentiator. Designed mobile-first with Kotlin and Jetpack Compose in mind.

<details>
<summary><b>🏗️ Architecture Overview</b></summary>

```mermaid
flowchart TB
    subgraph App["📱 Zipp Mobile — Kotlin / Jetpack Compose"]
        UI["Compose UI"]
        PALM["Palm Pay<br/>Palm-Vein Biometrics"]
    end

    subgraph Core["💳 Payment Core"]
        WALLET["Wallet / P2P"]
        QR["QR Payments"]
        BILLS["Bills & Travel"]
    end

    subgraph Rails["🔗 Payment Rails"]
        MPESA["M-Pesa<br/>Send / Paybill / Till"]
    end

    UI --> WALLET
    PALM --> WALLET
    UI --> QR
    UI --> BILLS
    WALLET --> MPESA
    QR --> MPESA
    BILLS --> MPESA
```

</details>

#### 🏠 [Home Matchmaker](https://realestate-nu-gray.vercel.app/)

Full-stack student housing app with swipe-to-match discovery and automated in-app payments via the M-Pesa Daraja API (React, Node.js, Supabase).

#### 🍲 [AfriFood](https://afrifood.vercel.app/)

Web and mobile recipe platform celebrating traditional African cuisine — database-driven with a custom relational schema in Supabase and heavily optimized image rendering.

#### 🔬 [Kenya Science Leadership Programme](https://www.kenyascienceleadershipprogram.co.ke/)

Web revamp and public-facing digital media assets for a national science leadership programme.

---

### 🙋 About Me

- 🏀 Competitive basketball player when I'm away from the keyboard
- 🎓 BSc in Business Information Technology, Kabarak University
- 📜 Certified in Cisco Networking & Cybersecurity (CCNA) and IBM Data & AI Fundamentals
- 💬 Ask me about UI/UX systems, React state management, M-Pesa integrations, or Kotlin/Compose workflows

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=KelseySaul&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Kelsey's GitHub Stats" height="165" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=KelseySaul&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="165" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=KelseySaul&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages" height="165" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=KelseySaul&theme=tokyo-night&hide_border=true&area=true" alt="Contribution Activity Graph" />
</p>
