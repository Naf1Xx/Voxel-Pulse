---
title: Privacy notice draft
---
# Privacy notice — review draft, not effective

This is a draft for the Voxel Pulse 0.1.0 launcher and proposed project website. It must not be used as the application's final privacy URL until the operator and remaining processing details have been verified.

## Launcher and account data

The inspected 0.1.0 implementation uses Microsoft's OAuth device code flow and is designed not to collect Microsoft passwords directly. The implemented sign-in chain communicates with Microsoft identity, Xbox Live, Xbox XSTS and Minecraft Services, including entitlement and profile endpoints. Successful live sign-in and Minecraft API approval are not yet confirmed.

The account record contains the Minecraft profile identifier and username, Xbox user identifier, Microsoft refresh token, Minecraft access token and expiration time. The Windows account store uses Windows Data Protection API (DPAPI) to protect the saved data. Its implementation can remove account records and save the updated store; the complete UI sign-out and server-side revocation behavior still require verification.

## Content and diagnostics

The inspected modules include endpoints for Modrinth, CurseForge, Mojang/Minecraft downloads, Fabric, Quilt and Prism metadata. Which services are contacted depends on features and configuration; endpoint presence alone does not establish that a feature is available or a request has occurred.

Account-related log messages can contain a username. The diagnostic module contains redaction rules for common credential patterns, but this is not a guarantee that every log is anonymous. Do not post unredacted logs in public support channels.

## Proposed website

The current website preview stores language, sound, volume and visual-effects preferences using browser local storage. Its release lookup contacts the GitHub API on request. The proposed GitHub Pages host records visitor IP addresses for security. See the [GitHub privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## Third-party policies

See the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement) and the privacy information of any third-party service you choose to use.

## Items to resolve before publication

Confirm the responsible operator and privacy contact, actual storage paths and retention periods, complete deletion and revocation behavior, analytics and crash reporting, all recipients, processing purposes and legal bases, international transfers, children's data and applicable user rights. The current static review does not establish absence of telemetry or all possible network traffic. Do not use this draft as a final policy.

[Home](index.html)
