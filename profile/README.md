# guild-sandbox — GitHub App & OAuth App Policy

**Owner:** InfoSec (Luther / Bhargav)  
**Last reviewed:** 06/17/2026
**Status:** Active

---

## How app installs work in this org

Org co-owners (engineering principals and technical leads) can install GitHub Apps and authorize OAuth Apps in **guild-sandbox** without filing a DevOps ticket. Self-governance is the model — you own the decision.

This policy covers both **GitHub Apps** (installed at the org level) and **OAuth Apps** (authorized by individual users or org owners) — both carry similar risks and are subject to the same exclusion list.

Before installing or authorizing an app, check the exclusion list below. If the app isn't on it, proceed. That's the entire process.

---

## Never install or authorize these

The following categories are prohibited in guild-sandbox Org. These apply to both GitHub Apps and OAuth Apps.

| Category | Why it's excluded |
|---|---|
| Apps with write access to `GuildEducationInc` Org repos | guild-sandbox is a non-production sandbox; no app installed here should be able to reach or modify code in the production org |
| Apps that exfiltrate source code to external systems not approved by InfoSec | Sending Guild code to unapproved third-party systems is a data loss risk regardless of the environment |
| Apps with any access to production AWS, databases, or internal systems | Sandbox tooling must not create a path to production infrastructure |
| Apps with known security advisories or active CVEs | Check the app's GitHub Marketplace listing and vendor security page before installing |

> **Specific named exclusions** will be listed here after InfoSec review. This section will be updated before org launch.

---

## If you install or authorize something by mistake

If you realize you've installed or authorized an app that falls into one of the categories above:

1. Remove it immediately:
   - **GitHub App:** Org Settings → GitHub Apps → Uninstall
   - **OAuth App:** Org Settings → OAuth App Policy → Revoke, or your personal Settings → Applications → Revoke
2. Post a note in `#guild-team-infosec` so InfoSec is aware — no ticket required, just visibility
3. If you're unsure whether removal is sufficient, ping Luther or Bhargav directly

---

## Audit cadence

InfoSec may review installed GitHub Apps and authorized OAuth Apps in this org on a periodic basis *(cadence TBD — to be confirmed with InfoSec)*. The published exclusion list above is the baseline they'll use. No action is required from co-owners outside of the install/remove flow described above.

---

## Questions

This is a trust-based model, not an automated enforcement system. If you have a question about a specific app — whether it's borderline, or you want a second opinion before installing — reach out to:

- **InfoSec:** Luther / Bhargav

DevOps is not in the approval chain. InfoSec is the right contact for anything security-related.
