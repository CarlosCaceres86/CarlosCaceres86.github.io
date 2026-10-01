# App privacy policy readiness — 30 September 2026

## Authorized delivery and scope
Owner requested continuing the app privacy policy and explicitly deferred creating email. Publish /privacy/app/ as a clearly marked prelaunch version, link from website privacy/help, preserve website styling and actual implementation claims. The site privacy remains separate. This is content documentation, not an app/backend change, a legal certification or an assertion of Play readiness. Controller legal identity requested asynchronously; do not infer it from GitHub profile.

## Verified inventory before the 1 October erasure fix
- Account email, password authentication, user/session identifiers; encrypted platform session secret, no plaintext password persisted in app.
- Child name/nickname and predefined avatar; no date of birth/photo upload. Norm/reward text/icon/points, assignments, daily activity, ledger, dates and actors; server plus authorized local replica/pending changes.
- Owner-selected invitee email, invitation credentials/IDs, statuses/scopes; valid credential preview may disclose child name before accepting; actual invite email generic, no child name in its current template.72h expiry is not a72h retention policy.
- Reminders local per account/device, no sync, generic notification; logout pauses but retains preferences; account deletion purges local preference state on that device.
- Android Google Play verification retains purchase token, account hash, product/state/acknowledgement and RTDN/voided records. Account deletion removes account linkage, not proof; no automatic expiry configured. Hash/token not anonymous. Google merchant credential/product not enabled; private cron paused.
- Technical telemetry intentionally avoids emails/child/domain content, while provider gateway/Auth logs can hold connection/IP information. No advertising/behavior analytics SDKs in inspected code. No GPS/camera/photo/contact/microphone/ad identifier permissions.
- Current Supabase project metadata independently verified region eu-west-1 via CLI (public metadata only); not a guarantee all auxiliary processing stays in EU. Gmail described only as documented beta SMTP setup; final transactional provider remains to be selected/confirmed.
- Deletion cascades owned workspaces/domain and memberships. Received board_invitations.invited_user_id becomesNULL but invited_email remains. Other owners' ledger/redemption rows clear actor_id, but older workspace_change_log JSON keeps prior actor UUID until workspace removal or future retention policy. These exceptions are disclosed; no blanket anonymous/full deletion promise.

App references: domain/Model.kt and design-system/ChildAvatar.kt; identity AuthRepository/AccountFlowState and platform session stores; docs/BOARD_REMINDERS.md; backend baseline create tables/record_change/triggers/delete FKs; migration20260930091458; backend MONETIZATION.md, OPERATIONS.md; CLOUD_PERMISSION_MATRIX.md; send-board-invitation/handler.ts; _shared/observability.ts. No production user rows or secrets inspected. Read-only independent review found and corrected two guest/invitation deletion overclaims.

## Launch gates still open
- [ ] Confirm controller legal identity and required contact details; no fictitious identity/address.
- [ ] Owner creates private privacy/support mailbox and external account-deletion request route; GitHub issues are not an acceptable private route. Instructions alone must not be marked a functioning external deletion flow.
- [ ] Establish and implement lawful basis/transparency/authorization for children's data, with appropriate representatives. Account contract alone does not automatically cover child data; OS permission is not GDPR consent. Do not promise nonexistent age/consent verification.
- [ ] Confirm final email provider, DPA/roles, subprocessor and international transfer arrangements for Supabase/email/Google; signed status not inferred from provider public DPA page.
- [x] Remove attributable deleted-account invitation and historical actor remnants in the live backend; preserve other owners' balances and minimum purchase proof. Accounts deleted concurrently and replicas after full log purge verified locally.
- [x] Adopt daily technical retention for sync/invitation metadata: remove the old contiguous sync-change prefix after a minimum age of30days and resolved/expired invitation metadata after a minimum age of7days from resolution/expiry. Purchase proof/voided events, provider logs and backups still need separate criteria; these windows do not mean complete deletion of all related data.
- [x] Expose policy in Account and before signup using the app's Tokenz actions and system URI handler. This does not implement consent/age verification.
- [ ] Final review and consistency with Play Data safety/audience declarations; expose policy in store when Play is configured.
- [ ] After these facts are complete, remove prelaunch notice and version the final policy. Publishing this draft does not close these gates.

