# tribass: a volca bass for your PC

A browser version of a 3-VCO bass synth with a 16-step sequencer, laid out like the Korg volca bass.
It is a single file with no install and no build step.

**On a PC:** double-click `index.html`, or open it in Chrome or Edge. (Firefox works too, but it has no MIDI support.)

**On an iPhone or iPad:** open the GitHub Pages address (https://wojtaes.github.io/tribass/) in Safari. Tap **Turn on sound**, or any key.
To keep it as an app, tap Share → **Add to Home Screen**. It then opens full screen and keeps working offline.
In portrait the panel rearranges into two rows of 8 keys. Turn the phone sideways for the full panel.
Sound plays even with the ring/silent switch set to silent. Web MIDI is not available on iOS.

To turn on GitHub Pages: repo **Settings → Pages → Build and deployment**, choose *Deploy from a branch*, then `main` and `/ (root)`.

## What it does

- 3 VCOs (saw or square each), with PITCH 1/2/3 detune of up to ±1 octave
- VCO group modes: 1 = all three in unison, 2 = VCO 1+2 together and VCO 3 separate, 3 = parts: each VCO has its own sequence (chords recorded earlier still play paraphonically)
- Resonant low-pass VCF (CUTOFF, PEAK) with light analog-style drive
- EG with ATTACK, DECAY/RELEASE and CUTOFF EG INT, plus Sustain on/off and Amp EG on/off
- LFO with RATE and INT, triangle/square/saw waves, targets amp/pitch/cutoff, and note sync
- 16-step sequencer: realtime rec, step rec (chords too), slide, active steps, tempo 56–240 BPM
- **Motion sequence:** arm ● and turn a knob while the pattern plays, and each step remembers that knob's position. It works for cutoff, peak, EG int, attack, decay, LFO rate and int, and the three pitches. Knobs with a recording show a red dot. Turn *Play motion* off or clear it in the settings panel.
- **WAV export:** *Record* captures until you stop it, while *1 loop* and *4 loops* play the pattern from step 1 and stop on their own. Then click *Download WAV* (16-bit mono, leading and trailing silence trimmed, up to 10 minutes).
- 8 memory slots, with 5 demo patterns in M1–M5 (M1 has a cutoff motion, M5 uses three separate parts). Your pattern and slots are kept in the browser.
- An output scope, and Web MIDI input (notes, Start/Stop, and the CCs listed below)

## Playing it

| Input | Action |
| --- | --- |
| `A W S E D F T G Y H U J K O L P` | The 16 keys (C to D#) |
| `Z` / `X` | Octave down / up |
| `Space` | Play / stop (in step rec, enters a rest) |
| `R` | Arm live recording |
| Hold `Shift` | FUNC |
| Mouse | Drag knobs up/down. Shift-drag for fine moves, scroll wheel to nudge, double-click to reset. |
| Touch | Tap keys, drag knobs up/down, double-tap a knob to reset. Tap FUNC, then a key or button. |

FUNC combinations follow the panel print: FUNC + key 1–3 sets the VCO group, 4–6 the LFO targets, 7 the LFO wave, 8 LFO sync,
9/10 the VCO wave, 11 Sustain, 12 Amp EG, and 13–16 clear slides / active steps / notes / everything.
FUNC + MEMORY writes, FUNC + STEP MODE is slide edit, FUNC + ▶ is active-step edit, and FUNC + ● is step rec.
In VCO group 3 the VCO buttons select which part the keys play and record into, and FUNC + VCO mutes it. In groups 1 and 2, a VCO button mutes and FUNC + VCO switches the wave.
CLEAR PART (FUNC + key 15) clears only the selected part in group 3.
The settings panel under the synth has all of these as plain buttons.

MIDI CC: 40 octave, 41 LFO rate, 42 LFO int, 43–45 pitch 1–3, 46 attack, 47 decay/release, 48 cutoff EG int,
71 peak, 74 cutoff, 7 volume.

## Not included yet

Sync in/out, and motion for the switches (only knobs record motion).
