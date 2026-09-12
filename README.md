<p align="center">
  <img src="icon.png" width="256" alt="DeliciousCoffee logo">
</p>

<h1 align="center">DeliciousCoffee</h1>

<p align="center"><b>A Kodi repository serving every c0def0rc0ffee add-on.</b><br>
Install it once and Kodi keeps them all fresh, like a bottomless cup.</p>

## Why this exists

Each add-on below lives in its own repository and can be installed by hand from a zip. That works, but every update means fetching a new zip on every Kodi box. DeliciousCoffee removes that chore: it is a standard Kodi add-on repository, so Kodi discovers, installs, and updates these add-ons on its own, exactly as it does with add-ons from the official repository.

## What's on the menu

| Add-on | What it does |
|---|---|
| [Engage](https://github.com/c0def0rc0ffee/Engage) | Personal watch schedule prompts: define weekly watch slots and get prompted when they arrive |
| [JellyRate](https://github.com/c0def0rc0ffee/JellyRate) | Pops up a star rating after playback and writes the score back to Jellyfin |
| [JellyStat](https://github.com/c0def0rc0ffee/JellyStat) | Watch statistics from your Jellyfin server, browsable inside Kodi |
| [Jellyfin Dual Play](https://github.com/c0def0rc0ffee/JellyDual) | Mirrors playback from one Kodi box to a second one, in sync |
| Dreadnought | Video screensaver that loops a clip of the Dreadnought drifting through a storm until you press a key |

The [Functional skin](https://github.com/c0def0rc0ffee/Functional) is served separately by its own repository add-on, because a skin follows its own release rhythm.

## Install

1. In Kodi, enable **Settings, System, Add-ons, Unknown sources** (one time per device)
2. Download the repository add-on:

   [repository.deliciouscoffee zip](https://raw.githubusercontent.com/c0def0rc0ffee/DeliciousCoffee/repo/zips/repository.deliciouscoffee/repository.deliciouscoffee-1.0.2.zip)

3. In Kodi: **Settings, Add-ons, Install from zip file**, pick the downloaded zip
4. Then: **Settings, Add-ons, Install from repository, DeliciousCoffee**, and install whatever you fancy

From then on updates arrive automatically whenever a new version is released.

## How it works

This repository's `repo` branch is a plain file feed in the layout Kodi expects:

```
addons.xml            every add-on's manifest, with current versions
addons.xml.md5        checksum Kodi polls to spot a new release
zips/<id>/<id>-<version>.zip
```

Kodi polls the checksum, notices a change, reads the new manifest, and pulls the new zip. No server, no service, just files.

The feed is generated and pushed by a build script that verifies every zip, checks versions against manifests, and scans the whole tree before anything is published.
