<p align="center">
  <img src="icon.png" width="200" alt="DeliciousCoffee logo: a steaming white cup of coffee with a play symbol in the crema, on a dark brown tile">
</p>

<h1 align="center">DeliciousCoffee</h1>

<p align="center"><a href="#install">Install</a> · <a href="#whats-on-the-menu">What's on the menu</a> · <a href="#how-it-works">How it works</a> · <a href="https://github.com/c0def0rc0ffee/Engage">Engage</a> · <a href="https://github.com/c0def0rc0ffee/JellyRate">JellyRate</a> · <a href="https://github.com/c0def0rc0ffee/JellyStat">JellyStat</a></p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.2-blue" alt="Repository add-on version 1.0.2">
  <img src="https://img.shields.io/badge/Kodi-19%20Matrix%2B-17B2E7?logo=kodi&logoColor=white" alt="Kodi 19 Matrix or newer">
  <img src="https://img.shields.io/badge/platform-any%20Kodi%20box-555555" alt="Runs on any platform Kodi runs on">
</p>

A Kodi repository that installs and updates the c0def0rc0ffee add-ons, instead of fetching each zip by hand. Install it once and Kodi keeps them all fresh, like a bottomless cup.

## Install

1. In Kodi, switch on **Settings, System, Add-ons, Unknown sources** (once per box).
2. Download [repository.deliciouscoffee-1.0.2.zip](https://raw.githubusercontent.com/c0def0rc0ffee/DeliciousCoffee/repo/zips/repository.deliciouscoffee/repository.deliciouscoffee-1.0.2.zip).
3. **Settings, Add-ons, Install from zip file** and pick that zip.
4. **Settings, Add-ons, Install from repository, DeliciousCoffee** and order whatever you fancy.

From then on, updates arrive on their own whenever a new version is released.

## What's on the menu

| Add-on | What it does |
|---|---|
| [Engage](https://github.com/c0def0rc0ffee/Engage) | Personal watch schedule prompts: set weekly slots, get a nudge when one arrives |
| [JellyRate](https://github.com/c0def0rc0ffee/JellyRate) | Asks for a 1 to 10 rating after playback and sends it to Jellyfin |
| [JellyStat](https://github.com/c0def0rc0ffee/JellyStat) | Watch statistics and a viewing log from Jellyfin, inside Kodi |
| [Jellyfin Dual Play](https://github.com/c0def0rc0ffee/JellyDual) | Synchronised playback across two or more Kodi boxes sharing a Jellyfin server |

The [Functional skin](https://github.com/c0def0rc0ffee/Functional) has its own repository add-on and its own release rhythm.

## How it works

The `repo` branch is a plain file feed in the layout Kodi expects. Kodi polls `addons.xml.md5`; when it changes, Kodi reads `addons.xml` and pulls the new zip from `zips/<id>/`. No server, no service, just files.

<!--
<summary>Front page of the DeliciousCoffee feed repository.</summary>
<remarks>The feed build copies this file onto the repo branch with every publish. The install link and the version badge name the repository add-on version and need changing whenever that version is bumped.</remarks>
-->
