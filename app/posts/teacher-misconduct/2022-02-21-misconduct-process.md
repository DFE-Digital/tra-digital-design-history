---
  title: "Teacher misconduct process"
  date: 2022-02-21
---

The Teacher Misconduct Unit (TMU) use the Teacher Misconduct System (TMS) to manage their misconduct cases. Each case goes through up to 3 life cycle stages:
1. initial assessment
2. investigation
3. hearing

Each of these three stages involves a multi-step process which takes a number of days, weeks or months. TMS has a detailed state model to record the progress of each case.

[![State model for a TMS case](TMS-case-states.png "State model for a TMS case")](TMS-case-states.png)

Cases move between states when case workers in the TMU create, populate or complete "activity" records in the TMS.

Each case displays a list of activities associated with it, along with their status - either "active" or "closed".

In most cases, it is the act of completing an activity on a case that creates the next activity and changes the case state, but in some cases, state changes are triggered by a user taking a different action on the system, such as allocating a case to a case worker or recording costs.

[![Activities associated with a case in TMS](TMS-activities.png "Activities associated with a case in TMS")](TMS-activities.png)

Throughout this post, the names of case activities are referred to *in italics* for extra clarity.

## Stage 0: Referral and creating a case

The TMU receives referrals by email or post. Referrals typically use one of [these forms](https://www.gov.uk/government/publications/teacher-misconduct-referral-form). Referrals can come from:
- Employers (who are legally required to make a referral under certain circumstances)
- Members of the public
- The police
- The Disclosure and Barring Service (DBS)
- Other regulators and interested organisations

The admin support team is responsible for monitoring the TMU inbox and uploading the referrals received onto the TMS, which must be done within one working day of receiving the referral.

The admin support team adds the referral to the TMS by creating a new case, which typically involves:
- searching contacts (to see if the teacher or school already exists on the system)
- creating a new teacher contact record
- creating a new school organisation record
- creating a new case
- adding contacts to a case
- attaching documents to a case (e.g. the referral form)

[![A screenshot of creating a case in TMS](create-case.png "Creating a case in TMS")](create-case.png)

When the case has been created:
- the business process stage is initial assessment
- the case state is [awaiting initial assessment](#awaiting-initial-assessment)
- an *initial assessment decision* activity is created

After creating a case, users can perform the following actions at any stage in the case life cycle, other than when the case is closed:

- view case documents
- enter allegations and select the behaviour type (e.g. harassment, indecent images)
- generate letters
- send an email from TMS (although the TMU do not use this functionality)
- create a task and assign it to a user

## Stage 1: initial assessment

The TMU must perform an initial assessment of a case within 3 working days of receiving the referral.

### Awaiting initial assessment

TMU case managers organise regular meetings to assess new referrals. They decide whether they have jurisdiction, and whether the allegations, if true, would meet the threshold of serious misconduct. The meeting is organised off-system.

After the meeting, an Initial Assessment Record of Decision (ROD) document is produced, sent to the teacher and uploaded to the TMS as a case document.

A case worker also records the outcome of the meeting by populating the *initial assessment decision* activity, recording:
- decision, either "continue with investigation", "require further information" or "close case" (the user can select a closure reason)
- decision date
- decision details (free text)
- meeting participants (TMS users)

[![A screenshot of the TMS initial assessment decision](initial-assessment-decision.png "Recording the initial assessment decision")](initial-assessment-decision.png)

When the *initial assessment decision* activity is marked complete:
- if decision = continue with investigation
  - the case status changes to [awaiting allocation](#awaiting_allocation)
- if decision = require further information
  - the case status changes to [awaiting further information](#awaiting-further-information)
  - a *further information* activity is created
- if decision = close case
  - the case status changes to [awaiting archiving](#awaiting-archiving)
  - a *case closure* activity is created

### Awaiting further information

When the further information that is needed is received, the case worker populates the *further information* activity.

[![A screenshot of the TMS further information activity](further-information.png "Recording the further information")](further-information.png)

When the *further information* activity is marked complete:
- if decision = continue with investigation
  - the case status changes to [awaiting allocation](#awaiting_allocation)
- if decision = close case
  - the case status changes to [awaiting archiving](#awaiting-archiving)
  - a *case closure* activity is created

### Awaiting allocation

Before the case proceeds to investigation, an SEO team leader allocates the case to a case worker and a case manager. They use a TMS dashboard which shows how many cases are assigned to each case worker and case manager.

Case workers and case managers currently have around 100 open cases each.

[![A screenshot of assigning a case to a case worker](further-information.png "Assigning a case to a case worker")](further-information.png)

When the case worker field is populated and the case is saved:
- the business process stage changes to [investigation](#investigation)
- the case status changes to [pending review meeting outcome](#pending_review_meeting_outcome)
- An *investigation* activity and a *review meeting* activity are created.

## Investigation

The TMU aim to complete the investigation stage within 20 weeks from the receipt of the referral. The investigation phase starts with a review meeting to decide whether an external investigation is needed, or whether the investigation phase can be conducted by the TMU.

Investigations end with a determination meeting to decide whether there is a case to answer, which means it should proceed to a hearing.

[![A screenshot of an investigation activity](investigation-activity.png "Investigation activity")](investigation-activity.png)

### Pending review meeting outcome

A meeting is held to determine whether the case will be investigated internally or by an external firm. Most cases are investigated externally, but if the case relates to a criminal conviction, rather than engaging a law firm, a member of the admin support team can gather the necessary documents from the police and compile the investigation bundle.

After the meeting, a case worker records the outcome of the meeting on the review meeting activity:
- investigation type, either internal or external
- meeting date
- details (free text)
- meeting participants (TMS users)

[![A screenshot of a review meeting activity](review-meeting.png "Recording a review meeting")](review-meeting.png)

When the review meeting activity is marked as complete:
- if investigation type = internal
  - the case status changes to [preparing investigation plan](#preparing_investigation_plan)
  - an *investigation plan completion - internal activity* is created
- if investigation type = external
  - the case status changes to [awaiting investigation instruction outcome](#awaiting_investigation_instruction_outcome)
  - an *instruct investigating officer firm* activity is created

### External investigations

#### Awaiting investigation instruction outcome

For external investigations, the case officer instructs a firm off-system by completing a Notice of Instruction form and attaching the details of the case, and sending it to the firm of solicitors securely using Egress or Deal Room.

Then the case worker fills out the name of the firm and instruction date on the *instruct investigating officer firm* activity and saves it.

[![A screenshot of an instruct investigating officer firm activity](instruct-investigating-officer-firm.png "Instruct investigating officer firm activity")](instruct-investigating-officer-firm.png)

When the firm responds, the case worker populates the instruction outcome and outcome date:
- if instruction outcome is Rejected and the activity is marked complete:
  - the case status is unchanged
  - another *instruct investigating officer firm* activity is created
- if instruction outcome is Accepted and the activity is saved (not completed):
  - the case status changes to [awaiting investigation plan](#awaiting-investigation-plan)

#### Awaiting investigation plan

When the caseworker receives the investigation plan, they set the plan received date on the *instruct investigating officer firm* activity and save it.
- the case status changes to [awaiting investigation plan approval](#awaiting-investigation-plan-approval)

#### Awaiting investigation plan approval

When the plan is approved, the case worker can set the approval date on the *instruct investigating officer firm* activity and mark it as complete. Then the case officer updates the case costs.

[![A screenshot of case costs](case-costs.png "Case costs")](case-costs.png)

When the case costs are populated and the case is saved:
- the case state changes to [awaiting investigation bundle](#awaiting-investigation-bundle)
- an *external investigation* activity is created

#### Awaiting investigation bundle

When the investigation bundle is received, the case worker uploads it to the CRM, updates the allegations on the consideration form. and adds the investigation bundle received date to the *external investigation* activity .

When the external investigation activity is marked as complete:
- the case state changes to [awaiting determination meeting outcome](#awaiting-determination-meeting-outcome)
- a *determination meeting* activity is created

### Internal investigations

#### Preparing investigation plan

For internal investigations, the case worker creates an investigation plan off-system. When the plan is ready, the case worker can set the plan completion date on the *investigation plan completion* activity.

[![A screenshot of an investigation plan completion activity](investigation-plan-completion.png "Recording completion of the investigation plan")](investigation-plan-completion.png)

When the *investigation plan completion* activity is marked as complete:
- the case state changes to [internal investigation](#internal-investigation)
- an *internal investigation* activity is created

#### Internal investigation

Next, the case worker fills out the consideration form (off-system), updates the allegations (on-system) and can then populate the *internal investigation* activity.

[![A screenshot of an internal investigation activity](internal-investigation.png "Internal investigation activity")](internal-investigation.png)

When the case worker populates whether teacher submission is required and the date the teacher was informed and saves the case:
- if teacher submission required = yes
  - the system automatically calculates when teacher submission is due
  - the case status changes to [awaiting teacher submission](#awaiting-teacher-submission)
- if teacher submission required = no
  - the case remains in the same status

If submission is not required, then the case worker completes the rest of the *internal investigation* activity. When the *internal investigation* activity is marked as complete:
- if submission outcome = further investigation needed:
  - the case state remains in the same status
  - another *internal investigation* activity is created
- if submission outcome = refer to determination meeting:
  - the case state changes to [preparing investigation bundle](#preparing-investigation-bundle)
  - internal investigation bundle activity is created

#### Awaiting teacher submission

Once the teacher submission has been received or time elapsed, the case worker completes the rest of the *internal investigation* activity.

[![A screenshot of an internal investigation activity with teacher submission](teacher-submission-required.png "Internal investigation activity with teacher submission")](teacher-submission-required.png)

When the *internal investigation* activity is marked as complete:
- if submission outcome = further investigation needed:
  - the case state changes back to [internal investigation](#internal-investigation)
  - another *internal investigation* activity is created
- if submission outcome = refer to determination meeting:
  - the case state changes to [preparing investigation bundle](#preparing-investigation-bundle)
  - internal investigation bundle activity is created

#### Preparing investigation bundle

The case worker prepares the investigation bundle (off-system) and then completes the *internal investigation bundle* activity:
- consideration form completion date
- consideration form completed by
- investigation bundle completion date
- investigation bundle completed by

[![A screenshot of an internal investigation bundle activity](internal-investigation-bundle.png "Internal investigation bundle activity")](internal-investigation-bundle.png)

When the internal investigation bundle activity is marked as complete:
- the case status changes to [awaiting determination meeting outcome](#awaiting-determination-meeting-outcome)
- a *determination meeting* activity is created

### Awaiting determination meeting outcome

For both internal and external investigations, when the bundle is ready, a determination meeting is held. This should not involve any of the previous decision makers for the case.

After the meeting, a case worker can record the outcome on the *determination meeting* activity, including the decision, decision date, meeting date and participants.

[![A screenshot of a determination meeting activity](determination-meeting.png "Determination meeting activity")](determination-meeting.png)

When the determination meeting activity is marked as complete:
- if decision = “refer to professional conduct panel”
  - the business process stage changes to [hearing](#hearing)
  - the case status changes to [awaiting presentation instruction outcome](#awaiting-presentation-instruction-outcome)
 - an *instruct presenting officer firm* activity and a *hearing* activity are created
- if decision = “close case”
  - the case status changes to [awaiting archiving](#awaiting-archiving)
  - a *case closure* activity is created

## Stage 3: Hearing

After the determination meeting is complete, if there is enough evidence then the case will proceed to a hearing. The hearing should take place within 52 weeks of the referral.

[![A screenshot of a hearing activity](hearing.png "Hearing activity")](hearing.png)

The hearing activity stays open throughout most of the hearing stage, in parallel with other activities. As well as the usual activity states of active and closed, the *hearing* activity has a separate state field associated with it with the following options:
- in progress
- provisional
- listed

### Awaiting presenting instruction outcome

As soon as the determination meeting outcome is available, the user is able to do the following in the system:
- notify all parties of the outcome of the determination meeting (via letters)
- instruct presenting officer firm
- record instruction outcome details

[![A screenshot of an instruct presenting officer activity](instruct-presenting-officer.png "Instruct presenting officer activity")](instruct-presenting-officer.png)

If the instruction is rejected, the case worker records the outcome and marks as complete.
- Another *instruct presenting officer firm* activity is created.

If the instruction is accepted, the user can update the instruction details. When the changes are saved and marked as complete:
- the case status changes to [awaiting hearing plan](#awaiting-hearing-plan)
- a *hearing plan* activity is created

### Awaiting hearing plan
When the hearing plan is received, the case manager uploads it to the case documents, and populates some other case fields. They complete the *hearing plan* activity ‘received date’ and save the details.

[![A screenshot of a hearing plan activity](hearing-plan.png "Hearing plan activity")](hearing-plan.png)

When the details are saved:
- the case status changes to [awaiting hearing plan approval](#awaiting-hearing-plan-approval)

### Awaiting hearing plan approval

The plan is approved by the case manager (HEO). As part of the approval, the HEO completes the costs related to the hearing plan. Once the hearing plan has been approved, the user updates the ‘approved by’ and ‘approved date’. A combination of the case manager and scheduling team then book resources for the hearing.

The user is able to do the following:
- book resources
  - rooms
  - presenting staff
  - legal advisers
  - panellists
- view booked resources
- amend booked resources
- assign chair to the panel

[![A screenshot of booking a bookable resource](bookable-resource-booking.png "Booking a bookable resource")](bookable-resource-booking.png)

Once the hearing start date and end date are entered into the system, the *hearing* activity status is changed to ‘provisional’.

After booking the hearing room, the *hearing* activity status is updated to ‘provisionally listed’.

After the panellists are booked, the *hearing* activity status is updated to ‘listed’.

When the *hearing plan* activity is marked as complete:
- the case status changes to [awaiting draft notice of hearing](#awaiting-draft-notice-of-hearing)
- a *notice of hearing* activity is created

### Awaiting draft notice of hearing

The ‘draft notice of hearing expected date’ is 12 weeks after the determination meeting decision date. This is calculated by the system.

The user completes the ‘notice of hearing sent date’ and ‘notice of hearing response received date’

[![A screenshot of a hearing plan activity](hearing-plan-2.png "Hearing plan activity")](hearing-plan-2.png)

Once completed and saved, the next activity is determined by the response to ‘allegation admitted’ and ‘meeting requested’:
- if both fields are answered Yes:
  - the case status changes to [PCPM process](#pcpm-process)
  - a *PCPM* activity is created
- if either or both of the fields are answered No:
  - the case status changes to [awaiting hearing bundle](#awaiting-hearing-bundle)
  - a *hearing preparation* activity is created

### PCPM

If the teacher admits to the allegations, the case is heard as part of a Professional Conduct Panel Meeting (PCPM), rather than scheduling a full hearing (PCPH). The teacher does not attend a panel meeting.

For the *PCPM* activity, the user is able to do the following:
- complete PCPM form
- record PCPM decision

[![A screenshot of a PCPM activity](pcpm.png "PCPM activity")](pcpm.png)

The *PCPM* decision will either be ‘proceed as a hearing’ or ‘proceed as a meeting’
If proceed as a hearing:
- the case status changes back to [awaiting draft notice of hearing](#awaiting-draft-notice-of-hearing)
- another *notice of hearing* activity is created

If proceed as a meeting, the user must complete the PCPM approval received date and notice of meeting sent.
- the case status changes to [hearing preparation](#hearing-preparation)
- a *hearing preparation* activity is created

Once the hearing preparation is complete, the case activity goes from ‘hearing outcome’ to ‘case closure’, same as the non-PCPM route.

### Hearing preparation

PCPM only. What happens here?

### Awaiting hearing bundle

Before the hearing, the user can complete all preparation activities. This includes:
- set/update the hearing date
- amend hearing details
- add additional hearing days
- update hearing status
- add/update service costs
- create the group of case papers and distribute to all parties
- postpone hearing by changing the hearing status to ‘postpone’
- adjourn hearing by changing the hearing status to ‘adjourn’

[![A screenshot of a hearing preparation activity](hearing-preparation.png "Hearing preparation activity")](hearing-preparation.png)

Once the hearing bundle is received from the presenting officer firm and the case worker enters the details. Once all hearing preparation tasks are completed, reason for closure should be set to ‘completed’ and the *hearing preparation* activity marked as completed
- the case status changes to [awaiting hearing outcome](#awaiting-hearing-outcome)
- a *hearing outcome* activity is created

### Awaiting hearing outcome

Before the hearing takes place, if new information or evidence is uncovered, the case will be referred back to the investigation stage.

Once the hearing has taken place, the outcome of the hearing is recorded in the system. If a hearing concludes early, the user is able to amend the number of days that panellists sat on the hearing.

[![A screenshot of a hearing outcome activity](hearing-outcome.png "Hearing outcome activity")](hearing-outcome.png)

The user fills in all required fields. On saving:
- the case status changes to [awaiting decision distribution](#awaiting-decision-distribution)
- a *hearing outcome* activity is created

### Awaiting decision distribution

Once the announced decision has been distributed, the case can be closed.

On marking the *hearing outcome* activity as complete:
- the case status changes to [awaiting archiving](#awaiting-archiving)
- a *case closure* activity is created

### Awaiting archiving

In the case closure activity, the user completes all the mandatory fields and the case is updated to ‘case resolved’. After this point, the case can no longer be updated.

## Extensions to the misconduct process (TMS Tasks)

In TMS, there are two types of tasks. There are tasks that are created by case workers and case managers to manage their work and track activities that they need to complete. These are a type of activity in the TMS system.

The tasks covered in this section are TMS tasks. These refer to uneditable system tasks which are part of the misconduct process. Case workers and case managers add TMU tasks to their cases at appropriate stages.

### Set asides

Following a prohibition order, the teacher may be permitted to apply to have the order set aside after the minimum period specified in the order (not less than 2 years).

[![A screenshot of a set aside](set-aside.png "Set aside")](set-aside.png)

The TMS facilitates the set aside process:
- set asides can be created for resolved cases
- information can be recorded in the set aside
- a panel can be scheduled for a hearing
- set aside letters can be generated
- relevant set aside documentation can be stored on the case record

### Induction appeals

Newly Qualified Teachers who fail their statutory induction are not able to teach in maintained schools. Teachers can appeal their induction outcome to the TRA. This is conceptually entirely separate from the misconduct process, and is comparatively infrequent.

TMS allows the following:
- create a contact record and set it as an induction appeal
- Record information about induction appeals
- A panel can be scheduled
- Induction appeals letters can be generated
- Relevant induction documentation can be stored on the contact record

### High court appeals

Appeals can be made against prohibition orders, within 28 days from the date that the notice of the order was served on the teacher.

The TMS allows the following:
- create a high court appeal
- set appeal received date
- record appeal type, cost and grounds of appeal
- record appeal decision date
- record information about high court appeals
- relevant high court appeals documentation can be stored on the case record
- record court date and book resources
- record appeal outcome

### Abeyance

At any point, a misconduct case can be temporarily suspended. In the TMS, users are able to apply abeyance to a case.  While in abeyance, the SLA clock stops. Abeyance can be ended by entering an end date and marking as complete.

[![A screenshot of an abeyance activity](abeyance.png "An abeyance activity")](abeyance.png)

The TMS allows the user to enter Abeyance information in the Abeyance activity.
- record abeyance start date and end date
- record abeyance reason

### Interim Prohibition Order (IPO)

Once the seriousness of the allegation has been established, an IPO can be made at any stage in the misconduct proceedings and without a need for a hearing. The teacher has 10 working days to respond and provide relevant evidence to the TRA. If an IPO is made, the teacher, referrer and teacher’s current employer are notified. The teacher cannot carry out any teaching work until the IPO is lifted.

[![A screenshot of an IPO on a case](ipo.png "An IPO on a case")](IPO.png)

The TMS allows the following:
- add IPO
- update IPO status
- record teacher notification and notification date
- record IPO decision date and review date
- record IPO decision maker, reviewer
- record updated and/or removed dates if updated or removed from DQT
- remove IPO

### Create additional review meeting

Sometimes an investigation may need to be changed from internal to external or from external to internal. In TMS, this is done by creating an additional review meeting activity. In the additional review meeting activity, the user can set the investigation type as internal or external and save.

[![A screenshot of an additional review meeting activity](additional-review.png "An additional review meeting activity")](additional-review.png)

### Create referral back determination meeting

During investigation, there may be a need to refer back to a determination meeting. This may be to amend allegations due to newly discovered information or to close the case. The TMS system allows the user to create a ‘referral back determination meeting’ activity.

[![A screenshot of a referral back determination meeting activity](referral-back.png "A referral back determination meeting activity")](referral-back.png)

In the referral back to determination meeting activity, the user fills in the referral back decision as follows:
- ‘discontinued’ or ‘discontinued DBS barred’. On marking as complete, the case is automatically resolved.
- ‘continue with professional conduct panel’. On marking as complete, this results in the case activity and case status automatically returning to what they were before the ‘referral back determination meeting’ was created

### Create case management hearing

[![A screenshot of a case management hearing](case-management-hearing.png "A case management hearing")](case-management-hearing.png)
