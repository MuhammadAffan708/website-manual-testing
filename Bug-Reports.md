
# BUG-001 — Email OTP Not Received

## Bug Information

| Field | Details |
|---|---|
| Bug ID | BUG-001 |
| Title | Email OTP Not Received |
| Application | NayaPay |
| Feature | Email OTP Verification |
| Severity | High |
| Priority | High |
| Status | Open — Requires Investigation |
| Reproducibility | Reproduced multiple times |

## Environment

| Environment | Details |
|---|---|
| Device | Tecno Camon 19 Neo |
| Operating System | Android 13 |
| Application Version | 3.7.7 |
| Network | Wi-Fi |

## Description

After entering a valid email address, the application displays the message "OTP has been sent to your mail." However, the OTP email is not received in the corresponding email account, preventing the user from continuing the verification process.

## Preconditions

- NayaPay application is installed.
- User has access to a valid email account.
- Device is connected to Wi-Fi.

## Steps to Reproduce

1. Open the NayaPay application.
2. Enter a valid email address.
3. Submit the email address.
4. Observe the confirmation message.
5. Open the corresponding email account.
6. Check the Inbox and Spam/Junk folders.
7. Search for NayaPay or OTP.
8. Wait for the OTP email.

## Expected Result

The OTP email should be delivered to the entered email address so the user can continue the verification process.

## Actual Result

The application displays "OTP has been sent to your mail," but the OTP email is not received.

## Reproducibility

The issue was reproduced multiple times, including with different email addresses.

## Severity

**High** — The issue prevents users from completing the email verification process.

## Priority

**High** — Investigation and resolution are required to restore the verification flow.

## Evidence

- Screen recording of the reproduction steps is available.

## Related Test Case

- TC-001 — Verify Email OTP Delivery

## Status

**Open — Requires Investigation**


https://github.com/user-attachments/assets/01287cb3-8117-48fe-9536-5744e1e317d9



# BUG-002 — Invalid Email Format Accepted

## Bug Information

| Field | Details |
|---|---|
| Bug ID | BUG-002 |
| Title | Invalid Email Format Accepted by Email Validation |
| Application | NayaPay |
| Feature | Email Validation |
| Severity | Medium |
| Priority | Medium |
| Status | Open — Requires Investigation |
| Reproducibility | Reproduced |

## Environment

| Environment | Details |
|---|---|
| Device | Tecno Camon 19 Neo |
| Operating System | Android 13 |
| Application Version | 3.7.7 |
| Network | Wi-Fi |

## Description

The NayaPay application accepts an email address containing an unquoted double quotation mark (`"`) in the local part.

According to the RFC 5322 dot-atom syntax, a double quotation mark is not permitted in an unquoted local part. The application should validate the email format and reject the invalid input.

## Preconditions

- NayaPay application is installed.
- User is on the name and email registration screen.
- Device is connected to Wi-Fi.

## Test Data

**Invalid Email Address:**

```text
aaaaaaaaaa{}*"&*/_+$##@gmail.com
```

**Validation Reference:** RFC 5322 — Email Address Syntax

## Steps to Reproduce

1. Open the NayaPay application.
2. Navigate to the name and email registration screen.
3. Enter a first name.
4. Enter a last name.
5. Enter the invalid email address:
   `aaaaaaaaaa{}*"&*/_+$##@gmail.com`
6. Observe the email input field.
7. Check whether the Next button remains enabled.

## Expected Result

The application should identify the invalid email format and display a clear validation message, such as:

> Please enter a valid email address.

The user should not be allowed to proceed with an invalid email address.

## Actual Result

The application accepts the invalid email address and the Next button remains enabled, as shown in the attached screenshot.

## Impact

Users may enter incorrectly formatted email addresses, potentially causing issues during email verification or account registration.

## Severity

**Medium** — The issue affects input validation and may allow invalid email data to proceed.

## Priority

**Medium** — The validation behavior should be reviewed and corrected.

## Evidence

https://github.com/user-attachments/assets/1b538276-d83a-48c8-8c1c-2fdb4f4b2f08

## Related Test Case

- TC-002 — Verify Invalid Email Format Validation

## Status

**Open — Requires Investigation**


# Bug-003 — Navbar Text Overflows on Mobile Portrait View

## Environment

