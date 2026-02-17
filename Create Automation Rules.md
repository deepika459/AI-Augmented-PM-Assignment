**triggers** - kick off the rule
**conditions** - that refine the rule
**actions** - perform tasks in your site

**Automation Tasks Applied and Tested**

- [ ]  Automatically assign the sub-task to the team manager/scrum master/team lead when create.
- [ ] Send notification email when comment section is updated.
- [ ] Close parent item when child item is closed.

# Automation Rules Created

1. [Automate Assignee](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6b36-6c4a-7a9b-8d8d-356aead87679) (New Rule Created From scratch)
2. [Comment Updates](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6b02-fce1-784f-a177-49466762852d) (New Rule Created From scratch)
3. [Transition-Done-Rule](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6bbe-397e-731c-9bd9-7453e880aaec)(New Rule Created From scratch)
4. [Transition In-Progress Rule](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6ba0-11e7-7c5e-a190-5c16fae92a04) (New Rule Created From scratch)
5. [When all child work items are completed → then close parent](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6ae9-699e-7551-9be8-64fef22bef18) (PRE Defined Rule)

 
![[Pasted image 20260217185151.png]]
**High Level Over-view**
Rule 1:  [Transition In-Progress Rule](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6ba0-11e7-7c5e-a190-5c16fae92a04)

![[Pasted image 20260217181336.png]]

2. Rule 2:  [Comment Updates](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6b02-fce1-784f-a177-49466762852d) 
	When comments updated, email received as part of comment update automation.

![[Pasted image 20260217183017.png]]
**Path to create a Automation Rule for transition(child->done, move Parent->done)**
Rule 3: [Transition-Done-Rule](https://kdeepika459.atlassian.net/jira/software/projects/PDA/settings/automation#/rule/019c6bbe-397e-731c-9bd9-7453e880aaec)
1. Select work item
2. Work item transitioned
3. From status= in-progress -> done
4. Click- add component -> add a branch
5. Related work item select-> parent->next
6. Add an ACTION
7. Transition the work item to -> done
```
		Trigger: Work item transitioned → To Done
		Condition: Issue type = Subtask
		Branch: Parent
	    Condition: All subtasks status = Done
	      Action: Transition parent → Done
```

![[Pasted image 20260217205351.png]]


## Jira Story Enhancement
**AI Enhancement** -  Applied on description to enhance the description to more informative for the users and acceptance criteria added.