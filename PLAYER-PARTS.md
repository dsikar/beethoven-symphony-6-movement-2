# B♭ trumpet player parts — movement II

Prepared for [issue #9](https://github.com/dsikar/beethoven-symphony-6-movement-2/issues/9), from the current orchestral adaptation, using MuseScore Studio 4.7.5.

Open `source/Beethoven_Op.68_2.mscz` and select **Parts** for **Trumpet 1 in B♭** or **Trumpet 2 in B♭**. Both are native linked excerpts inside the orchestral score. Edit played music in that score and re-export the PDFs after changes; PDFs are snapshots.

- [Trumpet 1 in B♭](parts/Trumpet-1-in-Bb.pdf)
- [Trumpet 2 in B♭](parts/Trumpet-2-in-Bb.pdf)

Each part has three A4 pages, 7 mm staves, multimeasure rests, system-start bar numbers and A–H at bars 18, 38, 54, 69, 79, 91, 111 and 122. Page 1 ends at bar 54; page 2 ends at bar 105. The following rests give time to turn: bars 55–56 and 106–107. Page 3 begins with the two-bar rest and then the bassoon cue at 108. Played notes retain the register agreed in #8, written G3–F5, with automatic stem directions and beaming preserved.

## Cues

Cues appear only in the player parts, in a second voice underneath the linked full-bar rest. They are small and have playback disabled note by note. At all cue bars (27, 36, 55, 56, 66 and 108), the accompanying full-bar rest hangs from the top staff line F5 into the E5 space, following the horn-part convention; its full-bar duration in 12/8 is unchanged. The label **(8va)** means the cue is shown one octave above its source, then transposed normally for B♭ trumpet, for a readable treble-clef register. Cue phrases omit slurs and ties; played articulations and ties are unchanged.

| Bars | Label | Source in current score | Parts |
| --- | --- | --- | --- |
| 27 | Vc. solo (8va) | Solo cello | Both |
| 36 | Fag. I, Va., Vc. (8va) | Bassoon 1 | Both |
| 55–56 | Vc., Kb. (8va) | Violoncello | Both |
| 66 | Va. (8va) | Viola, including grace note | Both |
| 108 | Fag. I, Va., Vc. (8va) | Bassoon 1 | Both |

Cue instruments and locations were informed by the immutable horn scans, movement II on PDF pages 2–3 and 7–8. The earlier local drafts place a cello cue at bar 28, but both current trumpet staves already play there. The current parts therefore use the solo cello at bar 27, keeping the authoritative entrance at 28. Bars 23–26 form a four-bar rest before that cue. No cue replaces a played note.

## Validation

- MuseScore loaded and saved both native excerpts. Every saved excerpt link resolves to an element in the master: 1,186 links in Trumpet 1 and 1,182 in Trumpet 2. All 404 and 406 played notes respectively match their master notes in sounding pitch and both spellings.
- All 38 cue notes per part match the named source at the documented octave, with correct B♭ spelling, small notation and `play=0`.
- MIDI exports before and after cue preparation contain identical sounding notes: 331 in Trumpet 1 and 334 in Trumpet 2 after ties are joined. Pitches, start and end times, velocities and tempo events agree exactly. Cues add zero MIDI note events. This is a MIDI playback comparison; no live MuseSounds audition is claimed.
- All six PDF pages were inspected for cues, rests, A–H, stems, beaming, dynamics, spacing and page turns.
- All 18 orchestral staves retain the same notation, including pitches, durations, ties, dynamics and tempo. The comparison ignores newly assigned element IDs and MuseScore's reordering of simultaneous hairpin records at bar 128. The master stylesheet is byte-for-byte unchanged; master playback track settings are unchanged.
- `originals/` and `references/` are unchanged. Original source and licence metadata remain embedded in the score and printed on the parts.

The older untracked trumpet drafts are separate historical files; the linked parts and PDFs above supersede them for this orchestral adaptation.

The rest placement was corrected in [#15](https://github.com/dsikar/beethoven-symphony-6-movement-2/issues/15) by correcting the six cue-bar rest offsets in each part. Bars 27, 36, 55, 56 and 66 use zero offset; bar 108 uses a two-space downward offset to compensate for MuseScore automatically raising the rest above the higher cue notes. Only those 12 rest positions changed in the score; the master score, part links, cues, duration values, page breaks and playback settings were preserved.
