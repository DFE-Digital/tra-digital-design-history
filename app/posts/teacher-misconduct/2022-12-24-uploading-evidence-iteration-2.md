---
title: Uploading evidence iteration 2
date: 2022-12-24
screenshots:
  items:
    - text: Asking if they have any evidence to upload (member of public)
      src: have-evidence.png
    - text: Asking if they have any evidence to upload (employer)
      src: have-evidence--employer.png
    - text: Upload evidence (member of public)
      src: upload.png
    - text: Upload evidence (employer)
      src: upload--employer.png
    - text: Uploaded evidence
      src: uploaded-evidence.png
    - text: Deleting a file
      src: delete.png
    - text: File deleted (there are other files left)
      src: file-deleted.png
    - text: File deleted (it was the last file to be deleted)
      src: file-deleted--start.png
    - text: Check answers
      src: check-answers.png
---

The current approach to [uploading evidence](/teacher-misconduct/changes-to-the-form) is problematic.

Firstly, it’s not easy to upload multiple files. The `type=file` input only allows files to be uploaded from the same directory.

So if users want to upload multiple files from different directories they’d have to go through the flow again which is unclear and long winded.

Secondly, it’s hard to categorise a file because users have to use the name to work out the what it contains. This may not be obvious because files are often named badly.

Thirdly, the idea to categorise files is to give a description to caseworkers so that they can find the file they’re looking for during their investigation.

But caseworkers will initially continue to upload evidence into the Teacher Misconduct System (TMS). So the descriptions would not be copied over unless they form part of the file name.

As a result, we’ve:

- changed the flow to make it easy to upload multiple files
- removed the ability to categorise a file

## How it works

The user is first asked whether they have evidence to upload. If they select ‘Yes’ they’ll be taken to the page to upload a file.

### Letting users upload additional files

After uploading a file, the user is shown a list of uploaded files where they can view or delete a file.

Underneath the list there’s question which asks the user if they want to upload another file. If they select ‘No’ they’ll be taken to the check answers page.

### Deleting a file

What happens when a user deletes a file depends on whether they’ve uploaded 1 file or multiple.

If there's multiple files in the list, a success message is shown at the top of the page.

If there's only 1 file, the user is taken to the page asking if they have evidence to upload with a success message at the top of the page.

## Further considerations

We want to consider how to make it easier for caseworkers to:

- understand what an uploaded file contains
- upload multiple files at a time

