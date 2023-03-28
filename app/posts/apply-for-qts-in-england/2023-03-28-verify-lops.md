---
title: Verifying letters of professional standing
date: 2023-03-28
screenshots:
items:

- text: "LOPS response recorded"
- src: response-recorded.png
- text: "LOPS response reviewed"
- src: response-reviewed.png
- text: "Task reviewed"
- src: task-reviewed.png
- text: "Task waiting on response"
- src: task-waiting-on-response.png
- text: "Verification steps"
- src: verifications-steps.png
- text: "Question whether to verify LOPS"
- src: verify-lops-question.png
---


A brand new piece of functionality that we’ve introduced to Apply for qualified teacher status (QTS) in England is the ability for assessors to verify that letters of professional standing are legitimate.


### Why it matters

Providing some form of proof of professional standing has always been a requirement – either by uploading a letter of professional standing, or by quoting a reference number, depending on the country or territory.

What’s different now is that with the anticipated numbers of applications under the new regulations (and the move to make the service available to more countries), we need a way to ‘spot check’ the documents that are provided as evidence with the competent authorities who produced them.

### User needs being met

* As an assessor I need to request further information from a competent authority as needed so that I can progress the application.

* As an assessor I need to know further information has been received so that I can continue the assessment of the application.


### Contacting competent authorities directly

The current process for contacting a competent authority is to do so by email, and for minimum viable product (MVP) this process will continue. What we’re building is a way to ‘book-end’ that process within the system. Crucially, we’re adding a way to record that the assessor has chosen to verify the document, and to note when a response has been received, then record the decision on whether that response verifies the document.

As the ratio of applications that will be verified in this way is still under discussion, we need a system that makes it easy for the assessor to choose to verify the letter of professional standing, or to skip that step if they need to.

Once the initial assessment is carried out and the recommendation is to award QTS, the assessor will see the following screen. It gives them the option to verify the letter of professional standing and sets out what it will mean if they do so.

![Question whether to verify LOPS](verify-lops-question.png)

The next screen provides a brief summary of the actions they need to take offline, and what they can expect to see on the task list while they’re carrying those out.

![Verification steps](verifications-steps.png)

### A two-step process

Once the assessor has chosen to verify the letter of professional standing, the task list will show 2 new links in the ‘Verification requests’ section –’Record LOPS response’ and ‘Review LOPs response’. Only when the first of these is marked as ‘Completed’ does the second become active.

![Task waiting on response](task-waiting-on-response.png)

This is because we understand that the verification process may be carried out by more than one person (either the helpdesk or the assessors themselves) so it's important to make sure that there’s a record of where to find the response and any important notes.

In the first link, ‘Record LOPS response’ the reviewer can record that a response has been received then add notes to an assessor reviewing the document on where to find it. Alternatively, should the system automatically set the status to ‘Overdue’ (which it will do so after 30 days of no response), the reviewer can select ‘No’ and then either push ahead for review, or choose to leave the request in ‘Overdue’ for longer.

![LOPS response recorded](response-recorded.png)

Once the second link ‘Review LOPS response’ is active, the assessor will see a playback of any notes that were added in the previous step, and be asked whether or not the response from the competent authority verifies that the letter of professional standing is legitimate. If not, again, they’ll need to leave an internal note to explain why.

![LOPS response reviewed](response-reviewed.png)

Once the assessor has made a decision on the ‘Record LOPs response’ screen, when they go back to the task list they’ll see that both LOPs links are now marked as ‘Completed’.

![Task reviewed](task-reviewed.png)

### Exceptions

It’s not always possible to verify the letter of professional standing. First, depending on which ‘bucket’ the country or territory is in, they may well offer online verification of professional standing, in which case we never ask for a document to that effect.

Secondly, in ‘LOPsless’ applications (where the competent authority will only send the letter directly to the TRA), there’s no need for verification, since we’d be approaching the same organisation for verification that sent the letter in the first place.

However, unlike verifying references, this process was never meant to take a blanket approach, verifying letters of professional standing for all applications. How many applications are ultimately sent through this process is something that the TRA will settle on as the feature comes into use.
