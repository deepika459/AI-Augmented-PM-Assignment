
# Sprint 1 – Smart Support Portal (High-Level)

## Objective

Deliver the basic working version of the support portal where users can log in and raise support tickets, and agents can manage them.

**Duration:** 2 weeks  

**Sprint Goal:** Basic ticketing workflow operational

## Work Items

### 1. Login & Authentication

**User Story:**  
User can log in to access the support portal.

**Tasks**

- Login page

- Credential validation

- Session/token creation

- Logout

### 2. Role-Based Access Control

**User Story:**  
System provides different access to Admin, Agent, and User.

**Tasks**

- Define roles
    
- Assign role to users
    
- Restrict pages based on role
    

### 3. Ticket Creation

**User Story:**  
User can raise a support request.

**Tasks**

- Ticket form
    
- Category & description
    
- Generate ticket ID
    
- Save ticket
    

### 4. Agent Dashboard

**User Story:**  
Agent can view and update tickets. The control panel where support agents see all user issues and work on resolving them

**Tasks**

- Ticket list view
    
- Change ticket status
    
- Assign ticket
    
- View ticket details
    

### 5. Notification

**User Story:**  
User receives confirmation after ticket creation.

**Tasks**

- Email/SMS confirmation
    
- Trigger on ticket creation

### 6. Testing

**Tasks**

- Functional testing
    
- Fix bugs
    
- Basic UAT

## Sprint 1 Deliverable

- User login works
    
- Tickets can be created
    
- Agents can manage tickets
    
- User gets confirmation notification

## What is NOT included (later sprints)

- AI chatbot
    
- Knowledge base articles
    
- Analytics dashboard


# Schedula MVP 

### Doctor Appointment Scheduling

**Epic:** **Schedula MVP – Appointment Management**

**Description**: This scheduler is for doctor appointment system, where we will be creating stories with priorities high/medium/low  where epic will be linked to user stories and stories to task, maintaining a proper order.
This epic allows a doctor to publish consultation availability and enables patients to book appointment slots. The system ensures that appointments are scheduled without overlap and patients are properly informed about their visit.

**Business Goal:**  
Reduce waiting time at clinic and avoid missed appointments.

**User Stories**
**Story 1 :** **Provider sets availability(High - Must Have)**

1. **Description:** Setting consultation hours so that patients can book appointment only when doctor is available.

2. **Tasks**
- Doctor login (Authentication based)
    
- Add clinic working days (Mon–Sat)
    
- Set start time and end time (for eg:  10 AM – 5 PM)
    
- Define consultation duration (for e.g., 15 min per patient)
    
- Auto-generate appointment slots
    
- Save availability in database
    
- Block specific dates (leave/holiday)
    
- Validate overlapping timings

**User Story 2 : Patient books appointment (MEDIUM - Should Have)
**

1. **Description:** Patient can view available appointment slots and select a suitable time so that they can visit the doctor without waiting.

 2. **Tasks**
- Patient selects doctor
    
- Fetch available slots API
    
- Show calendar with dates
    
- Show only free slots
    
- Prevent past date booking
    
- Create appointment record
    
- Prevent double booking
    
- Show booking confirmation screen

**User Story 3 — SMS reminder to patient (LOW – Could Have)**

 1. **Description:** patient should receive an SMS reminder before the appointment so that they can remember to visit the clinic on time.

 2. **Tasks**

- Integrate SMS gateway
    
- Send confirmation SMS after booking
    
- Schedule reminder SMS (e.g., 24 hrs before visit)
    
- Handle SMS failure retry
    
- Send cancellation SMS if appointment changed
    
- Maintain notification log

## Analyzing PERT Formula

Applying formula on below task :

**Story 1 :** **Provider sets availability(High - Must Have)**

1. **Description:** Setting consultation hours so that patients can book appointment only when doctor is available.

2. **Tasks**
	Doctor login (Authentication based) 

**Break “Doctor Login” into small activities**
- Login UI page
    
- Validate credentials (email/phone + password)
    
- Database user verification
    
- Session/JWT token creation
    
- Error handling (invalid login)
    
- Logout
**Estimating values (O, M, P)**

| Activity               | Optimistic (O) | Most Likely (M) | Pessimistic (P) |
| ---------------------- | -------------- | --------------- | --------------- |
| Login UI page          | 2h             | 4h              | 6h              |
| Credential validation  | 2h             | 5h              | 8h              |
| DB verification        | 1h             | 3h              | 6h              |
| Token/session creation | 2h             | 4h              | 8h              |
| Error handling         | 1h             | 3h              | 5h              |
| Logout                 | 1h             | 2h              | 4h              |
TE=(O+4M+P)/6
 1) Login UI :(2+4×4+6)/6=(2+16+6)/6=24/6=4h
 2) Credential Validation : (2+4×5+8)/6=(2+20+8)/6=30/6=5h
 3) Database Verification : (1+4×3+6)/6=(1+12+6)/6=19/6≈3.2h
 4) Token/session creation : (2+4×4+8)/6=(2+16+8)/6=26/6≈4.3h
 5) Error Handling : (1+4×3+5)/6=(1+12+5)/6=18/6=3h
 6) Logout : (1+4×2+4)/6=(1+8+4)/6=13/6≈2.2h
**So, total estimated time came out is => 4 + 5 + 3.2 + 4.3 + 3 + 2.2 ≈ 21.7 hours**
**≈ 22 hours == 3 working days in total.**