## Primary references checked
- AEPD information duty: https://www.aepd.es/derechos-y-deberes/conoce-tus-derechos/derecho-de-informacion
- AEPD rights: https://www.aepd.es/derechos-y-deberes/ejerce-tus-derechos
- Google Play user data: https://support.google.com/googleplay/android-developer/answer/10144311?hl=es
- External deletion request requirements: https://support.google.com/googleplay/android-developer/answer/13327111?hl=es
- Supabase DPA/location/transfer terms: https://supabase.com/legal/customer-resources/data-processing-addendum
- Subprocessors: https://supabase.com/legal/customer-resources/subprocessor-list
- Google provider privacy: https://policies.google.com/privacy?hl=es

## Verification
Static links/IDs/assets checked with scripts/check_site.py; real Chrome checks include new policy route, deletion/rights anchors and mobile document sizing. Runtime/deployed evidence recorded in tasks/verification.md after publication. Native app/backend source unchanged.

## 1 October technical update

Policy v0.2 describes the deployed additive erasure migration, not the historical exceptions above. Real account deletion now removes received invitations attributed by UID/current verified email and clears direct account/email fields in replication history, including FK-generated tombstones. Unconfirmed addresses or unknown historical unlinked addresses are not guessed. A durable workspace watermark triggers an authoritative snapshot for older replicas, preserving other users' pending commands/idempotence. Old historical actor UUIDs with no Auth user are also scrubbed. Lifetime purchase token/hash remains under the existing server-only restoration contract.

## Retención técnica/policy v0.3 — 1 de octubre de 2026

The owner approved daily cleanup of the old contiguous workspace sync-change prefix after30days and resolved/expired invitation metadata after7days from resolution/expiry. Devices whose sync cursor falls behind the retained prefix receive an authoritative full snapshot. These jobs use minimum-age thresholds; daily execution does not promise deletion at the exact threshold. Active memberships, children, rules, rewards, points and users' daily history remain available. The existing seven-day minimum retention for idempotency records is separate. Purchase proof/voided events, provider connection/diagnostic logs and backups remain outside this change and require separate retention criteria.

Hosted beta activation was verified on1October2026. The daily job uses the approved30/7-day minimum ages; see the current verification entry for its schedule and guard checks. Its first scheduled run has not yet been observed. This version updates the public retention description only. The prelaunch notice and launch/controller, contact, child-data legal-basis, provider/transfer and external rights-request gates remain open. The earlier v0.2 prepared/paused note above is retained as a historical audit record.

Deployment to beta passed900 hosted contracts; clean local baseline/migrations passed1128, focused erasure127, retention29 and full KMP575tasks. Original accounts, family data and balances were preserved; the domain data fingerprint was compared privately and unchanged without publishing original records or amounts. Maintenance job tokenz-privacy-metadata-retention runs as postgres at03:15UTC but is inactive; proposed30/7 and alternative90/30 windows are selectable only by an operator. Full correctness details and actual native device evidence are in the app repo's docs/evidence/privacy-20261001.

## Copias de recuperación/policy v0.4 — 1 de octubre de 2026

The first real encrypted backup from hosted beta authentication and the public service was written to controlled external storage. Its encryption key is held separately in the operator's local macOS Keychain; recipient/configuration material is outside Git, and the private key existed only in a mode-0700 temporary directory as a mode-0600 file and was removed afterward. No key material or storage paths are recorded here.

The manual operating cadence is weekly: keep the two most recent weekly copies and the latest copy made before a relevant operation. There is no scheduler and no paid backup service. Missed or delayed runs can leave a copy absent or older; retaining two weekly copies does not promise universal deletion exactly 14 days after creation. Existing account deletions do not edit already-created copies immediately. A future restoration must reapply subsequent erasures and access revocations before reopening service; if authoritative evidence is unavailable, keep the restored service closed. That follow-up erasure/revocation evidence mechanism is not implemented yet. The isolated local restore was compared against the hosted source and passed data-content plus normalized schema, security, index and sequence checks. The private operator evidence is maintained in the app repository; this public record omits customer content, amounts, identifiers, fingerprints and paths.

This verifies encrypted copy creation and an isolated local restore only. It does not establish disaster HTTP/API recovery readiness, legal certification, or an implemented replay mechanism for later erasure/revocation. The existing 30-day sync-prefix and 7-day resolved/expired-invitation metadata jobs remain active and separate; purchase proof/RTDN/logs still need their own criteria. The prelaunch, controller/contact, children's-data lawful-basis, provider/transfer and fiscal gates remain open.
