# Mattermost GraphQL Schema

Conceptual GraphQL schema for the [Mattermost](https://mattermost.com) open-source team messaging platform, derived from the [Mattermost REST API v4](https://api.mattermost.com/).

## Overview

Mattermost provides a comprehensive REST API v4 that exposes full programmatic control over team messaging, collaboration, integrations, and administration. This GraphQL schema translates those capabilities into a typed graph of interconnected objects.

## Schema Sources

- REST API Reference: https://api.mattermost.com/
- Developer Documentation: https://developers.mattermost.com/
- OpenAPI Reference Repository: https://github.com/mattermost/mattermost-api-reference
- GitHub Source: https://github.com/mattermost/mattermost

## Type Coverage

The schema defines **65 named types** across the following domains:

### Users & Sessions
- `User` — core user account with roles, preferences, MFA, and bot flag
- `UserProfile` — public-facing subset of user fields
- `UserSession` — authenticated session with token and team memberships
- `Status` — online/away/dnd/offline presence with DND end time
- `NotifyProps` — per-user notification configuration
- `Timezone` — automatic/manual timezone settings
- `Preferences` / `Preference` — key-value user preference store

### Teams
- `Team` — workspace with type (open/invite), invite link, and scheme
- `TeamMember` — user-team join with role flags and scheme overrides
- `TeamStats` — total and active member counts

### Channels
- `Channel` — open, private, direct, or group channel with message counts
- `ChannelMember` — user-channel join with unread state and notify props
- `ChannelMemberHistory` — join/leave audit log for a channel
- `ChannelNotifyProps` — per-channel notification overrides
- `ChannelStats` — member, guest, pinned post, and file counts
- `DirectChannel` — DM channel resolved to its two users
- `GroupChannel` — group DM resolved to its member list

### Posts & Threads
- `Post` — message with reply count, participants, metadata, and reactions
- `PostMetadata` — embeds, emojis, files, images, reactions, and priority
- `PostEmbed` — link preview or opengraph embed
- `PostPriority` — urgent/standard priority with acknowledgement request
- `PostAcknowledgement` — per-user acknowledgement of a priority post
- `Thread` — root post with reply count, participants, and follow state
- `ThreadMember` — user thread subscription with unread state
- `Reaction` — emoji reaction on a post

### Files
- `FileAttachment` — uploaded file with dimensions, MIME type, and preview

### Roles & Permissions
- `Role` — named permission set (built-in or scheme-managed)
- `Permission` — atomic capability identifier
- `Scheme` — team or channel permission scheme with default roles

### Emoji
- `Emoji` — custom emoji with creator reference

### Webhooks & Integrations
- `IncomingWebhook` — inbound webhook for posting messages
- `OutgoingWebhook` — trigger-based outbound webhook
- `Command` — slash command with autocomplete metadata
- `CommandResponse` — slash command response payload
- `OAuth2App` — registered OAuth 2.0 application

### Plugins
- `Plugin` — installed plugin with active state
- `PluginManifest` — plugin descriptor with server and webapp components
- `PluginComponent` — backend or webapp binary/bundle reference
- `PluginSettings` — plugin-specific configuration store

### Groups
- `Group` — LDAP or custom group for syncable team/channel access
- `GroupMember` — user-group association
- `GroupTeam` — group-to-team sync binding with auto-add flag
- `GroupChannel` — group-to-channel sync binding (type alias in schema)

### Audit & Compliance
- `Audit` — system-wide audit event with action, IP, and session
- `Compliance` — compliance export job descriptor
- `Log` — server log entry with level and caller info

### Bots
- `Bot` — bot account linked to a user with owner reference

### System & Config
- `System` — key-value system property
- `SystemInfo` — build metadata, server ID, and feature flags
- `Config` — full server configuration across all setting groups

### Invites
- `Invite` — shareable invite link for a team or channel
- `InviteMember` — result of inviting a specific email address

### Shared Channels & Remote Clusters
- `SharedChannel` — channel shared across a remote Mattermost cluster
- `RemoteCluster` — connected remote Mattermost server

### Playbooks (Incident Collaboration)
- `Playbook` — runbook template with checklists and automation settings
- `Checklist` — ordered list of items within a playbook
- `ChecklistItem` — individual task with assignee, state, and due date
- `PlaybookRun` — active incident run with status, timeline, and retrospective
- `PlaybookTask` — reference to a checklist item within a playbook
- `StatusUpdate` — status post linked to a playbook run
- `TimelineEvent` — audit event on a playbook run timeline
- `Retrospective` — post-incident retrospective text and publish state

### Cloud
- `CloudSubscription` — SaaS subscription with product, seats, and trial state
- `CloudCustomer` — billing entity with address and payment method
- `CloudAddress` — billing or company postal address
- `CloudPaymentMethod` — card brand, last four digits, and expiry
- `CloudAddon` — add-on product with quantity

### Import & Export
- `Import` — uploaded import file descriptor
- `Export` — async export job with status

## Root Operations

### Query
Full read access across all domains: users, teams, channels, posts, threads, files, roles, schemes, emoji, webhooks, commands, OAuth apps, plugins, groups, bots, audits, compliance, system config, statuses, preferences, shared channels, playbooks, cloud, and import/export.

### Mutation
Write operations for creating and managing all major entities including users, teams, channels, posts, reactions, files, threads, emoji, webhooks, commands, OAuth apps, plugins, bots, config, statuses, preferences, and playbooks.

## Authentication

Mattermost REST API v4 authenticates via Bearer token (Personal Access Token or session token). A GraphQL implementation would pass credentials in the `Authorization: Bearer <token>` HTTP header.

## Notes

This is a conceptual schema intended to describe the surface area of the Mattermost API in GraphQL terms. Mattermost does not currently expose a native GraphQL endpoint; this schema maps the REST API v4 resource model to GraphQL types, queries, and mutations.
