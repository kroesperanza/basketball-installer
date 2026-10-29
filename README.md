# 🏀 Basketball Scoreboard

An **offline** Windows app for running a basketball game on three screens:

| Screen | What it shows |
| --- | --- |
| **1 – Laptop** | The controller: scores, game and shot clocks, periods, fouls, timeouts, settings and history |
| **2 – TV / projector** | The main scoreboard: team names and scores, game clock, period, fouls, timeouts and a backup shot clock |
| **3 – Second external display** | The shot clock, in very large digits |

It needs no internet, login or server. All data stays on the laptop.

## ⬇ Download

**[Download the latest version](https://github.com/kroesperanza/basketball-installer/releases/latest)**. On that page, under **Assets**, click one of:

- **`Basketball-Scoreboard-Setup-x.y.z.exe`**: the installer (recommended). It adds Start-menu and desktop shortcuts and can update itself.
- **`Basketball-Scoreboard-Portable-x.y.z.exe`**: a single file that runs without installing, for example from a USB stick.

**Requirements:** Windows 10 or 11 (64-bit). One external display is enough to start; three screens need two separate video outputs (see [Setting up the displays](#-setting-up-the-displays)).

### "Windows protected your PC"

The app is not code-signed yet, so Windows SmartScreen may warn you the first time you run it. Click **More info → Run anyway**. This is only needed once per download.

## ⟳ Updating

In the installed version, click **⟳ Update** in the controller's header, then **Check for updates**, **Download update** and **Restart & install**. The app only goes online when you click this button. The game is saved first and comes back paused, and installing is blocked while a clock is running.

The portable version opens this page instead; download the new portable file from the latest release.

## 🖥 Setting up the displays

1. Connect the TV/projector and the shot-clock display.
2. Press **Win + P** and choose **Extend** (not *Duplicate*).
3. In **Settings → System → Display**, check that the laptop is the **main display**.
4. Start the app and click **Show Main Scoreboard** and **Show Shot Clock**.

The scoreboard opens on the left-most external display and the shot clock on the next one. To choose differently, open **⚙ Settings → Displays**.

**Hardware tips**

- An **HDMI splitter does not create a second display**; it shows the same picture twice. You need two separate video outputs.
- Many laptops have HDMI plus a **USB-C / Thunderbolt** port that carries video. A USB-C-to-HDMI adapter on that port gives you the third screen.
- With only one video output, use a Thunderbolt dock with two outputs, a USB-C dock with DisplayPort MST, or a DisplayLink adapter (needs its driver).

## 🎮 Running a game

- **Scores:** +1 / +2 / +3 and −1 for each team. Click a team name to edit it; **＋ Logo** adds a logo.
- **Game clock:** **Start / Pause**, **Set time** (type `mm:ss:tt`, e.g. `07:30:00`) and **±1s**. Hundredths show in small digits.
- **Shot clock:** **24** and **14** resets, **±1s** and **Set**. It counts `10, 09 … 05`, then tenths down to `0.0`. At 0 the buzzer sounds and the game clock stops; pressing Resume restarts the shot clock from 24. **Hide shot clock** blanks it on the displays.
- **Fouls and timeouts:** **Use** charges a timeout, stops both clocks and starts the timeout countdown, with a buzzer at the start and the end.
- **Periods:** **Next ▶** moves to the next period and keeps the scores. After the last period you can **Finalize game** or **Start overtime**.
- **Undo** reverses the last score, foul, timeout or period change. **📣 Horn** sounds the buzzer by hand.
- **Rules:** FIBA (4 × 10 min) and NBA (4 × 12 min) presets, or your own, in **⚙ Settings → Game rules**.
- **Close the app** with the red **✕** at the top right. The game is saved and restored next time.

### Keyboard shortcuts

| Key | Action |
| --- | --- |
| **Space** | Start / pause the game clock |
| **H** / **A** | Home +1 / Away +1 |
| **1** / **2** | Home +2 / Away +2 |
| **3** / **4** | Home +3 / Away +3 |
| **R** / **T** | Reset shot clock to 24 / 14 |
| **N** | Next period |
| **U** | Undo |
| **Esc** | Exit full screen on the external displays |

Shortcuts can be changed or turned off in **⚙ Settings → Sound & shortcuts**. The **⌨** button shows the current list.

## 💾 Saving

The game is saved automatically after every change. If the laptop shuts down unexpectedly, the next start restores the game with the clocks paused. Finished and saved games are listed under **History**.

Data folder: `%APPDATA%\Basketball Scoreboard` (**⚙ Settings → Data → Open data folder**).

## 🛠 Troubleshooting

| Problem | Fix |
| --- | --- |
| "No external display detected" | Press **Win + P → Extend**, then click **Detect displays**. |
| Scoreboard on the wrong screen | **⚙ Settings → Displays** → choose the display. |
| Shot clock says "Display unavailable" | Only two displays are connected. Add a third (see *Hardware tips*) or assign it in **⚙ Settings → Displays**. |
| External window is not full screen | Tick **Full screen** next to its button, or press **F11** on that window. |
| No sound | **⚙ Settings → Sound & shortcuts** → enable sound and click **Test buzzer**. Check the Windows audio output. |
| Shortcuts don't work | Click an empty area of the controller (a text box may have focus) and check that shortcuts are enabled. |

## 📝 What's new

**1.5.1**
- New quit dialog showing the score, period and clock
- Larger status bar on the controller; better fit on short laptop screens

**1.5.0**
- Game clock shows hundredths; **Set time** takes `mm:ss:tt`
- Shot clock always shows two digits and reads `0.0` at zero
- Shot clock violation stops the game clock; Resume restarts the shot clock at 24
- **Hide / Show shot clock** button
- Buzzer when a timeout starts and ends; optional score chime
- Full-screen controller with a **✕** close button

**1.4.0**
- In-app updates through the **⟳ Update** button

---

Developer: **Kristian Renz O. Esperanza**
