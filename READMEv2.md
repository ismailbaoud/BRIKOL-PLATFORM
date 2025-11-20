# Brikoli – Smart Mission Marketplace

**Brikoli** is a Moroccan digital platform connecting clients with skilled professionals for **short-term, urgent missions**. Unlike traditional freelance marketplaces, Brikoli focuses on **quick, task-based jobs** — such as plumbing, electrical repair, graphic design, or IT help — that can be completed within hours or days.  

The platform empowers vocational graduates (e.g., OFPPT students) and other professionals to **find paid missions easily**, while clients get **reliable help fast**. AI is planned for future iterations to recommend the best matches between missions and professionals.

---

## Vision

- Simplify short-term work connections in Morocco.  
- Make it easy for anyone to find **trusted professionals** for urgent or short missions.  
- Help skilled workers earn income efficiently.  
- Digitize the informal service economy with **trust, transparency, and accountability**.

---

## Target Users

- **Clients:** Individuals or small businesses needing help for urgent or short-term work.  
- **Professionals:** Skilled independent workers and OFPPT graduates looking for missions to gain experience and income.

---

## Core Problems Brikoli Solves

1. **Trust:** Verified professionals increase confidence.  
2. **Reliability:** Professionals arrive on time and complete jobs.  
3. **Communication:** Guided mission forms reduce miscommunication.  
4. **Pricing:** Standardized price ranges reduce conflicts.  
5. **Cash Preference:** Cash-on-completion accommodates local habits.  
6. **Accountability:** Ratings, reliability scores, and backup professionals ensure accountability.  
7. **No-Shows:** Backup professional system ensures missions are never left incomplete.  

---

## Minimum Viable Product (MVP)

### Objective
Validate the concept that clients post missions and professionals apply, with a focus on **simplicity, usability, and trust**.

### Core Features

#### 1. Authentication
- Register as Client or Professional  
- Basic info: name, email, phone, password  
- Optional: “Graduate Verified” badge (OFPPT verification)  

#### 2. Create Mission (Client)
- Title, description, category (Plumbing, IT, Design, etc.)  
- Budget range, location (text/map), urgency (Normal / Urgent / ASAP)  
- Guided mission diagnosis flow to define the problem accurately  
- Posted missions appear in the professional feed  

#### 3. Mission Feed (Professional)
- List of active missions  
- Filters: category, location, budget, urgency  
- “Apply for this Mission” button  

#### 4. Application System
- Professionals apply → clients accept or decline  

#### 5. Chat
- One-on-one real-time chat between client and professional  
- Text-only for MVP  
- Used to confirm mission details  

#### 6. Mission Status
- Lifecycle: Posted → In Progress → Completed  
- Client marks mission as “Completed”  

#### 7. Ratings & Reliability
- Client rates professional (1–5 stars + comment)  
- Reliability Score based on completion, punctuality, and reviews  
- Professionals ranked with badges: Gold, Diamond, Brikoli Guarantee  

#### 8. Backup Professionals
- Auto-assign backup professional if main cancels  
- Ensures mission completion and client satisfaction  

#### 9. Admin Panel
- View all users, missions, applications  
- Remove fake or spam posts  
- Manage verification badges  

---

## Technology Stack

### Backend (Spring Boot Ecosystem)
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Core | Spring Boot 3+ | Application entry point, REST APIs |
| Web | Spring Web (MVC) | Expose REST endpoints |
| Data | Spring Data JPA / Hibernate | ORM for relational DB |
| Database | PostgreSQL | Structured data storage |
| Auth | Spring Security + JWT | Role-based authentication |
| Validation | Hibernate Validator | Request validation |
| Chat | Spring WebSocket | Real-time messaging |
| Scheduler | Spring Scheduler / Quartz | Auto-expire missions, reminders |
| Monitoring | Spring Boot Actuator | System metrics and health checks |
| Containerization | Docker | Deployment portability |
| AI Integration | Spring Boot Microservice + OpenAI/TensorFlow | Future smart matching |

### Frontend (Angular Ecosystem)
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Framework | Angular 18+ | SPA development |
| UI Library | Angular Material / PrimeNG | Modern UI components |
| State Management | NgRx | Predictable data flow |
| Styling | Tailwind CSS / SCSS | Responsive modern styling |
| Routing | Angular Router | Role-based client/professional routing |
| API Integration | HttpClient + Interceptors | Secure backend communication |
| Realtime Updates | RxJS / WebSocket Client | Live chat, notifications |
| Forms | Reactive Forms Module | Complex validated forms |
| Testing | Jasmine / Karma / Cypress | Unit & E2E testing |
| Deployment | Vercel / Netlify / Firebase Hosting | Global hosting |

### DevOps & Infrastructure
- **Build Tools:** Maven / Gradle  
- **Version Control:** Git + GitHub  
- **CI/CD:** GitHub Actions  
- **Containerization:** Docker Compose  
- **Hosting:** Render / Railway / AWS EC2  
- **Database Hosting:** ElephantSQL / Supabase  

---

## Security Practices
- JWT Authentication & role-based access  
- Password encryption (BCrypt)  
- HTTPS/SSL enforced in production  
- Data validation via Hibernate Validator  
- CORS configured in backend  

---

## Future Extensions
- AI-based **Mission Matching** and **Smart Recommendations**  
- **Mobile App** (Angular + Ionic / Flutter)  
- Escrow-based **Payment Integration** (CMI, Wafacash, Inwi Money)  
- **Analytics Dashboard** for clients and professionals  
- Enhanced **Admin Portal** with AI moderation  

---

## Product Flow
1. Client posts mission.  
2. Professionals browse and apply.  
3. Client selects professional → chat opens.  
4. Mission completed → client marks as done → rating given.  
5. AI learns and improves future matches.  

---

## Business Model
- Commission per mission: 2–5%  
- Subscription for professionals: visibility boost, verified badge  
- Advertising: local suppliers, tool brands  

---

## Social Impact
- Helps graduates earn experience and income  
- Creates opportunities for freelancers in urban and rural Morocco  
- Digitizes informal service economy with trust and transparency  

---

## Market Insights
- **Internet penetration:** 90%+ in Morocco  
- **OFPPT graduates:** 678,000+ trainees annually  
- **Graduate unemployment:** ~20%  
- **Home-service demand:** growing steadily  
- **Platform awareness:** rising, opportunity for local adaptation  

**Key Risks & Mitigation**
| Risk | Mitigation |
|------|------------|
| Trust & Quality | Verified badges, reliability score, ratings |
| Two-sided marketplace | Start local (Casablanca), partnerships |
| Payments | Cash-on-completion, local payment integration |
| Regulation | Fairwork compliance, transparent terms |
| Informal competition | Speed, trust, AI matching |
| No-shows | Backup professional feature |
| Data privacy | HTTPS, minimal data storage, Moroccan privacy laws |

---

## MVP Success Metrics
- ≥ 20 missions posted per week  
- ≥ 50 professionals applying regularly  
- ≥ 5 completed missions per week  
- Positive feedback from both clients and professionals  

---

## Contributors
**Project Owner:** Ismail Baoud  
**Contact:** ismailBaoud04@gmail.com  
**Website:** [www.brikoli.*](#) *(coming soon)*

