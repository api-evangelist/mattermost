# Mattermost (mattermost)

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
