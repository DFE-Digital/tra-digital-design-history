---
  title: Returning after completion, using the back button
  date: 2022-09-07
---

Consider the scenario:

- a user comes to Get an identity (and technically Find) and completes their checks (and we’ve created an identity)
- they reach the "Continue to service page", and/or continue past it back to the service
- then for some reason, they use the back button in their browser to return to earlier Get an identity questions

At this point:

- we’ve already checked our records
- created a central identity (match or no match)

Once they have left this part of the service, on trying to return to it there is nothing more to do.

## Design changes

If a user attempts to reach a page they should no longer access, we will show them a custom error page.

This is similar to the way this situation is handled on GOV.UK Sign-in, where a user is always redirected back to a "your account has been created" page.

Technical note: The "continue with your NPQ registration" is the same content as is shown on the [finished bookend page](/get-an-identity/no-match-journey/03-allow-continue-anyway.png). It will vary based on service, so these two should remain in sync to minimise the fields a service needs to configure.

![Custom error page](01-error-page.png "Custom error page")
