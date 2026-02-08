
# Transforming Legacy Systems, Our Step-by-Step Migration from Yii2 to a Modern Web Stack - A Music Academy Management Platform

Write down your observations:
1.What is the scope of this project? (What are they building?)
2.What timeline are they working with?
3.Identify 2 potential risks you see in this project
## Objective
Migrate the first legacy PHP module to a modern architecture using Next.js (frontend) and NestJS (backend) while keeping the existing production system operational.

The migration will follow the Strangler Fig Pattern, meaning the new module will run alongside the legacy system and gradually replace its functionality without downtime.

---

## Scope
• Analyze legacy PHP (Yii2 + jQuery + Bootstrap) implementation
• Identify business logic, database calls, and web service dependencies
• Design API contract between frontend and backend
• Develop backend APIs in NestJS
• Build new UI screens in Next.js
• Integrate the module with the legacy system - modern module will be linked to the old one
• Perform regression testing and production rollout

---

## Business Value
• Reduce technical debt
• Improve maintainability and scalability
• Enable faster future feature development
• Reduce operational risk compared to full system rewrite
• Improve performance and user experience

---

## Acceptance Criteria
1. Users can access the module through the live website.
2. Existing user credentials work without new registration.
3. Legacy system functionality remains unaffected.
4. Data matches between legacy and new system.
5. Authentication works across both systems.
6. No critical defects after QA testing.
7. Module can be rolled back safely if required.

---

## Risks
• Hidden legacy business rules
• Session handling mismatch
• Database dependency conflicts
• API contract mismatch

---

## Definition of Done
• Module deployed to production
• QA regression completed
• Monitoring stable for 7 days
• Stakeholder approval received


**Time Management**
Week 1-2: Design screens Finalizing (10 days)
 FE Team: Finalize the UI design from the design team (Figma)- where we can decide which text, symbol, design symbols to be used.

Week 3-5 (15 days)
 BE Team: Backend (2 person) (11 days) (2 days more if any defect raised) -13 days total
		API creation at backend side, 
			1. legacy code observations for first module - 2 days- Notes preparation, listing important web service calls, Database calls if included etc, identifying request and response from the legacy code -> this will helps in building a formal structure in developers mind the things needs consideration.
			2. API Design Specification - 1 day 
			   (spending a day on API design before actual implementation)
				- deciding endpoints
				- defining payload structure - request and response format
				- defining behavior
				- error codes
				- exposing API end points for integration from backend side.
				- API Contract - a mutual agreement between the frontend and 
				  backend team
			3. Now we can start implementing the actual API after the mutual 
			   agreement with the front end - 5 days and deployment
			   Unit tests cases - 2 days, code coverage criteria (90+ 
			   percent),ensuring no new vulnerabilities added
			   Testing - through logs or response/request tools- 1 day 
	
Week 6-8
FE Team : Front end (1 person) (10-12 days) (2 days if any defect are raised) (14 days total)
		 API creation and integration of API (decided with backend)
			1. Finalize the UI design from the design team (Figma) - to be done when backend team deciding design specification
			2. API Design Specification - 1 day
			   (spending a day on API design before actual implementation)
			   - Integrate the exposed API  from the backend side in order to fetch the data,  so that team now can start building the UI and each team can now work independently without dependency of each other. - 1 day
			   - Start Building the UI which is finalized - 5 days (1 screen - one module )
			   - write test cases , coverage 90+ percentage, ensuring no new vulnerabilities added - 3days
Week 9-10
QA Team (2 person) (10 days total)
		Testing - 10 days
			Things to consider
				- No breakage 
				- Checking data with different users credentials(child, parents, admin), should match with the actual(old legacy code data).
				- Raise Defects for any mismatch of data


**What timeline are they working with**
3-6 month

**Identify 2 potential risks you see in this project**
1. If new engineers- legacy code understanding will require time like how api responses are checked, how deployment is done, being a monolithic app complex code base.
2. Code complexity in terms of Database integration, client approvals, tools licensing since modernization required.


https://www.loom.com/share/ea758343e9f74b8eb0bef9157c94d190