| Field           | Details                            |
| --------------- | ---------------------------------- |
| **Website**     | DEVFOREST AI (SMC-PRIVATE) LIMITED |
| **Device**      | Tecno Camon 19 Neo                 |
| **OS**          | Android 13                         |
| **Browser**     | Google Chrome                      |
| **Orientation** | Portrait                           |
| **Test Type**   | UI / Responsive Testing            |

## Preconditions

* Website is accessible.
* Device is connected to the internet.
* Browser is using the default zoom level.

## Steps to Reproduce

1. Open the DEVFOREST AI (SMC-PRIVATE) LIMITED website in Google Chrome.
2. Hold the device in **portrait orientation**.
3. Navigate to the affected navigation section.
4. Observe the navbar text.

## Expected Result

Navbar text should remain completely within the navigation container and should be clearly visible without overflowing or overlapping other elements.

## Actual Result

The affected navbar text extends outside the navigation container when the website is viewed in portrait orientation.

## Reproducibility

**100%**

## Severity

**Low**

## Priority

**Medium**

## Status

**Open**

## Cross-Viewport Verification

| Viewport           | Result                |
| ------------------ | --------------------- |
| Mobile — Portrait  |  Issue Reproduced    |
| Mobile — Landscape |  Working as Expected |
| Desktop            |  Working as Expected |


## Evidence

> https://github.com/user-attachments/assets/f39f1040-e22e-454c-8135-b47fdc012946

## Notes

The issue appears to be related to the responsive layout at the narrower mobile viewport.


# BUG-004 — Footer Social Media Links Redirect to Homepage

## Bug Information

| Field           | Details                 |
| --------------- | ----------------------- |
| **Bug ID**      | BUG-004                 |
| **Module**      | Website Footer          |
| **Category**    | Functional / Navigation |
| **Severity**    | Medium                  |
| **Priority**    | Medium                  |
| **Status**      | Open                    |
| **Date Tested** | 16 September 2026       |

## Description

The social media icons displayed in the website footer do not redirect users to their respective social media pages. Clicking an icon instead loads the website homepage.

## Steps to Reproduce

1. Open the **DevForest AI (SMC-Private) Limited** website.
2. Scroll down to the footer section.
3. Locate the available social media icons.
4. Click or tap the **LinkedIn** icon.
5. Observe the resulting page.
6. Repeat the test with the other available social media icons.

## Expected Result

Each social media icon should redirect the user to its corresponding official social media page.

## Actual Result

The social media icons do not redirect users to their respective social media pages. Instead, the website homepage is loaded again.

## Environment

| Field         | Details           |
| ------------- | ----------------- |
| **Platform**  | Web               |
| **Browser**   | Google Chrome     |
| **Device**    | Desktop / Mobile  |
| **Test Date** | 16 September 2026 |

## Impact

Users are unable to access the company's social media profiles through the footer links, which reduces the functionality of the website's social media navigation.

## Reproducibility

**100% — Reproduced consistently during testing.**

## Notes

The issue was observed with the available social media icons in the website footer.

### Evidence


https://github.com/user-attachments/assets/a8d98d74-e6d7-45fa-8ff2-9d014eddd206

# Bug-005 — Unexpected Page Scroll During Keyboard Navigation

| Field | Details |
| :--- | :--- |
| *Bug ID* | BUG-005 |
| *Project* | DevForest AI Website |
| *Severity* | Medium |
| *Priority* | Medium |
| *Category* | UI / Accessibility (a11y) |
| *Environment* | Windows 11 / Chrome (Latest) |

---

## 1. Summary
When navigating the website using the keyboard Tab key, the browser viewport rapidly scrolls and jumps to off-screen or misaligned elements, breaking standard visual focus sequence and degrading user experience.

## 2. Steps to Reproduce
1. Open the landing page.
2. Click near the header area to establish initial page focus.
3. Press Tab continuously to cycle through interactive elements.
4. Observe the viewport movement as focus transitions between components.

## 3. Test Results

* *Expected Result:* The focus indicator moves sequentially through visible elements while maintaining smooth, predictable viewport scrolling.
* *Actual Result:* The browser viewport executes sudden, high-speed scrolling jumps to hidden or misaligned DOM elements.

