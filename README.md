#  Brikoli – Smart Mission Marketplace

##  Overview
**Brikoli** is a Moroccan digital platform that connects **clients** with **skilled professionals** for **short-term or urgent missions**.  
Unlike traditional freelance marketplaces, Brikoli focuses on **quick, task-based jobs** — such as plumbing, electrical repair, graphic design, or IT help — that can be completed within hours or days.

The platform empowers **vocational graduates (e.g., OFPPT students)** and other professionals to find paid missions easily, while clients get reliable help fast.  
AI is used to recommend the **best matches** between missions and professionals.

---

##  Vision
> Simplify short-term work connections in Morocco — make it easy for anyone to find trusted professionals for quick missions, and help skilled workers earn income efficiently.

---

##  Target Users
- **Clients:** individuals or small businesses needing help for urgent or short-term work.
- **Professionals:** skilled independent workers and OFPPT graduates looking for missions to gain experience and income.

---

##  MVP (Minimum Viable Product)

###  Objective
Validate the idea that clients will post missions and professionals will apply for them.  
The MVP focuses on simplicity, usability, and trust.

###  Core Features

#### 1. Authentication
- Register as **Client** or **Professional**
- Basic sign-up (name, email, phone, password)
- Optional: "Graduate” badge

#### 2. Create Mission (Client)
- Form with:
  - Title
  - Description
  - Category (Plumbing, Design, IT, etc.)
  - Budget range
  - Location (text or map)
  - Urgency (Normal / Urgent / ASAP)
- Post mission → visible in the public feed

#### 3. Mission Feed (Professional)
- List of active missions
- Filters: category, location, budget, urgency
- “Apply for this Mission” button

#### 4. Application System
- Professionals can apply for missions
- Clients can view applicants and **Accept** or **Decline**

#### 5. Messaging
- One-on-one chat between client and accepted professional
- Text-only chat for MVP
- Used to confirm mission details

#### 6. Mission Status
- Mission lifecycle: **Posted → In Progress → Completed**
- Client can mark mission as “Completed”

#### 7. Ratings & Reviews
- Client rates professional (1–5 stars + comment)
- Profile shows ratings and number of completed missions

#### 8. Admin Panel
- View all users, missions, and applications
- Remove fake or spam posts (future : AI filtering)

---

##  AI Integration (Post-MVP)
- **AI Matching:** Suggest best professionals for each mission based on:
  - Skills, location, response rate, and reviews
- **Smart Recommendations:** Suggest suitable missions for professionals
- **Behavior Learning:** Improve suggestions with user activity data

---

##  Payment System (Phase 2)
- Escrow model:
  - Client pays upfront
  - Funds released to professional after completion
- Supported options:
  - CMI, Wafacash, Inwi Money, Payzone, Cash on Delivery

---

##  Technology Stack Overview

Brikoli is built using a **Spring Boot + Angular** ecosystem — a reliable, enterprise-grade architecture designed for scalability, modularity, and security.

---

###  Backend — Spring Ecosystem (Java)

| Layer | Technology | Description | Why It’s Used |
|--------|-------------|--------------|----------------|
| **Core Framework** | **Spring Boot 3+** | Application entry point, REST APIs, dependency injection | Simplifies setup, modular, production-ready |
| **Web Layer** | **Spring Web (Spring MVC)** | Expose RESTful endpoints for frontend | Clean API architecture |
| **Data Layer** | **Spring Data JPA / Hibernate** | ORM for relational database | Easier CRUD + pagination support |
| **Database** | **PostgreSQL** | Relational DB for structured data | Reliable, open-source, scalable |
| **Authentication** | **Spring Security + JWT (JSON Web Token)** | Auth & role-based access | Secure token-based login |
| **Validation** | **Hibernate Validator** | Request payload validation | Automatic backend form validation |
| **Mail & Notification** | **Spring Boot Mail / Twilio / Firebase** | For mission status or OTP messages | Easy integration and scalability |
| **WebSocket / Chat** | **Spring WebSocket** | Real-time client–pro communication | Live chat and instant notifications |
| **Scheduling** | **Spring Scheduler / Quartz** | Timed tasks (auto-expire missions, reminders) | Task automation |
| **Monitoring** | **Spring Boot Actuator** | System metrics and health checks | DevOps observability |
| **Containerization** | **Docker** | Package and deploy backend microservice | Cross-platform portability |
| **AI Integration (Future)** | **Spring Boot Microservice + OpenAI API / TensorFlow** | Suggest matching professionals for missions | Personalized recommendations |

