
### Burndown Charts and Velocity Report
Velocity says what ever the points we have allocated to the team in last sprint was correct or over allocated and can give the average measure of delivery points that can be allocated to the team.
we can see every sprint points and can measure the average of all the points, which says how much points we can allot to the upcoming sprint, we have some figures around which we can allot to the team.

Sprint 1-   18 points completed

Sprint 2-   22 points completed

Sprint 3-  20 points completed

so the average will be Average = 20 points
That means:  
Your team can safely take -20 story points every sprint.

#### Velocity measures the team’s average delivery capacity across sprints, while the burndown chart tracks remaining work within a single sprint to show whether the team is on schedule.

Project - Music academy Website
#### Epic description for jira
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

## Creating two User Stories.

1. Work on UI design Finalization -> user story - points
	Description
	 Front end team with work on design part for music academy block 
	- Front end UI screen designing -> task
			Description
			- Connect with the Design team and work on UI Creation
			- Finalize the no of screens 
2.  Work on Documenting the legacy code base- both for Front end and backend.-> user story
 - Backend to Document the Legacy codebase-> task

Description
		Notes preparation, listing important web service calls, Database calls if included etc, identifying request and response from the legacy code
- Frontend to analyse and document the legacy codebase. -> task

  Description
		 Frontend team document the legacy codebase. 

Note: if burn down is not progrssing incrementally downward(staircase), it will be difficult to track the correct progress.
