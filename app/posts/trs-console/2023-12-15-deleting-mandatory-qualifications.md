---
title: Deleting mandatory qualifications
date: 2023-12-15
description: Letting users remove a mandatory qualifications from a person's teaching record.
screenshots:
  items:
    - text: A qualification summary card with a delete action
      src: summary-card-delet.png
    
    - text: Question page asking for detail about why the MQ is being deleted
      src: delete-question-page.png
    
    - text: If the user selects yes to upload evidenve a file upload is revelaed
      src: delete-upload-evidece.png
    
    - text: The user is asked to confirm the data that is being deleted and the reasons why
      src: delete-confirm.png
    
    - text: A success screen for deleting the MQ
      src: delete-confirm.png

    - text: Different states for errors with the file upload if the file is an incorrect format or type, or the user has not selected a file
      src: delete-evidence-states.png
---

## As is 

In the old system, users sometimes needed to remove data about mandatory qualifications (MQ) that was inaccurate, added by mistake, or the training provider had asked them to remove. They did this by marking them inactive, instead of active. This didn’t remove the data, but effectively hid it from displaying on front end services. This meant that data was being kept for a long time even if it was known to be inaccurate. 

Users would also add a note describing why they had made the change, which was stored in an unstructed tab of all notes assoicated with a record.

## To be

We decided to add a delete action to the qualification summary card. This more accurately describes a destructive action than marking it as inactive.

The user is then asked to select a general reason for deleting the MQ. This is to make sure the action is valid and to help with monitoring and auditing. These have been defined by the service to cover the most common scenarios of:
- added in error
- provider request
- unable to confirm the data is correct

There is also an option for ‘another reason’. 

The user then adds more detail about the reason for deleting. This allows flexibility for different situations and may provide context, such as describing an email from a training provider asking them to remove something.

The user can then upload evidence to support the change being made, such as a screenshot of an email. The file upload is contained in radio buttons so it can post to the form and if users navigate back to this screen and remove it, the other inputs will remain.

## Change history

Once the deletion is confirmed, the action and context given will be recorded in a change history. This is for quality control and auditing. It is a long term database and this can help to answer enquiries a long time after the change was made. 

The reasons collected when making the change will be associated to the event and user. This will provide more structure than the old notes feature and make it easier to see changes over time.

## Next

We need to design the change history, because we’re using this to structure the information collected when making changes.