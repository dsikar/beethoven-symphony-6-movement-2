# Beethoven Symphony No. 6 — Movement II

We are creating B♭ trumpet parts for the second movement of Beethoven’s Symphony No. 6, Op. 68, to make up for the lack of horns in our orchestra. The original horn parts and full orchestral score provide the musical reference for deciding what the trumpets should play and in which register.

The movement is **Scene am Bach — Andante molto mosso**.

## Files

| File | Purpose |
| --- | --- |
| [`source/Beethoven_Op.68_2.mscz`](source/Beethoven_Op.68_2.mscz) | Current working orchestral score. Make future score edits here. |
| [`originals/Beethoven_Op.68_2.mscz`](originals/Beethoven_Op.68_2.mscz) | Unmodified original MuseScore score, retained for comparison. |
| [`references/Beethoven_6_Score.pdf`](references/Beethoven_6_Score.pdf) | Orchestral score supplied for ELLSO. |
| [`references/Beethoven_6_Hrns.pdf`](references/Beethoven_6_Hrns.pdf) | Original Horn I and Horn II parts supplied for ELLSO. |

The reference PDFs contain the full symphony; this project concerns movement II. On the horn scan, movement II starts at “in B, Szene am Bach” on Horn I page 2 and Horn II page 7, continuing on pages 3 and 8 respectively (PDF page numbers).

Open the working score in MuseScore Studio 4. Its instruments are assigned to MuseSounds; install the corresponding Muse Woodwinds, Muse Brass and Muse Strings libraries for that playback. Sample libraries are not included in this repository.

The original horn staves are in B♭ basso. Their transposition must be considered when adapting them for B♭ trumpets. A playback patch labelled “Horn in F” does not change the staff’s written transposition.

The working score includes **Trumpet 1 in B♭** and **Trumpet 2 in B♭**, adapted from the corresponding horn lines using octave changes that preserve both chord tones. Both trumpet parts span written **G3–F5**; [the register change log](TRUMPET-REGISTER-ADAPTATION.md) records every adjusted note by bar and position. The retained horns are muted for substitution playback, and both trumpet staves use MuseSounds Trumpet. The score also contains native linked **Trumpet 1 in B♭** and **Trumpet 2 in B♭** player parts. Open them through **Parts** in MuseScore. The three-page A4 PDFs are [Trumpet 1](parts/Trumpet-1-in-Bb.pdf) and [Trumpet 2](parts/Trumpet-2-in-Bb.pdf); [player-part notes](PLAYER-PARTS.md) describe cues, page turns and validation for [#9](https://github.com/dsikar/beethoven-symphony-6-movement-2/issues/9).

## Tracking changes

Every subsequent score change starts with a GitHub **feature request**, including corrections and engraving changes:

1. Open an issue using the feature-request template. State the affected bars and instruments, the requested change, and how to check it.
2. Work on a branch named `feature/<issue-number>-<short-description>`.
3. Reference the issue in commits and open a pull request describing the musical change and its validation. Use `Closes #<issue-number>` when the request is fully addressed.
4. Check the notation, sounding pitches, transposition, affected parts and playback as appropriate before merging.

Keep the original score and reference PDFs unchanged. Only include changes requested by the issue. Existing local drafts, exports, MuseScore backups and unrelated files are ignored by an explicit allowlist in `.gitignore`. Add any newly agreed deliverable to that allowlist in the relevant feature request.

## Sources and attribution

The original digital score comes from [OpenScore Orchestra / Hauptstimme](https://github.com/MarkGotham/Hauptstimme/tree/8f677853c45b74ca0afcd79677e5379c06c82354/data/Beethoven%2C_Ludwig_van/Symphony_No.6%2C_Op.68/2). Its metadata identifies the source edition as **IMSLP #516705**.

The original file was verified against the upstream Git blob `f9ad2b990859bf9e4c61904cd8992e34eccea302` when this repository was created. Upstream distinguishes **CC0 1.0 Universal for the score** from **CC-BY-SA for the annotations**; retain that attribution and the embedded notices. Those terms do not establish a blanket licence for the separately supplied ELLSO reference scans.

The reference PDFs were copied unchanged from the local `ELLSO/2026_Autumn` collection.
