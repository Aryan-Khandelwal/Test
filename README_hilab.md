# RosterFlow: Provider Data Operations (prototype)

A clickable prototype of a provider-data workflow for a US health plan: roster intake, exception review, provider outreach, directory and compliance tracking, and an audit trail.

**All data is synthetic.** The plan (MidAmerica Health), providers, NPIs (prefix 9) and tax IDs (prefix 99-) are invented. Nothing connects to a real system or real person.

## What it does

- **Command center:** open exceptions, rosters waiting, and the automation policy.
- **Roster intake:** three rosters in different formats, each with a proposed column mapping and confidence score.
- **Exception review:** evidence from each source, a suggested fix, and approve, override or send-to-outreach actions.
- **Provider outreach:** a simulated verification call whose result writes back to the record.
- **Directory and compliance:** the 30-day update clock per change and an attestation readiness check.
- **Audit trail:** every automated and human action, with time and reason.

Approving a fix updates the exception queue, the compliance view and the command center together. Use "Reset data" in the sidebar to start again.

## Running it

No build step and no dependencies. Open `index.html` in a browser. The only external resource is the Inter and JetBrains Mono fonts from Google Fonts; the app works without them.

## Deploying

This folder is ready for Vercel or Netlify as a static site.

- **Netlify Drop:** drag the folder onto app.netlify.com/drop.
- **Vercel:** `npx vercel --prod` from this folder, or import the folder in the dashboard. `vercel.json` sets clean URLs and asks search engines not to index the page.

Set access to public, then test the link in an incognito window before sharing.

## Files

- `index.html`: the whole app in one file (HTML, CSS and JavaScript, with the synthetic data embedded).
- `vercel.json`: hosting settings.
- `README.md`: this file.
