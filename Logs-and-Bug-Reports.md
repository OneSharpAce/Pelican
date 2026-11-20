# Pelican logs and bug reports: quick guide

This early alpha mainly collects **networking and performance data across the
3DS family**. Results from both original models (3DS, 3DS XL, and 2DS) and New
models (New 3DS, New 3DS XL, and New 2DS XL) are wanted. Successful test sessions
are useful too, especially when comparing how the same situation runs on
different models.

**Pelican can join farms hosted on PC, iOS, or Android on the same local
network.** Include the host platform, device/OS, game version, and your exact
console model in your report.

See the [release README](README.md) for setup and save backup advice.

## Find the logs

Pelican saves its logs in **`3ds\pelican` on your 3DS SD card**.
For example, if the card is drive `E:`, open `E:\3ds\pelican`.

| File | When to attach it |
| --- | --- |
| `pelican-log.txt` | Problems starting or playing the game. This is the current run's log. |
| `pelican-log-old.txt` | The previous run's log, especially if you restarted after a crash. |
| `converter-log.txt` | Problems converting, receiving, or installing files on the console. |
| `converted\convert-report.txt` | Conversion failures; include this with the converter log if available. |

**Copy the logs soon after the problem happens.** Each launch moves the game
log to `pelican-log-old.txt`, replacing the older backup. Entering the converter
screen starts a new `converter-log.txt`, replacing its previous contents.

1. Reproduce the problem if you can, and note what you were doing.
2. Exit Pelican normally if possible, then turn the console off before
   removing the SD card.
3. Put the card in your PC and copy the relevant `.txt` files somewhere safe,
   such as your Desktop. If you already restarted, copy both game logs.

For a **PC converter** problem, attach `convert-report.txt` from the output
folder you chose with `--out`. With the PC converter guide's commands, this is
`converted\convert-report.txt` beside `pelican-convert.exe`. If no report was
created, copy the error text from the terminal instead.

## Share test results and bugs on GitHub

1. Open Pelican's GitHub repository and select **Issues**. Sign in if needed.
2. Search for an existing issue or test results thread that matches. Add your
   results there, or choose **New issue** and use the relevant template if one
   is offered.
3. Give the issue a short, specific title that includes your model, such as
   **Old 3DS XL: disconnect when entering Town** or
   **New 2DS XL: 20-minute Android-hosted session results**.
4. Describe the problem using the checklist below, or the repository's template.
5. Drag the log `.txt` files into the issue description or comment box. Wait
   for their attachment links to appear, then submit the issue or comment.
   Attach the full logs so the events leading up to the error are included.

Include these details so results can be compared:

- Your Pelican release/build and **exact console model**, including whether it
  is an original or New model. For emulator results, give its name and version.
- The host platform (PC, iOS, or Android), device/OS, Stardew Valley version,
  and any mods; your converted source version and chosen language.
- Your network setup: whether the host uses Ethernet or Wi-Fi, whether both
  devices are on the same local network, and the number of connected players.
- How long you tested, what locations or activities you tried, and whether
  joining and staying connected worked.
- Any frame rate readings you observed, stutters, long pauses, input delay,
  players jumping around, or disconnects. Note when they happened and how often.
- For a problem, the steps to reproduce it, what you expected, and what happened.
- For conversion problems: PC tool, browser, or console conversion, and the
  exact error shown. Include your PC command if relevant.
- A photo or screenshot if it helps show the problem.

Attach the game log even when a session went well. If a number such as frame
rate or delay wasn't measured, describe what you observed.

For example:

```text
Pelican release/build:
Exact console model (original/New), or emulator/version:
Host platform (PC/iOS/Android), device / OS / Stardew Valley version / mods:
New or existing farmhand:
Converted source version and language:
Network setup (host Ethernet/Wi-Fi, same LAN, player count):
Session length and locations/activities tested:
Joining and connection stability:
Performance (FPS if observed, stutters, pauses, input delay):

Steps to reproduce:
1.
2.

Expected:
Actual:
How often it happens:

Logs attached:
```
