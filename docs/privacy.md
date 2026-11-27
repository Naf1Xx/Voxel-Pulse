---
title: Privacy notice draft
---
# Privacy notice — review draft, not effective

This is a draft for the Voxel Pulse 0.1.0 launcher and proposed project website. It must not be used as the application's final privacy URL until the operator and remaining processing details have been verified.

## Project operator and privacy contact

Voxel Pulse is operated by Daniil Kuznetsov (Кузнецов Даниил), an individual developer based in Russia. For privacy enquiries, contact [voxelpulse@outlook.com](mailto:voxelpulse@outlook.com). Any additional legally required identification and contact address remain to be verified for this draft.

## Approved design requirements

The project owner has adopted the following design requirements: no developer-operated user account database; no advertising or analytics telemetry; no transmission of account tokens to the developer; diagnostic reports sent only at the user's initiative; and a means to delete account data on request. These are approved design requirements, not a certification that every current build complies. Deletion in external services and copies held by third parties may require separate action.

Владелец проекта утвердил требования к разработке: отсутствие собственной серверной базы пользовательских аккаунтов, рекламной и аналитической телеметрии и передачи токенов разработчику; отправка диагностических отчётов только по инициативе пользователя; возможность удаления данных аккаунта по запросу. Это утверждённые требования, а не подтверждение соответствия каждой текущей сборки. Удаление данных в сторонних сервисах и их копиях может требовать отдельных действий.

## Launcher and account data

The inspected 0.1.0 implementation uses Microsoft's OAuth device code flow and is designed not to collect Microsoft passwords directly. The implemented sign-in chain communicates with Microsoft identity, Xbox Live, Xbox XSTS and Minecraft Services, including entitlement and profile endpoints. Successful live sign-in and Minecraft API approval are not yet confirmed.

The account record contains the Minecraft profile identifier and username, Xbox user identifier, Microsoft refresh token, Minecraft access token and expiration time. The Windows account store uses Windows Data Protection API (DPAPI) to protect the saved data. Its implementation can remove account records and save the updated store; the complete UI sign-out and server-side revocation behavior still require verification.

## Local storage and optional Prism integration

In the inspected 0.1.0 build, the default Windows data directory is %APPDATA%/VoxelPulse (overridable). Built-in accounts are stored in config/accounts.dat. The optional Prism integration reads and can copy the existing Prism accounts.json into the launcher’s separate prism directory; DPAPI protection of the built-in store must not be assumed for this separate file. UI and CLI logs rotate at 5 MB with five archived files each. The diagnostic report writer prunes its matching local reports to ten. A static scan of 431 classes in 11 project JARs found no recognizable analytics SDK references or hard-coded developer telemetry endpoint; it does not rule out dynamic network destinations, native code, external software or changes in later builds.

## Content and diagnostics

The inspected modules include endpoints for Modrinth, CurseForge, Mojang/Minecraft downloads, Fabric, Quilt and Prism metadata. Which services are contacted depends on features and configuration; endpoint presence alone does not establish that a feature is available or a request has occurred.

Account-related log messages can contain a username. The diagnostic module contains redaction rules for common credential patterns, but this is not a guarantee that every log is anonymous. Do not post unredacted logs in public support channels.

## Website

The website stores language, sound, volume and visual-effects preferences using browser local storage. Users can clear these preferences through browser site-data settings. The reviewed website code requests public releases from the GitHub API without browser credentials. No data collection forms or analytics scripts were found in that code; this does not establish the absence of processing by the hosting provider. GitHub Pages records visitor IP addresses for security. See the [GitHub privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## Support

If users contact the project by email or GitHub, their messages, contact or account details and voluntarily provided attachments may be processed to respond to their requests. Public GitHub issues are visible to other users. Do not publish passwords, authentication tokens or unredacted diagnostic logs. Support retention and deletion procedures remain to be verified.

## Third-party policies

See the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement) and the privacy information of any third-party service you choose to use.

## Items to resolve before publication

Confirm any additional legally required operator details and contact address, actual storage paths and retention periods, complete deletion and revocation behavior, analytics and crash reporting, all recipients, processing purposes and legal bases, international transfers, children's data and applicable user rights. The current static review does not establish absence of telemetry or all possible network traffic. Do not use this draft as a final policy.

[Home](index.html)
