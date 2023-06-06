---
title: Stopping users from opening files with suspected viruses
date: 2023-06-06
screenshots:
  items:
    - text: File being checked
      src: file-being-checked.png
    - text: File removed
      src: file-removed.png
---

Referrers can upload files that contain viruses.

To prevent caseworkers from opening files with viruses we’ve added functionality to [check each file before it’s included in the referral](/refer-serious-misconduct-by-a-teacher-in-england/checking-if-uploaded-files-have-viruses).

## How it works

If the zip file contains a file that’s currently being checked, the file will be:
- empty
- renamed to [name-of-file]-file-being-checked-for-viruses.[extension].txt

If the zip file contains a file that’s been removed, the file will be:
- empty
- renamed to [name-of-file]-file-removed-due-to-suspected-virus.[extension].txt

If the user clicks on the file while this is happening, they’ll be taken to a page that says the file is being scanned.

If the user clicks on a file that’s been removed, they’ll be taken to a page that says the file has been removed.

## Further considerations

If we find that a significant number of referrals include removed files, we’ll consider ways to prevent referrers from sending their referral with removed files.
