# SpeakerPause

A tiny macOS menu bar app that keeps your music from blasting out of the speakers.

Releases only. Download the DMG from [Releases](../../releases/latest).

## What it does

**Pause on Speaker Switch**
When audio switches to the built-in speakers (AirPods taken out, Bluetooth headphones disconnected, headphones unplugged), SpeakerPause pauses playback.

**Ghost Play Protection**
Bluetooth headphones like Beats Studio Pro can deliver a stale Play command after they drop out of range, restarting music on the Mac when you are not there. If you paused on your headphones, walked away, and playback suddenly starts again shortly after they disconnect, SpeakerPause pauses it right away. Pressing Play again goes through, so playing music on purpose still works.

Modes: Off, Smart (default), Aggressive. Pick which headphones are protected in Settings.

## Energy

No polling and no timers. The app sleeps until macOS reports an audio route or playback change, so it sits at 0% CPU.

## Install

1. Open the DMG and drag SpeakerPause onto Applications.
2. First launch: macOS says the developer cannot be verified. Open System Settings, Privacy and Security, and click "Open Anyway". If the button is missing, run:
   ```
   xattr -dr com.apple.quarantine /Applications/SpeakerPause.app
   ```
3. Allow Accessibility when asked. Ghost Play Protection needs it to pause playback.

Requires macOS 14 or newer, Apple Silicon or Intel.
