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
- [ ] Confirm and activate technical retention window for sync/invitation metadata; guarded operator maintenance is deployed but paused. Purchase proof/voided events, provider logs and backups still need separate criteria. No fabricated7/30-day full deletion guarantee.
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

Deployment to beta passed900 hosted contracts; clean local baseline/migrations passed1128, focused erasure127, retention29 and full KMP575tasks. Original3 accounts,2 workspaces,3 children and35 ledger rows/sum462 were preserved; domain data fingerprint was compared privately and unchanged. Maintenance job tokenz-privacy-metadata-retention runs as postgres at03:15UTC but is inactive; proposed30/7 and alternative90/30 windows are selectable only by an operator. Full correctness details and actual native device evidence are in the app repo's docs/evidence/privacy-20261001.
