# Promised Landscaping — Lead System Development

Development branch: `feature/lead-system`. Do not merge into `main` until submission, email, uploads and access control are tested.

## Current site
- Existing single-page HTML/CSS site in `index.html`.
- Preserve existing design, logo, phone links, SEO and analytics.
- Do not add customer information, private credentials, or uploaded images to GitHub.

## First release
1. Add an accessible "Request a Free Quote" form to the existing page, matching existing typography and colors.
2. Collect name, phone, email (optional), service, ZIP code, preferred schedule, project notes and optional photos.
3. Submit over HTTPS to a secure server endpoint with validation, abuse protection and rate limiting. Never embed a private API key in browser JavaScript.
4. Save leads and photos privately with least-privilege access and a clear retention policy.
5. Notify promisedlandscapingleo@gmail.com via a transactional email provider. Do not expose private mail credentials.
6. Show a success page only after confirmed server acceptance; display an error/retry option otherwise.
7. Add a password-protected owner dashboard with lead statuses (new, contacted, quoted, booked, completed, lost) and authenticated photo viewing.

## Deployment decisions to verify
- Whether the live domain is served by GitHub Pages or Hostinger, and whether Hostinger plan supports a server runtime/database.
- Select the backend accordingly. A static GitHub Pages site alone cannot securely process private photo uploads or run an authenticated dashboard.
- Test on staging, including mobile layout, spam resistance, notification delivery, upload size/type checks, and dashboard access.

## Future marketplace
Add contractor accounts, permission-separated lead routing and billing only after the direct-booking system is proven.
