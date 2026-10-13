# tribass: a volca bass for your PC

A browser version of a 3-VCO bass synth with a 16-step sequencer, laid out like the Korg volca bass.
It is a single file with no install and no build step.

**To run it:** double-click `index.html`, or open it in Chrome or Edge. (Firefox works too, but it has no MIDI support.)

## What it does

- 3 VCOs (saw or square each), with PITCH 1/2/3 detune of up to ±1 octave
- VCO group modes: 1 = all three in unison, 2 = VCO 1+2 together and VCO 3 separate, 3 = paraphonic (up to 3 notes)
- Resonant low-pass VCF (CUTOFF, PEAK) with light analog-style drive
- EG with ATTACK, DECAY/RELEASE and CUTOFF EG INT, plus Sustain on/off and Amp EG on/off
- LFO with RATE and INT, triangle/square/saw waves, targets amp/pitch/cutoff, and note sync
- 16-step sequencer: realtime rec, step rec (chords too), slide, active steps, tempo 56–240 BPM
- 8 memory slots, with 4 demo patterns in M1–M4. Your pattern and slots are kept in the browser.
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

FUNC combinations follow the panel print: FUNC + key 1–3 sets the VCO group, 4–6 the LFO targets, 7 the LFO wave, 8 LFO sync,
9/10 the VCO wave, 11 Sustain, 12 Amp EG, and 13–16 clear slides / active steps / notes / everything.
FUNC + MEMORY writes, FUNC + STEP MODE is slide edit, FUNC + ▶ is active-step edit, and FUNC + ● is step rec.
The settings panel under the synth has all of these as plain buttons.

MIDI CC: 40 octave, 41 LFO rate, 42 LFO int, 43–45 pitch 1–3, 46 attack, 47 decay/release, 48 cutoff EG int,
71 peak, 74 cutoff, 7 volume.

## Not included yet

Motion sequence (recording knob moves), sync in/out, and separate sequence parts per VCO in group mode 3.
