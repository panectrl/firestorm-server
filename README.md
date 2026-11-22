# ⚡ FIRESTORM ⚡

Windows dedicated-server downloads and setup instructions for Firestorm in
**Alien Swarm: Reactive Drop**.

Firestorm changes Marine movement, weapons, equipment recharge, squad recovery,
enemy encounters and mission pacing. Gameplay systems run on the server.

## Downloads

[Download the Windows hosting preview (v0.1.0-preview.2)](https://github.com/panectrl/firestorm-server/releases/tag/v0.1.0-preview.2).
The release includes the ZIP and its SHA-256 checksum. Sync the Firestorm
Workshop item and run the package’s `Check` action. Start when it reports
`workshopContent: matched`. The previous preview remains available in Releases.

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
the ZIP and match the Workshop VPK checksum listed in the release notes.

Reactive Drop's [official dedicated-server instructions](https://developer.reactivedrop.com/faq.html#i-would-like-to-run-a-dedicated-server-for-alien-swarm-reactive-drop-and-dont-know-where-to-start)
explain how to install the base server through SteamCMD.

## Activating Firestorm in Preview 2

The current public hosting ZIP does **not** automatically select the Firestorm challenge.
Complete the install and Workshop sync described in the ZIP's README first.

1. Add `rd_enable_workshop_item 3806545472` to the server's `reactivedrop/cfg/workshop.cfg`.
2. Copy `config/firestorm-activate.cfg` from the hosting ZIP to the server's `reactivedrop/cfg/` folder.
3. From PowerShell in the extracted hosting ZIP folder, run `SyncWorkshop`, wait for the
   Workshop item to finish downloading/mounting, and type `quit` in the game server console.
   Then run `Check` and `Start` (substitute your server folder if different):

   ```powershell
   .\Firestorm-Hosting.ps1 -Action SyncWorkshop -ServerRoot "C:\ReactiveDropServer"
   .\Firestorm-Hosting.ps1 -Action Check -ServerRoot "C:\ReactiveDropServer"
   .\Firestorm-Hosting.ps1 -Action Start -ServerRoot "C:\ReactiveDropServer" -Public
   ```

4. **In the running dedicated-server console**, confirm the Firestorm Workshop item is loaded,
   then enter these commands one at a time:

   ```text
   rd_workshop_list_vpk_paths
   exec firestorm-activate
   changelevel asi-jac1-landingbay_01
   rd_challenge
   ```

   The final command should report `horde_firestorm_proto`.

**Do not put `exec firestorm-activate` in `server.cfg` for this preview.** The config can
execute before Workshop mounting or during subsequent map changes. A `workshopContent: matched`
result verifies the file on disk, **not** the mounted provider, active challenge, or a
successful remote join. Verify those separately.

Firestorm-only challenge locking is **off by default**. Other challenges can be selected,
but compatibility with all third-party challenges is not yet qualified.

---
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
