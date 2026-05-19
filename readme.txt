Golds Custom Services, Inc. — Landing Site
============================================

Run by the Micek family out of Wanatah, Indiana.
A small family business that takes care of its drivers.

PUBLIC CONTACT (single point of contact: Maria)
- Email: maria@goldscustom.com
- Phone: (219) 252-7037

PUBLIC PROOF (intentionally minimal)
- USDOT 3833739 (active authority)
- Wanatah, IN
- "A small family business" — anyone who wants more can look it up.

DRIVER FLOW (gated)
1. Driver fills the public "Get in Touch" form (Driver Interest path) — name, phone, email, years driving.
2. Maria pre-screens and follows up by call/email.
3. If approved, Maria sends the application packet privately by email/text:
   - PDF: https://goldscustom.com/Golds_Driver_App_W9_Mobile.pdf  (hosted but unlinked from the site)
   - Form B (with file uploads): https://docs.google.com/forms/d/e/1FAIpQLSdJqERzoP3X6xSrzCpv7_lyq_BpU5XStxze7qmbUYK9P8Y4fQ/viewform

FILES
- index.html                          : single-page site (Home / About / Drivers / Contact)
- styles.css                          : warm family-business palette (navy / burgundy / cream / gold)
- script.js                           : footer year + mobile nav toggle
- Golds_Driver_App_W9_Mobile.pdf      : application packet — hosted but NOT linked from the site
- GOOGLE_FORM_BUILD.md                : build spec for the TWO Google Forms (A public, B private)
- img/                                : 3 truck photos (hero, fleet, drivers)
- README.txt                          : this file

DEPLOY (1-line)
- Drag the entire golds_landing/ folder onto https://app.netlify.com/drop
- Connect goldscustom.com under Netlify > Domain settings.

LOCAL PREVIEW
- python -m http.server 8000   then open http://localhost:8000

GOOGLE FORMS SETUP (REQUIRED BEFORE GOING LIVE)
FORM A - "Get in Touch" (no file uploads, embedded inline)
  1. Open the existing form:
     https://docs.google.com/forms/d/1OXwg7TJq2M5_yVkRhzF8ovihvTy8oRRg_td72ubRW5c/edit
  2. REMOVE any File Upload questions.
  3. Build it per GOOGLE_FORM_BUILD.md > "FORM A" (Driver Interest / Broker / General branches).
  4. Send > <> Embed HTML, copy the iframe src URL.
  5. Replace the iframe src in index.html (Contact section) — current src already points at this form.

FORM B - "Driver Application" (with file uploads, PRIVATE — not on site)
  1. The form already exists; ensure file-upload fields per GOOGLE_FORM_BUILD.md > "FORM B".
  2. Set form to "Restrict to people you share the link with directly" (private).
  3. Maria texts/emails the form URL + PDF URL to drivers after the screening call.

VERIFY AFTER DEPLOY
1. No "Download Application" or "Submit Application Online" buttons on the public site.
2. Drivers section CTA "Tell Us About Yourself" scrolls to Contact section.
3. Contact form (Form A) shows inline with branching by Reason for contact.
4. PDF still served at https://<your-domain>/Golds_Driver_App_W9_Mobile.pdf (HTTP 200, but no link to it on site).
