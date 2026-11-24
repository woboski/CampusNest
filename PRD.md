# Product Requirements Document (PRD)

## CampusNest: Hostel & Off-Campus Accommodation Finder

**Course:** BU-COS-209 (Backend Engineering)
**Team:** Group 1
**Members:** Wobo Chibitaru Marvelous (25/0599), Umoh Udeme David (25/1115), Osaigbovo Eloghosa Joan (25/1003), Osakue Joanna Otibhor (25/1257), Ukwute Onyinyechukwu Chigozie (25/1080), Uhunmwangbo Michael Ogochukwumenim (25/2315)
**Version:** 1.0
**Date:** November 24th, 2026

---

## 1. Overview

CampusNest is a platform that helps students find safe, verified, fairly priced hostels and off-campus accommodation near their university. It replaces the current mix of word-of-mouth, WhatsApp groups, and unverified agents with one trusted place to search, compare, and secure a room.

## 2. Problem Statement

Every academic session, thousands of students compete for limited on-campus beds. The rest must find housing off-campus, and the process is stressful, risky, and expensive.

Students face three core problems:

1. **Fake or misleading listings.** Photos do not match the real room, or the room is already taken.
2. **Inflated agent fees.** Agents charge heavy "commission" or "agreement" fees on top of rent, with no clear price transparency.
3. **No landlord verification.** Students pay deposits to people they cannot verify, and have no recourse if things go wrong.

## 3. Who Has This Problem? (Target Users)

### Primary users
- **Students needing housing:** fresh students (admitted, unfamiliar with the area), returning students who missed hostel allocation, and students relocating for internships or industrial training.

### Secondary users
- **Landlords and hostel owners:** want reliable tenants and to fill rooms quickly without paying agents.
- **Parents/guardians:** want assurance that their child is in a safe place.
- **Legitimate agents:** want a credible channel to list properties.

### User personas

| Persona | Description | Main pain point |
|---|---|---|
| Fresher (e.g. "Ada", 17) | New to the city, relies on a cousin or WhatsApp for leads | Cannot tell real listings from scams |
| Returning student (e.g. "Tunde", 21) | Missed hostel allocation, short on time | Agent fees and last-minute pressure |
| Landlord (e.g. "Mr. Okoro") | Owns a few rooms near campus | Hard to reach students without agents |

## 4. How Users Cope Today

- Asking seniors, friends, and relatives for leads
- Browsing WhatsApp groups, Facebook posts, and general classifieds
- Walking around the neighborhood looking for "To Let" signs
- Paying agents to show them rooms
- Settling for whatever is available because of time pressure

**Consequences:** wasted transport money and time, lost deposits to scams, overpaying, living far from campus, and unsafe or poor-quality housing.

## 5. Why Existing Solutions Fall Short

| Existing solution | Limitation |
|---|---|
| WhatsApp/Facebook groups | No verification, scams are common, listings go stale, no structured search |
| General property sites | Built for families and professionals, not students; prices are out of range; weak coverage near campuses |
| Agents | High fees, inconsistent honesty, no accountability |
| University hostel allocation | Limited capacity; many students are left out |
| Word of mouth | Limited reach, depends on who you know |

**Gap:** there is no student-focused, verified, transparent marketplace for accommodation near campus.

## 6. Research Approach, Assumptions & Validation Plan

> Our research so far is based on the team's own experience as students and on informal conversations with fellow students. We have not yet run a formal survey, so the points below are assumptions to be validated, not confirmed findings. This section will be updated as real responses come in.

### 6.1 Basis of our current understanding
- First-hand experience of the team members: searching for, or helping friends and family search for, off-campus housing
- Common patterns students talk about openly: WhatsApp-based searching, agent fees, and fake or outdated listings
- Observation of how listings are currently shared and advertised around campus

### 6.2 Core assumptions (hypotheses)

| # | Assumption | How we will validate it |
|---|---|---|
| H1 | Many students who live off-campus found their place through word of mouth, WhatsApp groups, or agents, not a dedicated platform | Ask: "How did you find your current accommodation?" |
| H2 | A significant number of students have encountered a fake, misleading, or already-taken listing | Ask: "Have you ever seen or been caught by a fake listing?" |
| H3 | Agent and "agreement" fees are often high and feel unjustified | Ask: "How much did you pay in fees on top of rent, and did it feel fair?" |
| H4 | Students do not feel able to verify who a landlord or agent really is before paying | Ask: "How did you confirm the landlord or agent was genuine?" |
| H5 | Security, distance from campus, and water/electricity matter more to students than minor price differences | Ask students to rank what matters most when choosing a place |
| H6 | Landlords would prefer to reach students directly rather than rely on agents | Short chat with 1 to 2 landlords or hostel managers |
| H7 | Students would use a platform that verifies listings and landlords | Ask: "Would you use an app that verifies landlords? What would make you trust it?" |

### 6.3 Planned validation method
Because time is limited, we will use short, low-effort methods rather than a long form:
- **Quick chat survey:** 3 questions sent by WhatsApp to 5 to 10 students (course group, hostel mates, friends living off-campus)
- **Informal interviews:** voice notes or short calls with at least 2 students and, if possible, 1 landlord or hostel manager
- **Team input:** each team member answers the same questions based on their own experience

**Core questions:**
1. How did you find your current hostel or room?
2. Have you seen a fake listing, or paid an agent fee that felt too high? How much?
3. What would make searching for accommodation easier or safer?

### 6.4 Working findings (assumed, pending validation)
These are the findings we expect to see, based on our own experience and conversations. They are labeled as assumptions and will be replaced with real responses as they are collected.

