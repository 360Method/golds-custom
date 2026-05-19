# Google Forms — Build Sheet (TWO FORMS)

| # | Form | Audience | Where it lives |
|---|------|----------|----------------|
| A | **Get in Touch** (no file uploads) | Drivers expressing interest, brokers, shippers, general | **Embedded inline** in the Contact section |
| B | **Driver Application** (with file uploads) | Drivers Maria has pre-screened | **PRIVATE** — not linked from the public site. Maria sends the URL by email or text after the screening call. |

---

## FORM A — "Get in Touch" (PUBLIC, embedded)

**Use the existing form** at:
https://docs.google.com/forms/d/1OXwg7TJq2M5_yVkRhzF8ovihvTy8oRRg_td72ubRW5c/edit

**Important:** REMOVE any File Upload questions. Forms with uploads cannot be embedded.

### Form-level settings
- **Title:** Get in Touch — Golds Custom Services
- **Description:** Maria reads every message. Tell us how to reach you and we'll follow up.
- **Settings → Responses → Collect email addresses:** Verified
- **Make question required by default:** on
- **Settings → Presentation → Show progress bar:** on

---

### Section 1 — "Tell us who you are" (always shown)

1. **Full name** — Short answer — required
2. **Phone number** — Short answer — required
3. **Email** — Short answer — required (auto-fills from verified email)
4. **Reason for contact** — Multiple choice — required
   Options:
   - I'm a driver interested in working here
   - I'm a broker / shipper
   - General inquiry
   - **Branching ("Go to section based on answer"):**
     - Driver → Section 2 (Driver Interest)
     - Broker / shipper → Section 3 (Broker)
     - General inquiry → Section 4 (General)

---

### Section 2 — "Driver Interest"

Description: Just the basics for now. If we look like a fit on both sides, Maria will reach out to set up a real conversation.

1. **Years of driving experience** — Short answer — required
2. **Do you currently hold a valid CDL-A?** — Multiple choice (Yes / No) — required
3. **City and state where you're based** — Short answer — required
4. **Where did you hear about us?** — Short answer — optional
5. **Anything else you'd like Maria to know?** — Paragraph — optional
6. After section: **Submit form**

---

### Section 3 — "Broker / shipper"

1. **Company name** — Short answer — required
2. **Lanes / origin → destination** — Paragraph — required
3. **Equipment needed** — Multiple choice (Refrigerated / Dry van / Other) — required
4. **Anticipated volume** — Short answer — optional
5. **Notes** — Paragraph — optional
6. After section: **Submit form**

---

### Section 4 — "General inquiry"

1. **Your message** — Paragraph — required
2. After section: **Submit form**

---

### After publishing Form A
1. Click **Send → `<>`** (Embed HTML).
2. Copy the iframe **`src`** URL.
3. In `index.html`, find the iframe in the `<section id="contact">` block and replace the `src=` value.
4. Redeploy.

---

## FORM B — "Driver Application" (PRIVATE — do NOT publish on the site)

This form contains file uploads. Maria sends the link to drivers AFTER the pre-screening call. It is not linked from the public site.

**Form already exists at:**
https://docs.google.com/forms/d/e/1FAIpQLSdJqERzoP3X6xSrzCpv7_lyq_BpU5XStxze7qmbUYK9P8Y4fQ/viewform

If you need to rebuild it, the field list:

### Form-level settings
- **Title:** Driver Application — Golds Custom Services
- **Description:** Upload your filled application PDF, CDL (front + back), and DOT medical card. Google sign-in required.
- **Settings → Responses → Collect email addresses:** Verified
- **Restrict to people you share the link with directly** (this keeps it private)
- **Make question required by default:** on

### Single section
1. Full name — Short answer — required
2. Phone number — Short answer — required
3. Email — Short answer — required
4. Years of OTR experience — Short answer — required
5. Do you currently hold a valid CDL-A? — Multiple choice (Yes / No) — required
6. Current DOT medical card status — Multiple choice (Current / Expired / None) — required
7. **Filled driver application (PDF)** — File upload — required (PDF, max 10 MB)
8. **CDL — front photo** — File upload — required (JPG / PNG, max 10 MB)
9. **CDL — back photo** — File upload — required (JPG / PNG, max 10 MB)
10. **Current DOT medical card** — File upload — required (PDF / JPG / PNG, max 10 MB)
11. Anything else we should know? — Paragraph — optional

### Where Maria sends the application packet
- **PDF (still hosted on the site, but unlinked):** https://goldscustom.com/Golds_Driver_App_W9_Mobile.pdf
- **Form B (this form):** https://docs.google.com/forms/d/e/1FAIpQLSdJqERzoP3X6xSrzCpv7_lyq_BpU5XStxze7qmbUYK9P8Y4fQ/viewform

Maria text-or-emails both URLs together once a candidate is approved to apply.

---

## Notes / caveats

- File uploads in Google Forms require respondents to be signed in to a Google account. After Maria's screening call, she can confirm whether the driver has a Google account; if not, she emails the PDF and asks for replies with attachments.
- Form B responses land in Maria's Drive under "Form responses".
- Public site never exposes Form B's URL or the PDF link in any visible navigation.
