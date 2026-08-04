# Mattermost (mattermost)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Mattermost is an open-source collaboration platform for technical teams that combines secure team messaging, workflow automation, voice/video calling, and integrations as a self-hosted Slack alternative. The Mattermost REST API exposes full programmatic control over users, teams, channels, posts, files, integrations, plugins, and webhooks.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mattermost/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mattermost/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Messaging
- Collaboration
- Team Chat
- Open Source
- DevOps
- Self-Hosted

## Timestamps

- **Created:** 2026-05-11
- **Modified:** 2026-05-29

## APIs

### Mattermost REST API

REST API v4 for managing users, teams, channels, posts, threads, files, integrations, plugins, webhooks, slash commands, and OAuth applications. Authentication uses Personal Access Tokens or session tokens via Bearer authentication.

- **Human URL:** [https://api.mattermost.com/](https://api.mattermost.com/)
- **Base URL:** `https://your-mattermost-server.com/api/v4`

#### Tags

- Messaging
- Users
- Teams
- Channels
- Posts
- Webhooks
- Integrations

#### Properties

- [Documentation](https://api.mattermost.com/)
- [API Reference](https://developers.mattermost.com/integrate/reference/rest-api/)
- [Open A P I  Source](https://github.com/mattermost/mattermost-api-reference)
- [Developer  Guide](https://developers.mattermost.com/contribute/more-info/server/rest-api/)
- [Postman Collection](collections/mattermost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mattermost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mattermost WebSocket API

Real-time WebSocket event stream for Mattermost v4. Clients connect to /api/v4/websocket, authenticate via cookie, Authorization header, or an authentication_challenge action, and receive event envelopes (event, data, broadcast, seq) covering posts, channels, users, teams, reactions, typing, status, threads, plugins, and more. Client actions user_typing, get_statuses, and get_statuses_by_ids are supported over the same socket.

- **Human URL:** [https://developers.mattermost.com/api-documentation](https://developers.mattermost.com/api-documentation)
- **Base URL:** `wss://your-mattermost-server.com/api/v4/websocket`

#### Tags

- WebSocket
- Events
- Real-Time
- Messaging
- AsyncAPI

#### Properties

- [Documentation](https://developers.mattermost.com/api-documentation)
- [AsyncAPI](https://raw.githubusercontent.com/api-evangelist/mattermost/refs/heads/main/asyncapi/mattermost-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [API Reference](https://developers.mattermost.com/integrate/reference/rest-api/)
- [Postman Collection](collections/mattermost.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mattermost.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/mattermost)
- [Website](https://mattermost.com)
- [Documentation](https://docs.mattermost.com)
- [Developer  Portal](https://developers.mattermost.com/)
- [GitHub Organization](https://github.com/mattermost)
- [Sign Up](https://mattermost.com/sign-up/)
- [Pricing](https://mattermost.com/pricing/)
- [M C P Server](https://github.com/mattermost/mmctl-mcp)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
