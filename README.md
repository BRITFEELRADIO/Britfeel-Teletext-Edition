<img width="1138" height="594" alt="teletex" src="https://github.com/user-attachments/assets/b328fc6b-91ce-47b3-83a0-d348ff5600e1" />
<div align="center">

  # britfeel-teletext edition.

**A real-time terminal viewer for the britfeel thread on /r9k/**  
with a live `/pol/` DEFCON threat indicator

<br>

[![Python](https://img.shields.io/badge/python-3.10+-blue?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Mac-lightgrey?style=flat-square)]()

</div>

---

<div align="center">

### What it does

Automatically finds the latest britfeel thread · streams new posts as they arrive  
tracks dubs/trips/quads/quints · monitors `/pol/` for signs of a happening

</div>

---

## Features

- 🔴 **Live post streaming** — polls the thread every 3 seconds, renders new posts instantly
- 🎲 **Roll detection** — highlights dubs, trips, quads and quints with coloured borders and banners
- 📺 **YouTube titles** — resolves YouTube links inline so you can see what people are posting
- 💬 **Quote previews** — shows a snippet of the post being replied to beneath each reply
- 👤 **User tracker** — press `U` to track any name or tripcode across the thread
- ☢️ **DEFCON indicator** — scans `/pol/` every 90 seconds for signs of a happening

---

## Install if you're a hardman

```bash
pip install requests rich
python teletext.py
```

Or build a standalone exe with PyInstaller:

```bash
pip install pyinstaller
pyinstaller --onefile teletext.py
```

The exe will be in `dist/`.

---

## Usage

Just run it — it finds the latest britfeel thread automatically.

```
python teletext.py
```

| Key | Action |
|-----|--------|
| `U` | Track a user by name or tripcode |
| `Enter` | Confirm username |
| `Backspace` | Edit username |
| `Enter` (empty) | Clear tracked user |

---

## Status bar

| Element | Meaning |
|---------|---------|
| `lid` `lad` `lod` | Running word counts for the thread |
| `d` `t` `q` `Q` | Dubs · Trips · Quads · Quints rolled so far |
| `DEFCON` | /pol/ threat level (see below) |
| `U:` | Tracked user — post count and active hours (last 2 days) |

---

## DEFCON levels

<div align="center">

| | Level | Threads lit up | Meaning |
|--|-------|---------------|---------|
| 🕊 | **COMFY** | 0 | All quiet on the western front |
| ☢ | **DEFCON 5** | 1–3 | Background noise |
| ☢☢ | **DEFCON 4** | 4–7 | Mild chatter |
| ☢☢☢ | **DEFCON 3** | 8–11 | Something worth watching |
| ☢☢☢☢ | **DEFCON 2** | 12–19 | Significant event developing |
| ☢☢☢☢☢ | **DEFCON 1** | 20+ | Absolute meltdown |

</div>

Scans the **5 most recently active** `/pol/` threads in full + catalog snippets for everything else.  
Only posts made in the **last 30 minutes** are scored. Each thread counts once regardless of hit frequency.

<details>
<summary>Keywords monitored</summary>

```
ITS HAPPENING · IT'S HAPPENING · WHAT WAS THAT · OH SHIT OH FUCK
HAPPENING THREAD · GET IN HERE · BREAKING · CONFIRMED · JUST IN
missiles launched · missile strike · missile attack
nuclear launched · launched nukes · nuclear strike · nuclear attack
nuke dropped · nukes dropped · bomb dropped · bombed
under attack · being bombed · air raid · airstrikes · airstrike
invasion began · invasion has begun · troops crossing
shots fired · war declared · war has started
nuked · nukes · nuke · warhead · ICBM · ballistic
detonation · mushroom cloud · martial law · false flag
```

</details>

---

## Requirements

- Python 3.10+
- `requests`
- `rich`
- A terminal with Unicode and colour support

---

<div align="center">

*lad · lad · lad · lad · lad*

</div>
