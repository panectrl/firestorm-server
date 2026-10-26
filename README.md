# Firestorm Server

Windows hosting downloads for **Firestorm**, a co-op combat overhaul for
**Alien Swarm: Reactive Drop**.

Firestorm changes Marine movement, weapons, equipment recharge, squad recovery,
enemy encounters and mission pacing. It runs its gameplay systems on the server;
players use the normal Reactive Drop client.

## Downloads

The first public hosting package is being prepared. **No binary download is
published yet.** Published packages will appear on the
[Releases page](https://github.com/panectrl/firestorm-server/releases).

This repository is the public home for hosting instructions and selected release
files. The development source repository, its history and internal build records
are separate.

## For players

Subscribe to the [Firestorm Workshop item](https://steamcommunity.com/sharedfiles/filedetails/?id=3806545472)
and join a Firestorm-enabled server when one is available. Ordinary players do
not need to download or replace a DLL.

The creator-hosted server is not online 24/7. Independent hosting downloads are
being prepared so other hosts can run their own sessions.

## For hosts

The planned package is a **Windows x86 server overlay**. It requires a separate
stock Reactive Drop server installation and matching Firestorm Workshop content.
It does not include the base game, a custom player client or the development
repository.

A hosting release will include the server DLL, required supporting files, clean
configuration templates, installation and startup scripts, checksums, and
applicable notices and credits. Use the instructions supplied with that exact
release; a matching content version is part of the installation.

Reactive Drop's [official dedicated-server instructions](https://developer.reactivedrop.com/faq.html#i-would-like-to-run-a-dedicated-server-for-alien-swarm-reactive-drop-and-dont-know-where-to-start)
explain how to install the base server through SteamCMD. Firestorm-specific
installation instructions will accompany the first hosting package.

## Updates and support

Release notes will identify the package version, supported content and validation
performed. Steam updates can replace a modified server DLL; stop the server and
follow the release's reapplication instructions after updating the base server.

For a hosting problem, open an issue with the package version, stock game build
and a description of the failure. Keep passwords and personal server settings out
of public reports.

Firestorm is a free, non-commercial community mod. Alien Swarm and Source are
Valve projects; Alien Swarm: Reactive Drop is developed by Reactive Drop Team.
Applicable upstream notices and asset credits accompany the hosting package.
