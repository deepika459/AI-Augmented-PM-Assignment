Presenter: Deepika Kumari
Project: Schedula (Salon booking App)

### Crisis 1 Report: Scope Creep Emergency (12 min)

#### Scenario summary

- **Date:** February 18, 2026
- **Time:** 9:00 AM
- **Client request (email):** Add WhatsApp booking before launch next week, plus:
    - Google Calendar sync
    - Automatic birthday discount coupons
    - Instagram integration for booking via DMs
- **Current delivery reality:**
    - Sprint 3 (final sprint before launch)
    - 6 days until launch demo
    - Velocity: 19 points per sprint
    - Remaining work: 18 points (already at capacity)

---

#### 1) Problem statement

The client is requesting multiple new “must-have” features one week before launch, even though the team is already at full capacity, creating a high risk of missed launch/demo or degraded quality.

---

#### 2) Root cause analysis (3 Whys)

1. **Why is this happening now (one week before launch)?**
    
    Because the client is discovering and prioritizing competitive and customer-driven feature requests late in the cycle.
    
2. **Why were these expectations not managed earlier?**
    
    Because scope boundaries and a formal change control process for late requests were not clearly established (or not enforced) with the client.
    
3. **Why wasn’t there a firm scope agreement and prioritization method?**
    
    Because success criteria for the launch (MVP definition, what “must-have” means, and trade-offs between scope, time, and quality) were not aligned in a written agreement and recurring checkpoints.
    

---

#### 3) Response options (3 options with trade-offs)

#### Option A — Say “No” to new scope for launch (defer all requests)

**What we do:** Confirm launch scope is frozen. Add requests to a post-launch backlog with dates for review.

**Pros:** Protects demo date and quality. Reduces risk and team burnout.

**Cons:** Client may feel unheard. Competitive/customer pressure remains unresolved in the short term.

#### Option B — “Yes, but trade-off”: Swap scope (replace existing items with 1 new feature)

**What we do:** Offer to take **only one** of the three requests for launch by removing an equivalent amount of planned work (points) from Sprint 3.

**Pros:** Client gets something meaningful. Keeps schedule realistic.

**Cons:** Some previously planned items get cut. Requires strong prioritization and client sign-off.

#### Option C — Fast, limited workaround (manual or semi-manual “concierge MVP”)

**What we do:** Implement a lightweight interim solution, such as:

- WhatsApp booking as a “Click to WhatsApp” button with a structured message template (no full workflow automation), or
- Instagram DM handled manually with a standardized intake script

**Pros:** Meets the “we have it” expectation with minimal engineering. Low risk to launch.

**Cons:** Not scalable. Operational overhead. Not a true integration.

---

#### 4) Recommendation 

**Recommend Option B + Option C hybrid:**

- Commit to one highest-impact request only if it can fit by swapping scope (Option B).
- For the other requests, offer a manual/lightweight workaround for launch (Option C), with a clear post-launch plan.

	**Rationale:** Because we only have six days left and the team is already fully booked, taking on all three requests now would put the launch demo and overall quality at risk. This plan keeps us on track for the launch while still making sure we address what the client cares about.

---

#### Suggested “decision meeting” output

- “We can include one item before launch if we remove an equivalent amount of planned work.”
- “For the other items, we can provide a launch-safe workaround and schedule the full integrations immediately after launch.”

---
## CRISIS 2: Team Conflict Scenario

**Problem:**  
Booking page implementation is delayed and team members (Developer, Designer, QA) are blocked due to continuous design changes and lack of clarity on which version should be implemented and tested.
## Root Cause - 5 Whys Analysis

**Why 1 - Why is the booking page delayed?**  
Because development keeps re-implementing UI multiple times and QA cannot start testing.

**Why 2 - Why is development re-implementing UI?**  
Because design specifications are changing after development has already started coding.

**Why 3 - Why are designs changing after development started?**  
Because accessibility validation (contrast/usability) is happening _after_ handoff to development.

**Why 4 - Why is accessibility validation happening late?**  
Because there is no formal design approval or sign-off stage before development begins.

**Why 5 - Why is there no design sign-off stage?**  
Because the team lacks a defined handoff process between Design → Development → QA.

### Root Cause (Actual)

**Missing design handoff and approval workflow — not color contrast itself.**  
The issue is a _process failure_, not a person’s mistake.
### Immediate Fix

**Tell Rajesh** - **Developer**

-  Stop reworking colors repeatedly.
    
- Implement layout structure (components, spacing, responsiveness) but keep colors configurable via CSS variables/theme tokens.
    
- Wait for final approved design before final styling.
    
- Continue work on non-blocked modules (API integration, validation logic, booking rules).

**Tell Priya** - **Quality Assurance**

- Perform accessibility and contrast testing before handing off the design.
    
- Provide:
    
    - Final Figma link
        
    - Exact color codes
        
    - Font sizes
        
    - Component states (hover, error, disabled)
        
- Mark the design as **“DEV READY”** once validated.

**Tell Amit** - **Tester**

- Do not wait idle.
    
- Start preparing:
    
    - Test cases
        
    - Accessibility checklist
        
    - Booking validation scenarios
        
- Begin testing backend functionality and logic while UI finalization is pending.

#### Process Change (Prevention Strategy)

#### New Rule — “Design Handoff Protocol”

Before development starts, design must include:

1. Final Figma link
    
2. Accessibility-checked colors
    
3. Responsive layout
    
4. Component states (error, hover, disabled)
    
5. PM approval

Only after this → story moves to **Ready for Development**

#### Workflow Update

Design → PM Approval → Dev → QA

--- 

## CRISIS 3 RESPONSE

#### 5 Whys

**Why 1:** Why are invalid bookings allowed?  
→ Because the system is not validating business rules for booking time slots.

**Why 2:** Why are business rules not validated?  
→ Backend validation for booking constraints (closing hours, holidays, minimum duration, stylist availability) was not implemented.

**Why 3:** Why was backend validation not implemented?  
→ The team relied mainly on frontend validation and assumed salon owners would enter correct timings.

**Why 4:** Why did the team rely only on frontend validation?  
→ Requirements for server-side validation and edge cases were not clearly documented in acceptance criteria.

**Why 5:** Why were acceptance criteria incomplete?  
→ No domain rule checklist or QA review was done during requirement finalization for booking logic.

**Root Cause:**  
Missing server-side validation and incomplete requirement definition for booking business rules.

---

### Demo Strategy Tomorrow: 

- Use a pre-configured salon account with valid working hours only.
    
- Demonstrate booking only between allowed times (e.g., 10 AM – 7 PM).
    
- Avoid showing holiday booking, overlapping booking, or manual slot editing.
    
- Explain to client: “We are currently validating advanced edge cases and they will be included before launch.”

---

### Client Message: 

We found a bug in some of the more complex booking checks, especially around edge cases like holidays and overlapping appointments. The main booking flow is working well and we will be showing it in tomorrow’s demo. We are adding extra protections now, and the fix will be finished before launch, so bookings will stay correct and dependable for customers.

---

### 3-Day Action Plan

**Day 1:**

- Immediately freeze new feature work.
    
- Assign 1 backend + 1 QA + 1 frontend dev to booking validation fix.
    
- Implement server-side validation for:
    
    - closing hours
        
    - minimum duration (30 min)
        
    - stylist availability
        

**Day 2:**

- Add holiday calendar validation
    
- Add overlapping booking prevention
    
- QA regression testing on booking flow
    
- Create test cases for all edge conditions
    

**Day 3:**

- UAT testing with staging data
    
- Client verification demo (optional)
    
- Deploy fix to production
    
- Monitor booking logs for errors