# MIDI Player

A one-page web app for listening to several MIDI files at once, like a song's stems, and seeing
every note. Nothing to install, and your files never leave your computer: the page reads them
right in the browser.

**Open it:** https://aaron-montoya.github.io/midi-player/

## How to use it

1. Drag MIDI files (`.mid`, `.midi`) anywhere onto the page, or press **Add MIDI files**. Add as
   many as you like; files with several tracks show each track separately.
2. Press **Play** (or Space). **Home** goes back to the start.
3. Each track gets its own lane in the piano roll, in the same order as the track list, with its
   own range of notes. The notes playing right now light up.
4. In the track list: **M** mutes a track, **S** solos it (only soloed tracks play), the slider
   sets its volume, and **×** removes a file.

Moving round the piano roll: drag to move, scroll for more tracks, Shift + scroll to move in time,
Ctrl + scroll (or the Zoom slider) to zoom. Click the strip along the top (the whole song) or the
bar numbers to jump. **Follow** keeps the playhead in view; **Loop** starts again at the end.

## What it sounds like

The sounds are simple built-in synths, picked from each track's General MIDI instrument (piano,
mallets, guitar, bass, strings, brass, synths...) and a synthesized drum kit for channel 10. It's
for hearing how the parts fit together, not a finished mix.

The tempo comes from each file, including tempo changes. The bar numbers follow the first file.

## How it's built

One file, `index.html`: plain HTML, CSS and JavaScript with no libraries. It reads the MIDI files
itself, plays them with the browser's Web Audio, and draws the piano roll on a canvas.
