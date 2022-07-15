---
  title: Support screens for changing names
  date: 2022-07-15
  screenshots:
    items:
      - text: "A user with a verified name"
        src: 01-user-with-verified-name.png
      - text: "A user with an unverified name that does not match"
        src: 02-user-with-unverified-name-no-match.png
      - text: "Changing an official name"
        src: 03-changing-an official-name.png
  related:
    sections:
      - title: Related content
        items:
          - text: Prototype PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/122
          - text: Prototype iteration PR
            href: https://github.com/DFE-Digital/find-a-lost-trn-prototype/pull/124
---

Users will be able to create identities that:

- have an unverified official name
- have a name that does not match DQT

[Read about asking for names and changing names](/get-an-identity/names-in-get-an-identity/)

## TRN required

While the service requires TRNs, all users will be in DQT. During this time all users can request their official name changes through the current TRA process, which updates DQT.

DQT can cascade changes to Get an identity.

## TRN not required

Later we will allow users who are not in DQT (ie people without TRNs) to create identities. For these users there needs to be a way of changing their official name in Get an identity.

For a new name to be verified, there will need to be a process where a support agent confirms that name by seeing a copy of an official document. This verification process will be based on the existing TRA practice.

A support agent will need somewhere to make these changes. These designs show what those support screens might look like.