---

###  Database

| Technology | Use |
|-------------|-----|
| **PostgreSQL** | Main relational DB (missions, users, reviews, etc.) |
| **MongoDB** *(optional)* | For chat messages or flexible content storage |
| **Flyway / Liquibase** | Database versioning and migrations |

>  Choose PostgreSQL for MVP. MongoDB can be added later for chat or AI features.

---

###  Frontend — Angular Ecosystem

| Layer | Technology | Description | Why It’s Used |
|--------|-------------|--------------|----------------|
| **Framework** | **Angular 18+** | Frontend SPA framework | Scalable, modular, and enterprise-ready |
| **UI Library** | **Angular Material / PrimeNG** | Modern UI components | Fast UI development, consistent design |
| **State Management** | **NgRx (Redux pattern)** | Manage application state | Predictable and maintainable data flow |
| **Styling** | **Tailwind CSS / SCSS** | Utility-first styling | Responsive, modern styling |
| **Routing** | **Angular Router** | Client-side navigation | Supports user role-based routing |
| **API Integration** | **HttpClient + Interceptors** | Communicate securely with backend APIs | Handles JWT and error responses |
| **Realtime Updates** | **RxJS / WebSocket Client** | Reactive programming for chat and notifications | Efficient live data updates |
| **Forms** | **Reactive Forms Module** | Build complex, validated forms easily | Clean UX for mission creation and login |
| **Testing** | **Jasmine / Karma / Cypress** | Unit and end-to-end testing | Ensures reliability |
| **Deployment** | **Vercel / Netlify / Firebase Hosting** | Host Angular app globally | Fast and cost-effective delivery |

---

###  DevOps & Infrastructure

| Category | Technology | Description |
|-----------|-------------|-------------|
| **Build Tools** | Maven or Gradle | Dependency & build management |
| **Version Control** | Git + GitHub | Code management & collaboration |
| **CI/CD** | GitHub Actions | Continuous integration and automated deployment |
| **Containerization** | Docker Compose | Local orchestration (backend + frontend + DB) |
| **Monitoring** | Prometheus + Grafana *(optional)* | Backend performance and API uptime |
| **Hosting** | Render / Railway / AWS EC2 | Backend hosting |
| **Database Hosting** | ElephantSQL / Supabase | Cloud PostgreSQL hosting |

---

###  Security Practices

| Focus | Implementation |
|--------|----------------|
| **Authentication** | JWT (Bearer token) |
| **Authorization** | Role-based (CLIENT / PROFESSIONAL / ADMIN) |
| **Password Security** | BCrypt hashing |
| **CORS** | Configured via Spring Boot |
| **Data Validation** | Hibernate Validator |
| **HTTPS / SSL** | Enforced in production |

---

###  Future Extensions

| Feature | Stack |
|----------|--------|
| **AI Matching** | Spring Boot microservice + OpenAI API / TensorFlow |
| **Mobile App** | Angular + Ionic or Flutter (using same APIs) |
| **Payment Integration** | CMI, Inwi Money, Wafacash APIs |
| **Analytics Dashboard** | Angular Charts + Spring REST endpoints |
| **Admin Portal** | Angular module for admin features + Spring Admin endpoints |

---

###  Why This Stack?

1. **Scalable:** Spring Boot and Angular are enterprise frameworks built for long-term growth.  
2. **Modular:** Each feature (missions, chat, payments) can evolve into its own microservice.  
3. **Secure:** Built-in authentication, validation, and encryption support.  
4. **Developer Friendly:** Fast setup, excellent community support, easy CI/CD.  
5. **AI-Ready:** Spring Boot can easily integrate with OpenAI or TensorFlow microservices later.


---

##  Product Flow

1. **Client** posts a mission.
2. **Professionals** browse and apply.
3. **Client** reviews applications and selects one.
4. **Chat** opens for communication.
5. **Work completed** → client marks as done → rating given.
6. **AI learns** and improves future matches.

