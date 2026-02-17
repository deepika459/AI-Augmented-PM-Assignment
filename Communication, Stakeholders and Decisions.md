
**Presenter:** Deepika Kumari
**Context Project :** Schedula (Salon Booking App)

As a Project Manager, things matters in todays time.
1. Clear Communication -> Verbally and Written
2. Know how to handle the Stakeholders
3. Making Decision when no perfect answer is present.

### PM Messy v/s Clear Answer
### **Exercise** 1
**Stakeholders Asked :** "Fix the issue ASAP and update me"
**Issue/bug :** "Customer can book past closing time"

**Messy PM answer** 
Just work on the issue and let me know once completed.
	Shows: 
		- No module identified
		- No expected behavior
		- No priority 
		- No verification method
		- Dev's will be guessing
	Results:
		- Re-work
		- Follow ups
		- Delays
	
**Clear PM answer**

**Bug/Issue Title**
Customers are able to book appointments after business closing hours.

**Business Impact**
Appointments booked after the business hours can not be accomplished, it will lead to customer dissatisfaction and support escalations.

**Affected Module**
Customer Booking Portal

**Expected Behavior**
Users should not be able to create a booking after 8:00 PM.

**Acceptance Criteria**
1. Booking before 8:00 PM → allowed
2. Booking exactly at 8:00 PM → allowed
3. Booking after 8:00 PM → blocked with message:
    “Bookings are closed for today. Please select another date.”

**Validation**
- Testing to be done using different user accounts
- Confirm booking is not stored in database after 8 PM

**Priority & Communication**
- Priority: High (customer-facing issue)
- Please update the ticket with investigation findings and ETA.
- Inform if additional time is required.

## Decision Making Example
Based on the problem below make decisions what needs to be done step wise.
**Problem:**  
Your appointment-booking application is ready for launch in **3 weeks**.

But QA discovered two major things:
- The **WhatsApp reminder notification feature** (auto reminder before appointment) is incomplete and still buggy.
    
- The **Online payment integration** is working but only for card payments — UPI is not yet added.

**Engineering team says:**

- Completing WhatsApp reminder → needs **10 more days**
    
- Adding UPI payments → needs **12–14 days**
    
- Doing both together → **very high risk of unstable release**
### Exercise 2 (Decision Making)

**Step 1 :** Defining a problem
**Problem:** 
We must decide which feature to launch in the upcoming release because engineers capacity and timeline do not allow both to be delivered safely .

**Step 2:** Listing 2-3 options
Option:
 1. Do Both now.
	 - Pros: Client Happy short term.
	 - Cons: Stress among devs, high chances of bugs.
2. Do WhatsApp reminder feature now.
	- Pros: Some value delivered, less risky, High chances of good delivery.
	- Cons: Client slightly disappointed
3. Do UPI payment option now
	- Pros: Some value delivered, less risky, High chances of good delivery.
	- Cons: Client slightly disappointed

**My Selection choice**

Option 2, Do WhatsApp reminder feature now
Reason: Launch with WhatsApp reminders first and postpone UPI to the next release.  
The reminder feature directly supports the core business goal —> ensuring customers attend booked appointments and reducing no-shows, which impacts client revenue and satisfaction.  
Users can still complete payments using existing card options, so the booking flow is not blocked.  
Delivering both features together risks launch instability, while delivering reminders first improves launch success and customer retention.