---
title: New regulations part 4 – Receiving references
date: 2023-03-15
screenshots:
items:

- text: "Application overview (Waiting)"
- src: application-overview-waiting.png
- text: "Application overview (Received)"
- src: application-overview-received.png
- text: "Reference list (Received)"
- src: reference-list-received.png
- text: "Assess reference"
- src: assess-reference.png
- text: "Reference list (Accepted)"
- src: reference-list-accepted.png
- text: "Reference list (Rejected)"
- src: reference-list-rejected.png
- text: "Reference list (All accepted)"
- src: reference-list-accepted-all.png
- text: "Application overview (Completed)"
- src: application-overview-completed.png
- text: "Award flow (step 1)"
- src: award-flow-p1.png
- text: "Award flow (step 2)"
- src: award-flow-p2.png
- text: "Award flow (step 3)"
- src: award-flow-p3.png
- text: "Award flow (step 4)"
- src: award-flow-p4.png
- text: "Award flow (step 5)"
- src: award-flow-p5.png

---


### Background

In the previous design history update we looked at the process of requesting references before awarding qualified teacher Status (QTS).

The other end of this process begins when the references start to come back. The assessors need to know new references have been received, but the system should also discern the point at which the assessor needs to review them.

We need to automate the process so assessors are only invited to review the new information once it’s potentially enough to make a decision to either award or decline QTS.


### Understanding the rules

The process for requesting references is the same no matter which country or state the applicant is recognised in, but the rules differ on how we treat what we receive.

For ‘Tier 1’ countries (broadly comprising those countries and states that offer online ratification) we do not necessarily need the reference from the applicant’s current or most recent role. If other references provide the minimum number of months, the assessor can use those to make their decision on whether to award or decline QTS.

For countries that sit outside Tier 1, the current or most recent role is mandatory, so even with references covering sufficient duration, the assessor cannot take a decision without that key reference.


### Building the logic

As soon as the assessor submits the request for references, the status of the ‘Verify reference requests’ on the task list and the overall status of the application will switch to ‘Waiting on’.

![Application overview (Waiting](application-overview-waiting.png)

When a reference comes back, the system will check whether or not the country that recognises the applicant is in Tier 1. If not, the assessor will not be asked to review the reference and the status will not change.

If the country is in Tier 1, we can move to the second question – whether the reference provides evidence of the 9-month minimum teaching time (either on its own or combined with the other references received so far).

If the duration is not yet sufficient, again the assessor will not be asked to review the references received so far and the status remains set to ‘Waiting on’.

If the system establishes that the references received are potentially enough to make a decision, the status switches to ‘Received’ and the assessor can view the references overview page.

![Application overview (Received)](application-overview-received.png)


### The references overview page

The references overview page shows the assessor all the references that have been requested and their current status (either waiting on, received, accepted, rejected or overdue).

From here, they can view the individual references that have been returned, where they’ll see a playback of the answers given by the person providing that reference.

![Reference list (Received)](reference-list-received.png)
<br>
![Assess reference](assess-reference.png)

Based on their assessment of that reference, they can mark it as ‘Accepted’ or ‘Rejected’, and their decision will show in the status on the overall references page. They can then decide whether they’re able to award or decline QTS at this point, or whether they need to wait for more references to arrive.

![Reference list (Accepted)](reference-list-accepted.png)

If it’s the latter, the status of the application will revert to ‘Waiting on’ until they’re invited to review more references, or the end date for references is reached and the outstanding ones become overdue.

As more references come in, the assessor reviews each one, either accepting it or rejecting it. A rejected reference may or may not warrant a decline – an applicant could potentially still be awarded QTS with a rejected reference if their other references provide enough experience.

It’s for the assessor to review that reference and take a decision on whether or not the reasons for rejection have wider implications for the whole application.

![Reference list (Rejected)](reference-list-rejected.png)

When the assessor is ready to move to a final decision (as in the screenshot below, where all 3 references have been accepted), selecting ‘Yes, I can progress this application to award or decline’ will take them back to the task list, where ‘Verify reference requests’ is now marked ‘Completed’ and ‘Assessment recommendation’ is active.

![Reference list (All accepted)](reference-list-accepted-all.png)
<br>
![Application overview (Completed)](application-overview-completed.png)

From here, the assessor will follow either the award or decline route. In the case of awarding, they’ll see a screen that plays back any important considerations (whether that applicant has any rejected references or needs to do a statutory induction period). They’re also asked to tick a declaration that they’re certain they want to award QTS.

![Award flow (step 1)](award-flow-p1.png)
<br>
![Award flow (step 2)](award-flow-p2.png)

They’ll then have one more opportunity to check and amend the age range and subjects that the applicant is qualified to teach in England. We know from testing with assessors that while it’s important to capture this information during the initial assessment, they also need to be able to make any change at this point, in light of verifying qualifications, letters of professional standing and references.

We play back the assessor’s own initial assessment recommendations on this age range and subjects page in a ‘Check your answers’ format, so they can make any last changes before awarding QTS.

![Award flow (step 3)](award-flow-p3.png)

We then ask the assessor one final time whether they’re happy to award QTS, before moving the application into ‘Award pending’.

![Award flow (step 4)](award-flow-p4.png)
<br>
![Award flow (step 5)](award-flow-p5.png)