---

##  Business Model

- **Commission per mission:** 2–5% of the mission value.
- **Premium professional profiles:** visibility boost and advanced tools.
- **Advertising:** targeted ads from tool suppliers or local brands.

---

##  Future Roadmap

| Phase | Focus | Key Additions |
|-------|--------|----------------|
| **MVP** | Core posting & applying | Missions, profiles, chat, ratings |
| **Beta** | Monetization & trust | Escrow payments, verification badges, analytics |
| **Full Platform** | AI + scaling | AI matching, partnerships, mobile app |

---

##  Design Guidelines

**Core Screens:**
1. Landing Page  
2. Create Mission  
3. Mission Feed  
4. Mission Detail (Applications)  
5. Client Dashboard  
6. Professional Dashboard  
7. Chat Screen  
8. Rating Screen  

---

##  MVP Success Metrics
- ≥ 20 missions posted per week
- ≥ 50 professionals applying regularly
- ≥ 5 completed missions per week
- Positive feedback from both sides

---

## 🇲🇦 Social Impact
Brikoli will:
- Help **graduates** earn and gain experience.
- Create opportunities for **freelancers** in urban and rural Morocco.
- Digitize the informal service economy with trust and transparency.

---


#  Brikoli — Market Evidence & Risks

> A data-backed overview of the opportunity for Brikoli — a short-mission marketplace connecting clients with skilled professionals and OFPPT graduates in Morocco.

---

##  Executive Summary

**Brikoli** aims to digitize and simplify the way Moroccans find help for short-term or urgent work.  
With high smartphone usage, strong vocational training infrastructure, and persistent unemployment among graduates, Morocco offers a fertile environment for a **mission-based platform economy**.

This document presents:
-  Real **market statistics** (with sources)
-  Main **risks and challenges**
-  **Validation experiments** to strengthen the business case

---

##  Market Statistics (with Sources)

