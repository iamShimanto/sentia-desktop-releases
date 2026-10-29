# Sentia Desktop — Releases

Official release binaries for **Sentia Desktop**, the personal AI agent app
(Tauri 2 + Svelte + Rust). This repository exists only to host downloads —
it contains **no source code** (the app's source lives in a private
repository).

## Download

Grab the newest build from the
[latest release](https://github.com/iamShimanto/sentia-desktop-releases/releases/latest):

| Platform | File | How it updates |
| --- | --- | --- |
| Linux (any distro) | `Sentia Desktop_x.y.z_amd64.AppImage` | **Self-updating** — the app checks this repo and installs new versions in place |
| Debian / Ubuntu / Kali | `Sentia Desktop_x.y.z_amd64.deb` | Manual: download the new `.deb` and install it over the old one (your data is kept) |
| Fedora / RHEL | `Sentia Desktop-x.y.z-1.x86_64.rpm` | Manual: download the new `.rpm` and install it over the old one (your data is kept) |
| Windows | — | Not published yet — see the release notes of each version |

## In-app updates

Sentia Desktop checks for updates quietly at startup and from
**Settings & Appearance → About & updates**. Updates are delivered from
this repository's `latest.json` manifest and are **signature-verified**
(minisign) by the app before anything installs — a file that does not
match the maintainer's signing key is refused.

On Linux, in-app updating works for the **AppImage** build. If you
installed the `.deb` / `.rpm`, update by downloading the newer package
from the latest release and installing it manually; your accounts,
chats, skills and memory live outside the package and are preserved.

## Data & privacy

Installing or updating never uploads anything. The update check is a
single anonymous HTTPS GET of `latest.json` from GitHub.