## 4. Technical Analysis & Fix Recommendation
* *Hidden Elements:* Ensure off-screen or collapsed UI components use display: none; or visibility: hidden; to exclude them from the tab order.
* *DOM Alignment:* Re-align the HTML DOM tree sequence with visual CSS placement to avoid layout jump issues caused by Flexbox/Grid ordering.
* *Tab Indices:* Remove positive integer tabindex attributes (e.g., tabindex="1"), sticking to standard document flow or tabindex="0".
## EVIDENCE


https://github.com/user-attachments/assets/3da23496-5787-4fee-97e9-b8609bfaa11f


## Bug-006 — Mismatched Label Text on 404 Error Page

### Description
The custom 404 "Page not found" page displays a small label above the heading that reads **"Coming soon"**, which contradicts the actual message below it ("Page not found"). This creates confusing/misleading messaging for the user — "Coming soon" implies the page will exist in the future, while "Page not found" implies the URL is invalid.

### Environment
- **URL:** `https://whiteboxtech.net/<invalid-path>` (e.g. `/randomtext123`)
- **Browser:** Google Chrome
- **OS:** Windows
- **Device:** Desktop

### Steps to Reproduce
1. Go to `https://whiteboxtech.net/`
2. Manually enter any invalid/non-existent path in the URL bar (e.g. `whiteboxtech.net/randomtext123`)
3. Press Enter and wait for the page to load
4. Observe the small label text above the "Page not found" heading

### Expected Result
The label above the heading should match the page's actual context — e.g. **"Error"**, **"404"**, or **"Oops!"**

### Actual Result
The label incorrectly displays **"Coming soon"**, which conflicts with the "Page not found" message directly below it.

### Screenshots
*(<img width="1920" height="1020" alt="Screenshot 2026-09-25 091406" src="https://github.com/user-attachments/assets/4c443c8e-9bc5-4516-ba08-0c4179b1f645" />
)*

### Severity
`Low`

### Priority
`Low`

### Labels
`bug` `ui` `copy` `404-page`

### Additional Notes
- Likely caused by a reused UI component (e.g. an "Under Construction" label component repurposed for the 404 template) without updating its text.
- Page also took a few seconds to load — recommend separately verifying load time isn't an unrelated performance issue.

### Suggested Fix
Update the label text on the 404 template component to reflect its actual purpose (e.g. replace "Coming soon" with "Error" or "404"), decoupling it from any "Coming Soon" component if shared.


# BUG-007 — Registration form accepts invalid email address (consecutive dots and space)

| Field | Details |
|---|---|
| Bug ID | BUG-007 |
| Module | CPB & CCS Registration Form (Homepage) |
| URL | https://pmtac.com/ |
| Severity | Medium |
| Priority | Medium |
| Type | Functional / Input Validation |
| Status | Open |
| Reported by | Muhammad Affan |
| Date reported | 2026-09-29 |
| Environment | Google Chrome 153.0.8010.50 / Windows 11 Pro (Build 26200) / Dell Latitude 5400 |

## Description
The registration form accepts an invalid email address and shows a success message. The address contains consecutive dots (..) and a space before @. Neither is allowed in a valid email address (RFC 5322), and mail providers such as Gmail cannot create such an address.

## Steps to Reproduce
1. Open https://pmtac.com/ and scroll to the "Register for PMTAC's CPB & CCS Training Programs" form.
2. Fill in First Name, Last Name and Phone with valid data.
3. Select a Program and a Preferred Training Schedule.
4. In the Email field, enter exactly: user.. @gmail.com
5. Click Send.

## Expected Result
The form shows a validation error (e.g. "Please enter a valid email address") and does not submit.

## Actual Result
The form submits and displays: "Your submission was successful".

## Impact
- Invalid emails are stored in the system.
- Follow-up emails to applicants will bounce or never arrive, so leads can be lost.
- Indicates weak or missing server-side email validation.

## Additional Test Results (same form)
| Input | Expected | Actual | Result |
|---|---|---|---|
| user..@gmail.com | Reject | Accept | Fail |

## Suggested Fix
Add server-side email validation (not only browser-side), rejecting spaces, consecutive dots, and leading/trailing dots in the local part.

## Attachments

https://github.com/user-attachments/assets/282b439a-1f4f-4679-a20c-ed4f10979fca


## References
- RFC 5322, Internet Message Format (local-part syntax)

