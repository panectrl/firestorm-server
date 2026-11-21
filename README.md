# ⚡ FIRESTORM ⚡

Windows dedicated-server downloads and setup instructions for Firestorm in
**Alien Swarm: Reactive Drop**.

Firestorm changes Marine movement, weapons, equipment recharge, squad recovery,
enemy encounters and mission pacing. Gameplay systems run on the server.

## Downloads

[Download the Windows hosting preview (v0.1.0-preview.1)](https://github.com/panectrl/firestorm-server/releases/tag/v0.1.0-preview.1).
The release includes the ZIP and its SHA-256 checksum. See the release notes for
the supported stock Reactive Drop build and matching Workshop revision.

This repository is Firestorm’s public download page for server hosts. Firestorm’s
development source is private.

## For players

Subscribe to [⚡ FIRESTORM ⚡ on Steam Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=3806545472)
and join a Firestorm-enabled server using the standard Reactive Drop client.

The creator-hosted server is not online 24/7. Community hosts can run their own
sessions using the Windows hosting preview.

## For hosts

The preview is a **Windows x86 server overlay**. It requires a separate
stock Reactive Drop server installation and matching Firestorm Workshop content.
It does not include the base game, a custom player client or the development
repository.

The ZIP includes `server.dll`, an installation and startup script with rollback,
configuration examples, checksums, and notices. Use the setup instructions in
the ZIP and install the Workshop revision listed in the release notes.

Reactive Drop's [official dedicated-server instructions](https://developer.reactivedrop.com/faq.html#i-would-like-to-run-a-dedicated-server-for-alien-swarm-reactive-drop-and-dont-know-where-to-start)
explain how to install the base server through SteamCMD.

## Updates and support

Release notes will identify the package version, supported content and validation
performed. Steam updates can replace a modified server DLL. Stop the server and
follow the release's reapplication instructions after updating the base server.

For a hosting problem, open an issue with the package version, stock game build
and a description of the failure. Keep passwords and personal server settings out
of public reports.

Firestorm is a free, non-commercial community mod. Alien Swarm and Source are
Valve projects. Alien Swarm: Reactive Drop is developed by Reactive Drop Team.
Applicable upstream notices and asset credits accompany the hosting package.
