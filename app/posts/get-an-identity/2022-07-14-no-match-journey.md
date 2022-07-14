---
  title: No match journey (TRN required)
  date: 2022-07-14
  screenshots:
    items:
      - text: "Allow users to continue without knowing TRN"
        src: 01-allow-users-to-continue-without-knowing-trn.png
      - text: "Prompt the user if there is no match"
        src: 02-prompt-if-no-match.png
      - text: "Allow continuing without a match"
        src: 03-allow-continue-anyway.png
---

We’ve iterated the [TRN required journey](/get-an-identity/npq-with-a-trn/) to include designs for when the answers given do not match a DQT record.

In the TRN required scenario, every user should be in DQT. We know for certain that they have not matched because of the information they’ve given, rather than, as it would be in the wider case, because it’s possible they don’t have a TRN and are not in DQT at all.

## Allow users to continue without their teacher reference number (TRN)

If when we ask someone for their TRN they don’t know it, we don’t want to block their onward journey. We know it can be difficult for users to find their TRN, there's a whole service for that – Find a lost TRN.

At this point we’ve already asked them all the questions we would on Find a lost TRN – and if their answers had matched, we would not have reached this TRN page. Email, name, date of birth and National Insurance number – if 3 of those match then we stop asking questions. So, if we sent them to Find a lost TRN, they'd answer the same questions again, not find their TRN, and get directed to support.

We can shortcut that repetitive journey by raising a support ticket from Get an identity. The request will be slightly different, instead of giving the user their TRN we would be linking their newly created Get an identity account with their DQT data. We might email them their TRN too.

## Continuing without a match

If the user reaches the end of the Get an identity journey without matching in DQT, we follow the same pattern as Find a lost TRN – we present their answers back to them and ask if they are correct or if anything needs changing.

If everything looks good and they do not want to change their answers, we let them continue.

We expect:

- a support agent to connect the dots behind the scenes if they can
- contact the user if they need more information
- to pass this user back to the wrapping service, but will indicate that we could not match them with DQT yet, but also that we know they should be in there
