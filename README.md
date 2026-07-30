# RaidLogs Uploader

Desktop uploader for the [RaidLogs](https://www.curseforge.com/wow/addons/raidlogs) WoW addon.

RaidLogs shows **avoidable damage scores** for any player directly in your in-game tooltips — no alt-tabbing to WarcraftLogs. After each raid, open the uploader, drop your `WoWCombatLog.txt`, and your scores appear in-game automatically.

---

## Download

Go to the [**Releases**](https://github.com/ArgoEMT/RaidLogsUploader/releases/latest) page.

| Platform | File |
|---|---|
| **macOS** | `RaidLogs-Uploader-macOS-x.x.x.zip` |
| **Windows** | `RaidLogs-Uploader-Windows-x.x.x.zip` |

---

## Installation

### macOS

1. Download and extract the `.zip`.
2. Move `RaidLogs Uploader.app` to your **Applications** folder.
3. On first launch, right-click the app → **Open** to bypass Gatekeeper.

### Windows

1. Download and extract the `.zip` anywhere on your machine.
2. Run `raidlogs_windows.exe`.
3. If Windows SmartScreen appears, click **More info → Run anyway**.

---

## Setup

### Enable combat logging in WoW

In the WoW chat box, type:

```
/combatlog
```

A message in chat confirms logging is active. The log is saved to:

```
World of Warcraft\_retail_\Logs\WoWCombatLog.txt
```

You only need to do this once — WoW remembers the setting across sessions.

---

## Usage

1. **Open the uploader** after your raid session.
2. **Drop your log file** onto the upload zone (or click to browse).
3. The app parses the file locally — your raw log never leaves your machine.
4. Click **Upload** to submit your results.
5. Scores appear on player tooltips in-game within seconds.

---

## What the score means

RaidLogs only tracks mechanics a player **should handle**: avoidable hits, soaks, dispels, interrupts. Unavoidable damage is excluded.

**Score = PASS ÷ (PASS + FAIL) × 100**

A mechanic is scored as:
- `PASS` — zero failures while alive
- `FAIL` — at least one failure while alive
- `?` — never exposed to the mechanic, or dead before it was cast (excluded from the score)

Your displayed score is your **best result across all kills** of that boss at that difficulty.

---

## FAQ

**Scores are missing for some players.**  
Only players whose logs have been uploaded will have scores. More uploads from the same raid = more complete data.

**The app shows "Offline".**  
Check your internet connection. If it persists, the RaidLogs server may be temporarily unavailable — try again shortly.

**I don't see all my encounters.**  
Make sure `/combatlog` was active before the pull. Only Raid encounters are tracked.