### 1. Internet & Smartphone Reach
- Morocco had **34.5 million internet users** at the start of 2024.  
- Internet penetration rate: **≈ 90.7%** of the population.  
  **→ Source:** [DataReportal – Digital 2024: Morocco](https://datareportal.com/reports/digital-2024-morocco)

>  Interpretation: A high percentage of connected users ensures accessibility for a web/mobile platform like Brikoli.

---

### 2. Vocational Training (OFPPT) Supply
- Over **678,000 trainees** began vocational training in the **2024–2025** academic year.  
- OFPPT manages **2,250 training centres** across the country.  
  **→ Source:** [Barlamantoday (2024)](https://barlamantoday.com/2024/09/05/over-670000-trainees-begin-2024-2025-year-at-vocational-training-centers/)

- Since 2000, **≈ 680,000 graduates** have come from **private vocational centres**.  
  **→ Source:** [Morocco World News (2019)](https://www.moroccoworldnews.com/2019/12/74593/680000-moroccans-graduates-private-vocational-training)

>  Interpretation: A large pool of trained professionals represents the “supply side” of Brikoli.

---

### 3. Graduate & Youth Unemployment
- National unemployment rate (2024): **13.3%**  
- Unemployment among **graduates**: **≈ 19.6%**  
  **→ Source:** [Reuters (Feb 2025)](https://www.reuters.com/world/africa/moroccos-unemployment-rate-rises-133-2024-drought-hits-farmers-2025-02-03)

>  Interpretation: Many trained workers remain underemployed — a strong incentive to accept short-term missions.

---

### 4. Platform Economy & Digital Work Trends
- The **gig/platform economy** is growing in Morocco.  
- Academic and NGO studies (e.g., **Fairwork Morocco**) highlight both the potential and challenges of fair digital work.  
  **→ Source:** [Fairwork Morocco Project](https://fair.work/en/fw/research/morocco/)

>  Interpretation: Public awareness of gig platforms is rising, and there’s room for ethical, locally adapted models.

---

### 5. Home & Service Market Demand
- Global home-services and handyman markets show consistent growth (≈7–10% CAGR).  
- Moroccan demand follows similar urbanization and modernization trends.  
  **→ Source:** [Market Research Future, 2023 Report](https://www.marketresearchfuture.com/reports/handyman-services-market-11108)

>  Interpretation: Rising demand for convenience and verified professionals supports Brikoli’s business model.

---

##  What These Numbers Mean

| Factor | Meaning for Brikoli |
|--------|----------------------|
| **High connectivity** | Large reachable market via mobile/web apps |
| **Many OFPPT graduates** | Abundant professional supply ready for work |
| **Graduate unemployment** | Motivated user base seeking short gigs |
| **Growing gig awareness** | Easier market entry; people know the concept |
| **Home-service demand** | Strong early traction potential in cities |

---

##  Key Risks & Challenges

### 1. Trust & Quality Control
- **Issue:** Clients need assurance that professionals are competent and reliable.  
- **Risk:** One bad experience can erode trust.  
- **Mitigation:** OFPPT verification badges, ratings, ID checks, and escrow system.

---

### 2. Two-Sided Marketplace Balance
- **Issue:** Matching enough professionals to missions in each city.  
- **Risk:** One-sided activity reduces engagement.  
- **Mitigation:** Start local (Casablanca pilot), OFPPT partnerships, launch incentives.

---

### 3. Payments & Cash Preference
- **Issue:** Many Moroccans prefer cash payments.  
- **Risk:** Low adoption of online escrow systems.  
- **Mitigation:** Integrate local options (CMI, Wafacash, Inwi Money), allow “cash-on-completion” for early users.

---

### 4. Regulation & Worker Protection
- **Issue:** Platform work is being reviewed by regulators.  
- **Risk:** Future legal requirements on contracts or insurance.  
- **Mitigation:** Comply with Fairwork standards, transparent terms, legal advisory.

---

### 5. Competition & Informal Market
- **Issue:** Facebook/WhatsApp groups and classifieds dominate.  
- **Risk:** Users may prefer familiar informal channels.  
- **Mitigation:** Focus on **speed**, **AI matching**, **trust**, and **official certification**.

---

### 6. Cancellations & Reliability
- **Issue:** No-shows or unconfirmed missions can cause friction.  
- **Mitigation:** Add penalties for cancellations, backup professionals, check-in confirmations.

---

### 7. Data & Privacy
- **Issue:** Managing personal data and location securely.  
- **Mitigation:** Use HTTPS, store minimal data, follow Moroccan privacy laws.

---

##  Validation Experiments (Low-Cost)

| Experiment | Goal | Description |
|-------------|------|--------------|
| **Pilot with 1 OFPPT Center** | Test engagement | 50 professionals, 200 missions in Casablanca |
| **Facebook/WhatsApp Ads** | Validate client demand | Measure mission post conversions |
| **Cash vs. Prepaid Test** | Test payment habits | Offer both methods, track preference |
| **User Interviews (20+20)** | Understand trust & pricing | Talk to clients and professionals directly |

---

##  Sources

- [DataReportal – Digital 2024: Morocco](https://datareportal.com/reports/digital-2024-morocco)  
- [Barlamantoday (2024)](https://barlamantoday.com/2024/09/05/over-670000-trainees-begin-2024-2025-year-at-vocational-training-centers/)  
- [Morocco World News (2019)](https://www.moroccoworldnews.com/2019/12/74593/680000-moroccans-graduates-private-vocational-training)  
- [Reuters (2025)](https://www.reuters.com/world/africa/moroccos-unemployment-rate-rises-133-2024-drought-hits-farmers-2025-02-03)  
- [Fairwork Morocco Project](https://fair.work/en/fw/research/morocco/)  
- [Market Research Future (2023) – Handyman Services Report](https://www.marketresearchfuture.com/reports/handyman-services-market-11108)

---

## 🇲🇦 Final Outlook

The Moroccan market is **ripe for short-mission digital work**:
- High internet penetration  
- Abundant trained professionals  
- Persistent unemployment  
- Strong urban service demand  

With careful attention to trust, regulation, and local payment habits, **Brikoli** can become the **go-to platform for mission-based work in Morocco**.

---


---

##  Contributors
**Project Owner:** ismail baoud

---

##  Contact
For collaboration or investment inquiries:  
 **ismailBaoud04@gmail.com**  
 **www.brikoli.*** *(coming soon)*

---
# BRIKOL-PLATFORM