- # BUG-008: Poor mobile Largest Contentful Paint (LCP) on homepage

| Field | Details |
|---|---|
| **Bug ID** | BUG-008 |
| **Project / Site** | Whitebox: Custom Logistics & Transportation Software |
| **URL** | https://whiteboxtech.net/ |
| **Module** | Homepage: Performance |
| **Type** | Non-functional (Performance) |
| **Severity** | Medium |
| **Priority** | High |
| **Status** | Open |
| **Reported by** | Muhammad Affan |
| **Date reported** | 2026-09-30 |
| **Found by** | Lighthouse audit (Chrome DevTools) |

---

## Summary
The homepage loads slowly on mobile. The Largest Contentful Paint (LCP) is **6.0 s**, well above Google's "good" threshold of 2.5 s, and the Lighthouse Performance score is **52/100**. Users on mobile see the main content late, which can increase bounce rate and hurt search ranking.

## Environment
| Item | Value |
|---|---|
| Browser | Google Chrome (desktop) |
| Tool | Lighthouse in Chrome DevTools |
| Mode | Navigation |
| Device | Mobile emulation |
| OS | Windows |
| Date / time | 2026-09-30, 01:34 |
| Note | Run in a regular window; browser extensions may have affected the result |

## Steps to Reproduce
1. Open Google Chrome and go to `https://whiteboxtech.net/`.
2. Press **F12** to open DevTools.
3. Open the **Lighthouse** tab.
4. Select **Mode: Navigation** and **Device: Mobile**.
5. Tick **Performance** (and the other categories).
6. Click **Analyze page load**.
7. Read the Performance score and the Metrics section.

## Expected Result
- Performance score of **90 or above**.
- LCP of **2.5 s or less**.
- FCP of **1.8 s or less**.

## Actual Result
| Metric | Actual | Target | Status |
|---|---|---|---|
| Performance score | **52** | ≥ 90 | Fail |
| Largest Contentful Paint (LCP) | **6.0 s** | ≤ 2.5 s | Fail |
| First Contentful Paint (FCP) | **1.9 s** | ≤ 1.8 s | Fail (marginal) |

Lighthouse **Diagnostics** from the same run:

| Audit | Result | Status |
|---|---|---|
| Minimize main-thread work | **4.1 s** | Fail |
| Reduce unused JavaScript | Est. savings of **513 KiB** | Fail |
| Avoid enormous network payloads | Total size **4,774 KiB** | Warning |
| Avoid long main-thread tasks | **10** long tasks found | Informational |

Other Lighthouse scores from the same run, for reference:

| Category | Score |
|---|---|
| Accessibility | 93 |
| Best Practices | 96 |
| SEO | 100 |

## Impact
- Slow perceived load on mobile devices and slower connections.
- Higher chance that users leave before the hero content appears.
- Poor Core Web Vitals (LCP) can negatively affect search ranking.

## Suspected Cause
The diagnostics point mainly to **heavy JavaScript and a large page weight**, not only the hero image:
- 4.1 s of main-thread work and 10 long tasks suggest the browser is busy running scripts, which delays rendering of the main content.
- About 513 KiB of JavaScript is unused on load.
- The total page size of 4,774 KiB is very large for a mobile visit. Images likely account for part of it, but this is not yet confirmed.

Still to confirm: the "Largest Contentful Paint element" entry in Diagnostics, and the largest files in the DevTools **Network** tab (sort by Size).

## Suggested Fix (for the development team)
- Remove or code-split unused JavaScript and load non-critical scripts later (defer / lazy-load).
- Break up long tasks so the main thread is not blocked.
- Compress and resize images; serve WebP or AVIF.
- Preload the LCP image and do not lazy-load it.
- Re-run Lighthouse to confirm LCP ≤ 2.5 s.

## Attachments
- Screenshot: Lighthouse mobile report showing Performance 52 and LCP 6.0 s
  <img width="1920" height="1080" alt="Screenshot 2026-09-30 014035" src="https://github.com/user-attachments/assets/6f18831e-0a04-4fba-a715-a1858a947f64" />

## Additional Notes
- Lighthouse results vary between runs. Re-test 2 to 3 times in an Incognito window to confirm the result is consistent.
- Also re-test on Desktop mode and compare.

















