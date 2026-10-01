# Verified delivery — 30 September 2026

Public repository: https://github.com/CarlosCaceres86/CarlosCaceres86.github.io
Live website: https://carloscaceres86.github.io/

GitHub confirmed public visibility, main default branch, Pages built from main/root (legacy branch deployment) and HTTPS enforced. Live home returned HTTP200 and the expected Tokenz title. The initial public deployment was b9ffcf3f939a12a1f84ba2073be9f6373243e3b5; subsequent documentation commits do not change site behavior. New repository contains only approved public site files; private app/backend source and secrets were not copied. Commit author uses repository-local GitHub noreply identity.

## Validation
- Pure demo logic:7 Node tests passed (complete/undo, point total, insufficient reward, exact boundary, single redemption, no negative undo, unknown keys, fresh/reset state).
- Static integrity:3 HTML documents,60 local document/asset/fragment links, no failures.
- Real Chrome desktop and responsive mobile widths1440/768/390/320px: no horizontal overflow, navigation touch targets at least48px, typography/assets loaded, no console or HTTP errors.
- Both local and deployed site: keyboard skip link, tab arrow navigation, completing/undoing norms, insufficient reward, Escape/focus return, cancel preserving points, confirmation deducting points, reset and reload resetting state. Native FAQ, help/privacy and return navigation passed.
- Network contained only own-host resource requests, no cookies created. This does not imply GitHub's hosting infrastructure keeps no technical/IP logs; website privacy explains that boundary.
- Independent read-only review found decorative overflow and small touch targets; both fixed and independently verified against the deployed site.
- Desktop/mobile/reward screenshots retained outside public source, in the operator's ExtData evidence folder. No mobile app code changed; native app builds were not required for this standalone web delivery.

## Remaining launch work
User-supplied public/private contact address has not yet been provided. Help uses a clearly labeled public GitHub issue channel, with no invitation/account/children data requested. Website privacy is technical information about this site/demo; app policy/responsible entity/private support remain release prerequisites. Download and checkout are not offered. Association files require real Android signing and Apple identifiers plus device verification, so no placeholder files were published. Backend/auth/mobile links remain unchanged.

## App privacy extension verified

The prelaunch app policy is live at https://carloscaceres86.github.io/privacy/app/ and linked from /privacy/ and /help/. Owner explicitly deferred contact email; unknown controller/contact, child-data lawful basis, processor/transfer agreements and final retention remain clearly visible, not filled with invented values. No app/backend configuration or data was changed.

Local and deployed Chrome browser suite passed the new app route, deletion/rights anchors, all existing demo flows and responsive sizing at1440/768/390/320px, with no console/HTTP errors or external asset requests/cookies. Static check:4 HTML documents and84 local resource/fragment links, no failures. HTTP200 text/html verified for policy/webprivacy/help. Independent source review corrected guest invitation email and historical actor-ID deletion overclaims. Screenshot capture reloads the policy after viewport changes to avoid stale sticky-header paint artifacts. Public site build aed6a7554b7bdcba8ef2dd2cc76c336467e74dbd was built successfully before deployed checks; later QA/document-only commit preserves site content. See privacy-readiness.md for evidence and remaining operational/legal gates.

## Account erasure/policy v0.2 — 1October2026

Policy describes the actually deployed atomic account cleanup and remains prelaunch; operator metadata job is explicitly prepared and paused. New app link is available from Account and before signup. Full native evidence lives in the private app repository. Published website regression passed1440/768/390/320px, policy/deletion/rights anchors, all demo/keyboard/document flows, clean console and no third-party resource requests/cookies. Static integrity4documents/84local resources passed. App backend1128local/900hosted, focused127erasure/29retention, fullKMP575tasks. Original data compared privately unchanged; no original balances/records reproduced here. New provider/contact/retention legal criteria remain in privacy-readiness.md.

## Retención técnica/policy v0.3 — 1October2026

Owner approved a daily maintenance policy: delete the old contiguous sync-change prefix after a minimum age of30days, and resolved/expired invitation metadata after a minimum age of7days from resolution/expiry. Hosted beta job id6 was verified active on1October2026 as postgres on schedule `15 3 * * *` in GMT; its guarded transaction left other cron jobs unchanged. The first scheduled execution has not yet been observed. Devices behind the retained sync prefix receive an authoritative full snapshot. Active memberships, children, rules, rewards, points and users' daily history remain preserved. Daily execution makes these minimum-age thresholds, not exact-time deletion guarantees. The separate seven-day minimum for idempotency records remains. Purchase proof/voided events, provider logs and backups are outside these windows and still need separate criteria. Local retention assertions passed29/29 in the private app repository; no private customer data, keys or amounts are reproduced here.

The public policy remains prelaunch. Controller/contact, child-data lawful basis, processor/transfer agreements and launch readiness gates remain open. See privacy-readiness.md for the retained historical audit and current outstanding criteria.

Local site checks: `python3 scripts/check_site.py` passed with4HTML documents and84local links/assets/fragments; `node --test tests/demo.test.mjs` passed7/7; `git diff --check` passed. Playwright/Chrome smoke passed locally and on the deployed site at1440/768/390/320px, including policy/deletion/rights navigation, keyboard flow, all demo interactions, no console/HTTP errors, third-party requests or cookies. GitHub Pages build1253240839 for commit e9593cd completed successfully; the public app policy returned HTTP200 and served v0.3 with the approved retention text.

## Copias de recuperación/policy v0.4 — 1 de octubre de 2026

Published policy copy now describes encrypted recovery backups made manually on a weekly cadence, the two most recent weekly copies plus the latest pre-operation copy, and the effect of later account erasures/revocations on restoration. It states that missed runs can make copies older, that count-based rotation is not an exact 14-day deletion promise, and that restoration must stay closed if authoritative evidence for later erasures/revocations is unavailable. It does not claim an implemented replay mechanism, disaster HTTP/API recovery readiness, or legal certification. Existing 30/7 metadata retention terms and prelaunch gates remain unchanged. Backup and isolated-restore evidence is kept in the private app repo; this public repository includes no customer content, amounts, private keys, fingerprints or storage paths.

Local checks for the v0.4 page: `python3 scripts/check_site.py` passed with4HTML documents and84local links/assets/fragments; `node --test tests/demo.test.mjs` passed7/7; `git diff --check` passed. Local/deployed browser smoke and HTTP200/v0.4 confirmation are recorded after publication below.
