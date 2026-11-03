# Sample: an email login route is not a completed signup

This is an internal, coordinator-assisted Naïve browser trial, not a customer engagement. The website is https://capafy.ai/login. We are not affiliated with Capafy. This sample makes no claim of a completed account, customer, payment, or zero-intervention result.

## Observed evidence

- Event 385 called browser.goto; event 386 returned the login URL.
- Screenshot completion 388 showed the welcome page with Google, GitHub and Email options.
- browser.act completion 394 followed the Email option. Screenshot completion 399 showed an email field, Terms/Privacy checkbox and Continue button. The primary coordinator inspected this image.
- Native email.inboxes returned an active inbox belonging to the agent identity. This proves an inbox exists, not that mail was delivered.
- browser.act completion 419 returned a redacted result for the email-entry action. It was not a screenshot and does not prove the server accepted that email.
- No submit receipt, OTP processing, authenticated account page, published product or sale was verified in this trace.

Event references are from the same private trial session; raw authenticated traces and signed screenshot URLs are not included in this public sample.

## Findings and retest

1. An earlier selector conversion used a position among all children where the observed XPath counted a specific element type. Use observed targets or a correctly matched selector; then inspect the destination page.
2. Reopening a browser on a new turn is necessary before acting on the previous page. The runtime closes it between turns. Retest by reopening the last verified URL before the next observation.
3. Model names in session settings do not prove that model executed. Read actual model-request spans and budget errors before attributing results.

The demonstrated outcome is narrower: an agent-operated cloud browser reached an email-only login form. Signup, email delivery, product publication and revenue require separate evidence. No invented timings, accuracy percentages, customer results or extrapolated profit are included.


This sample describes our own internal trial. For the live pilot scope, request process and price, see [the pilot offer](README.md).
