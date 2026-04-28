This is a fork of [Eijebong's](https://github.com/Eijebong) Archipelago lobby system, commonly known as Bananium.
The goal of this fork is to adapt the lobby system for use in the Archipelago core webhost as a supplemental tool
for hosts to collect yamls.  

This will involve stripping out the following features:
- Discord authentication (not desired in core space)
- Yaml checking (currently not prepared to handle updates for it)
- generation/hosting capabilities (intended just to load yamls for host player to download before generation)

The following features will be added/revised:
- Authentication for the host player via existing Session ID token for webhost
- Ability for non-host players to upload yaml files, along with an optional ID field for bundling yamls
- Ability for host player to edit/rename/delete yaml files (individual and bundled options)
- Manual password access to yaml collection lobby as a backup (same idea as server admin password on rooms)
