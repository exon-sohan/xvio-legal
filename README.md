# xvio-legal

Public legal documents for the **xvio Insights** Azure Marketplace offer (`callinsight`, Product ID `c5ac7a04-dbbe-459d-bb22-27f4b3d3c2e5`), published by **ExonPro Innovations LLP**.

This repo exists so that the Terms of Use and Privacy Policy URLs referenced from the Microsoft Marketplace listing resolve anonymously over the public internet (as required by Microsoft Marketplace certification policies 100.5.1.4 and 100.6.1).

---

## Documents

| File | What it is | Used in Partner Center field |
|---|---|---|
| [TERMS.md](TERMS.md) | Terms and Conditions | Properties → Legal → Terms of use URL |
| [PRIVACY.md](PRIVACY.md) | Privacy Policy | Offer Listing → Privacy policy link |

---

## Stable URLs (use these in Partner Center)

Always reference the **tagged** version, not `main`. Tags are immutable; `main` may change without notice.

```
Terms of Use:
  https://raw.githubusercontent.com/exon-sohan/xvio-legal/v1.0.1/TERMS.md

Privacy Policy:
  https://raw.githubusercontent.com/exon-sohan/xvio-legal/v1.0.1/PRIVACY.md
```

---

## Updating the documents

1. Edit `TERMS.md` and/or `PRIVACY.md` on a feature branch.
2. Bump the `Version` and `Effective Date` headers in any file you change.
3. Update the `Permanent URL` footer to match the new tag.
4. Open a PR; merge to `main`.
5. Cut a new tag (`vX.Y.Z`) — the new tag becomes the canonical URL.
6. Update the URLs in Microsoft Partner Center → callinsight → Properties → Legal *and* Offer Listing → Privacy policy link.
7. Resubmit the offer for re-certification (changing legal links triggers a re-cert per Microsoft policy).

The previous tag stays valid forever — old URLs continue to resolve.

---

## Why this repo exists

The cert blocker was that Partner Center pointed to a URL inside a **private** GitHub repository (`exon-sohan/insightflow-bicep-templates`). Microsoft's cert testers and end-users hit `raw.githubusercontent.com` without auth, so private-repo URLs always 404.

This repo is **public** and contains *only* legal documents — no source code, no infra, no secrets. Nothing here is sensitive; everything is intended to be read by the public.

ARM templates and other infrastructure live in the separate `exon-sohan/insightflow-artifacts` repo (also public, but for a different purpose).

---

*Copyright 2026 ExonPro Innovations LLP. All Rights Reserved.*
