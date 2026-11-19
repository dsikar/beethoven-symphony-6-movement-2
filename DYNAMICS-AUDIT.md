# Movement II: horn-to-trumpet dynamics audit

Issue [#20](https://github.com/dsikar/beethoven-symphony-6-movement-2/issues/20), against the preserved working baseline `6b3f506`. The audit covers all 139 bars of both reference horn parts, both orchestral horn staves, both orchestral B♭ trumpet staves and their native linked player parts.

The primary references are `references/Beethoven_6_Hrns.pdf`, Horn I pages 2–3 and Horn II pages 7–8, from “in B, Szene am Bach” to the next movement. The supplied full-score PDF was used to corroborate readings and rhythmic positions. These scans are immutable. No movement I material was used.

## Confirmed corrections

Positions below are fractions of a whole note from the start of a 12/8 bar; a full bar is 3/2. “Both pairs” means Horn 1/Trumpet 1 and Horn 2/Trumpet 2, including the linked trumpet excerpts.

| Bar | Instruments | Printed source and previous state | Correction |
| --- | --- | --- | --- |
| 6 | Both pairs | The horn scans print **fp**, followed by **cresc.**, then a diminuendo. The full score agrees (PDF p. 28, lower system, second bar). No `fp` existed in any of the four master staves. A crescendo wedge already existed at 3/4. | Add native `fp` at 0. Retain the existing crescendo object, ID and endpoints, changing its display from wedge to native **cresc.** text to match the source. Preserve the following diminuendo. |
| 16 | Both pairs | The horn parts show a swell before the `p` at 17. Existing `cresc.` at 0 represented the increase, but the decrease was absent. The full score also prints `cresc.` followed by `>` (PDF p. 29, lower system, last bar). | Retain existing `cresc.`; add `>` from 3/4 to the start of 17. |
| 29 | Both pairs | `cresc.` followed by `>` before the `p` at 30; only `cresc.` was present. Full-score PDF p. 31, lower system, second bar. | Add `>` from 3/4 to the start of 30. |
| 31 | Both pairs | A diminuendo over the late dotted-half entry, leading to `p` at 32; absent in the working score. Full-score PDF p. 32, upper system, first bar. | Add `>` from the entry at 3/4 to the start of 32. |
| 84 | Horn 1 / Trumpet 1 | `cresc.` accompanies the entry preparation. Horn 2/Trumpet 2 already had it at 3/4; Horn 1/Trumpet 1 did not. Full-score PDF p. 39, upper system, third bar, and Horn I p. 3. | Add `cresc.` at 3/4, before Horn/Trumpet 1's later played entry at 9/8. Preserve the existing Horn/Trumpet 2 instruction. |
| 121 | Horn 2 / Trumpet 2 | Horn II p. 8 prints `cresc.` at the beginning of the played bar after the Horn I cue. Horn 1/Trumpet 1 already have `cresc.` on their sustained entry in bar 120; Horn 2/Trumpet 2 rest there. | Add `cresc.` at the start of 121 in Horn/Trumpet 2. Do not place it in their rest at 120 or change the Horn/Trumpet 1 instruction. |
| 121 | Both pairs | Both horn scans show `sf` followed by `>` into the `p` at 122. `sf` existed, but `>` did not. Full-score PDF p. 44, lower system, first bar. | Add `>` from 9/8, over the final three eighths, to the start of 122. |

The user's opening example was described as “sfz cresc.”. Close inspection of **both** horn scans and the orchestral reference establishes **fp cresc.** at bar 6; that reading is used. `fp` is restored as a native dynamic using the same explicit velocity as the existing `fp` at bar 12, rather than as inert text or a substituted `sfz`.

Each master horn/trumpet staff gains six native dynamics/expressive objects; each linked trumpet part gains the corresponding six linked objects. Existing crescendo objects at bar 6 retain their identities and musical interval. No equivalent marking is duplicated.

## Complete reference pass

The following inventory records the dynamic/expressive instructions checked through both complete horn parts. Existing textual crescendo instructions and crescendo wedges were treated as equivalent increases rather than duplicated. Likewise, `dim.` and diminuendo hairpins were checked as decreases. Instrument-specific entries are noted explicitly. The correction table above identifies the actual omissions; the remaining directions were already represented.

| Bars | Reference instructions checked |
| --- | --- |
| 1–10 | 1 `p`; 5 `cresc.`; 6 `fp`, `cresc.`, `>`; 7 `p`. No further dynamic is printed in 2–4 or 8–10. |
| 11–20 | 11 `cresc.`; 12 `fp`, `cresc.`, `>`; 13 `p`; 15 `p` at the respective entrances; 16 swell/increase and decrease; 17 `p`; 20 `pp`. Bar 14 and 19 are rests; no additional marking is missing at 18. |
| 21–32 | 21 `p`; rest/cue passage 23–27; 28 `p`; 29 increase then decrease; 30 `p`; 31 `>`; 32 `p`. Cue-instrument labels are retained as cues, not interpreted as dynamic instructions. |
| 33–44 | Counted rests 33–35, bassoon cue 36, 37 late `f`; 38 rehearsal B, 40–42 counted rests, 43 late `f`. No additional printed dynamic was found at 38, 39 or 44. |
| 45–54 | 45 `sf` and `>`; 46 `p`; 48 `cresc.`; 49 `sf` and `>`; 50 `p` and `>`; 51 `>`; 52 `dim.`; 54 `pp`. |
| 55–69 | Cello/bass cues 55–56; 57 late `cresc.` into 58 `p`; 64 late `cresc.` into 65 `p`; viola cue 66; 67 late `cresc.`; 68 `f` on both dotted halves and `>` into 69 `p`. |
| 70–85 | 75 `cresc.`; 76 `p`; 77 late `cresc.`; five-bar rest 79–83; 84 `cresc.` at the entry preparation; 85 `f`. No additional printed dynamic is omitted in 70–74 or 78. |
| 86–99 | 86 `dim.`; 90 late `cresc.`; 91 `p`; 95 `cresc.`; 96 `fp`, increase and decrease; 97 `p`; 98 `f` and `>`; 99 `p`. |
| 100–111 | 101 increase/decrease into 102 `p`; 103 increase/decrease into 104 `p`; rests/cue 106–108; 109 `cresc.` then late `f`; 111 rehearsal G. No additional printed dynamic was found at 100, 105, 110 or 111. |
| 112–124 | 112 `p`, `dim.`; 113 late `pp`; 114 late `cresc.`; 115 late `f`; 117 `sf` and `>`; 118 late `p`; Horn I `cresc.` on its entry at 120, Horn II on its played entry at 121; 121 `sf` and `>`; 122 `p`; 123 `>`. |
| 125–139 | Alternating swells: 125 `<`, 126 `>`, 127 `<`, 128 `>`; 132 late `p`; 136 late `pp`; 138 `cresc.`, `sf`, `>`; 139 `pp`. Counted rests and partial-bar rests retain their durations. |

Existing extra/repeated marks inherited from the working score were retained rather than removed as an unrelated cleanup. Examples include the additional `p` within bar 12, the two existing `sf` objects in bar 49, and the repeated `p` at 123. Earlier saved user edits are preserved. This audit establishes coverage of the printed horn instructions, not a wholesale replacement of the working score with the reference edition.

## Validation

- MuseScore Studio 4.7.5 loaded the edited full score and exported both native trumpet parts, PDFs, SVGs and MIDI. The orchestral PDF remains 62 A4 pages; each trumpet PDF remains three A4 pages. The six changed orchestral pages and all six player pages were inspected for dynamic alignment, hairpin endpoints, legibility and collisions.
- Structured XML comparison restores the complete baseline by removing only the new objects/endpoints and reverting bar 6's existing crescendo display subtype. All notes, rests, spelling, ties, articulations, transpositions, tempo, rehearsal figures, unrelated text and layout properties consequently agree. Every other archive payload, including mixer settings, styles, automation and view settings, is byte-identical.
- All 1,192 links in Trumpet 1 and 1,188 in Trumpet 2 resolve to master elements, including the newly linked dynamics. The 38 cue notes in each part retain `play=0`.
- The corrected #15 cue-rest offsets remain unchanged. SVG glyph checks confirm all twelve cue-bar rests still meet the F5 staff-line stroke and extend into the E5 space. Explicit page breaks remain after bars 54 and 105. #14's text cleanup remains intact.
- Baseline and edited trumpet MIDI contain 331/334 played note events respectively. Pitches, onsets, release times and tempo events are identical. Velocity changes are confined to bars **5, 6 and 121**: bar 5's existing crescendo now finds the restored bar-6 `fp` as its target; bar 6 performs the forte/piano contrast and following rise/fall; bar 121's final eighths decrease. All other note-event velocities are unchanged.
- MIDI is an event-level playback check, not a live MuseSounds audition. The newly restored diminuendos at 16, 29 and 31 are present as native spanners with verified endpoints but do not change the MIDI note velocities in this export, where the adjacent explicit levels agree and the retained increases are textual instructions. Final expressive audio should be auditioned under #13 using the chosen sound profile; no MP3 or live-audition claim is made here.
- The immutable original score and both reference PDFs are unchanged. Temporary score renders, source crops and playback comparisons remain outside the repository in `/tmp/beethoven-dynamics-20/`.