| Working finding | Status | Related hypothesis |
|---|---|---|
| Most off-campus students find housing through friends, WhatsApp groups, or agents rather than a dedicated platform | Assumed | H1 |
| A noticeable share of students have come across a fake, misleading, or already-taken listing | Assumed | H2 |
| Agent and "agreement" fees are commonly seen as high and poorly explained | Assumed | H3 |
| Students usually have no reliable way to verify a landlord or agent before paying | Assumed | H4 |
| Security, distance from campus, and water/electricity are the top concerns when choosing a place | Assumed | H5 |
| Landlords would welcome a way to reach students directly | Assumed | H6 |
| Students would be open to using a platform that verifies listings and landlords | Assumed | H7 |

### 6.5 Limitations
- Findings so far are not statistically representative and reflect a small, informal group of students
- Responses may be biased toward students in our own circles
- The MVP is designed so these assumptions can be tested early with real users, and the product scope will be adjusted if the evidence contradicts them

## 7. Proposed Solution

CampusNest is a web platform (with a mobile-friendly interface) offering:

- **Verified listings:** every landlord and property goes through a verification process before going live
- **Transparent pricing:** rent, deposit, and fees shown upfront, with no hidden agent charges
- **Smart search and filters:** by price, distance from campus, room type, amenities (water, power, Wi-Fi), and security
- **Real photos and reviews:** authentic images and ratings from past tenants
- **Secure payments (escrow):** deposit is held until the student confirms move-in
- **Roommate matching:** connect students looking to share a place
- **Report and flag system:** students can report suspicious listings

## 8. Goals & Success Metrics

| Goal | Metric | Target (first 6 months) |
|---|---|---|
| Reduce scams | Number of fraud reports per 100 listings | Fewer than 2 |
| Adoption | Registered students | _[e.g. 1,000]_ |
| Supply | Verified listings | _[e.g. 200]_ |
| Speed | Average time to find accommodation | Under 7 days |
| Trust | Average listing/landlord rating | 4.0 or higher |

## 9. MVP Definition

The Minimum Viable Product focuses only on solving the core trust and discovery problem.

### In scope (MVP)
- User registration and login (student, landlord roles)
- Landlord profile with basic verification (ID upload, manual admin approval)
- Create, edit, and delete property listings (photos, price, location, amenities)
- Search and filter listings
- Listing detail page with landlord info
- Contact/inquiry feature (message landlord or request a viewing)
- Report a listing
- Basic admin dashboard (approve landlords and listings, handle reports)

### Out of scope (future versions)
- Escrow/online payments
- Roommate matching
- In-app chat
- Mobile app (native)
- Reviews and ratings
- Map view and virtual tours

## 10. Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-1 | Users can register and log in as student or landlord | Must |
| FR-2 | Landlords can submit verification documents | Must |
| FR-3 | Admin can approve or reject landlords and listings | Must |
| FR-4 | Landlords can create and manage listings with photos | Must |
| FR-5 | Students can search and filter listings | Must |
| FR-6 | Students can view listing details and landlord profile | Must |
| FR-7 | Students can send inquiries or viewing requests | Must |
| FR-8 | Users can report suspicious listings | Should |
| FR-9 | Students can save/bookmark listings | Should |
| FR-10 | Reviews and ratings | Could |
| FR-11 | Escrow payments | Could (post-MVP) |
| FR-12 | Roommate matching | Could (post-MVP) |

## 11. Non-Functional Requirements

- **Security:** hashed passwords, role-based access, input validation, secure file uploads
- **Performance:** search results return in under 2 seconds
- **Availability:** target 99% uptime
- **Usability:** mobile-first, works on low bandwidth
- **Privacy:** protect user data and comply with applicable data protection rules (e.g. NDPA in Nigeria)
- **Scalability:** the design should support adding more campuses

## 12. User Stories

- As a **student**, I want to filter listings by price and distance so that I can find something affordable near campus.
- As a **student**, I want to see that a landlord is verified so that I do not lose money to a scam.
- As a **student**, I want to report a fake listing so that others are protected.
- As a **landlord**, I want to list my rooms so that I can reach students without paying an agent.
- As an **admin**, I want to review landlord documents so that only legitimate listings go live.

## 13. High-Level Technical Considerations

> _Per the assignment, the problem is researched first. The stack below is tentative and open to discussion._

- **Frontend:** _[TBD by team]_
- **Backend:** REST API with authentication and role-based access
- **Database:** relational database (users, landlords, listings, inquiries, reports)
- **Storage:** cloud storage for photos and documents
- **Hosting:** _[TBD]_

### Core data entities
`User`, `LandlordProfile`, `Listing`, `ListingImage`, `Inquiry`, `Report`

## 14. Risks & Mitigations

| Risk | Impact | Mitigation |
|---|---|---|
| Landlords do not sign up | No supply | Start with a few partner landlords; offer free listing at launch |
| Fake documents submitted | Loss of trust | Manual admin review; physical verification for early listings |
| Students bypass the platform | Low engagement | Provide value through search, trust, and verification |
| Data privacy issues | Legal and trust risk | Collect minimal data; secure storage |

## 15. Timeline (Proposed)

| Phase | Activity | Duration |
|---|---|---|
| 1 | Research (surveys and interviews) | Week 4 |
| 2 | Design and database schema | Week 5 |
| 3 | MVP backend build | Weeks 6 to 8 |
| 4 | Testing and pilot with students | Week 9 |
| 5 | Iterate and plan v2 | Week 10 |

## 16. Open Questions

- How will landlord verification work in practice (ID, proof of ownership, site visit)?
- What is the revenue model (listing fee, premium listings, commission)?
- Which campus do we pilot with first?

---

_End of document_