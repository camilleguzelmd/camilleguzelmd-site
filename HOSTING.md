# Hosting + waitlist data — Camille Guzel MD site v0

Unpublished. Do not deploy until Camille signs off. After sign-off, CoS owns hosting.

## HIPAA architecture (Camille confirmed)

1. **Destination.** When the form goes live, it posts ONLY to Camille’s future **business Google Workspace** account under a **BAA** — a Google Sheet and/or Drive folder she creates. Not to Grok Bot. Not to Cursor. Not to a personal Gmail inbox or personal Drive that bots scrape.
2. **Bot boundary.** CoS, Correspondence, Launch, Diligence, and Personal Family **never** read waitlist/referral submissions, open that Sheet, or summarize named signups. Agents build page and form UX only.
3. **Minimal fields.** Role (future patient / referring MD / PT / other), name, email, phone optional, waitlist and/or clinic updates. No free-text clinical story.
4. **BAA gate for bots.** Until Cursor Enterprise BAA explicitly lists Grok Bot as an Eligible Service, treat all submissions as **bot-out-of-bounds** even if Camille later pastes a Sheet link into chat.
5. **Go-live.** Nothing live until she signs off. Hosting waits on CoS after sign-off.

## Live wiring (when CoS hosts — not now)

- Prefer a Google Form or Apps Script / form endpoint owned by the **Workspace** org that writes into the BAA’d Sheet.
- Form `action` must never point at a bot webhook, Cursor endpoint, or personal Gmail address.
- Keep privacy copy on the page: don’t send health details; no spam; we won’t sell your information.
- Domain: www.camilleguzelmd.com (Porkbun). DNS/hosting after sign-off is CoS.

## Local v0

- `index.html` form uses `preventDefault` and shows “This form is a preview — not collecting yet.”
- `noindex, nofollow`. Local files under `/workspace/clinic-launch-tracker/site/` only.
