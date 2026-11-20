# Movement II audio export

[Download / play the MP3](audio/Beethoven-6-movement-2-trumpets-no-horns.mp3). Prepared for [#13](https://github.com/dsikar/beethoven-symphony-6-movement-2/issues/13).

## File and source

- Complete movement II, bars 1–139: **11:11.4**; MP3 container duration 671.425306 s includes encoder framing. Decoded musical audio is 671.397982 s.
- MP3, libmp3lame, **320 kbps**, **44.1 kHz**, **two channels**, ID3v2.3; 26,858,402 bytes.
- Canonical source: `source/Beethoven_Op.68_2.mscz`, reviewed main commit `c2893ec` (PR #21, dynamics audit). SHA-256: `86b879d3dd49d48a7bc65e417e6ed352a1ef575570b0eb55fd152b4ad3f84735`.
- MP3 SHA-256: `347d074f60583ed72e20160cb98b3ee5782860c34c18cded49c0ce43ed32608c`.
- Rendered using the installed **MuseScore Studio 4.7.5** and the score's saved **MuseSounds** resources, including ensemble violins/violas/cellos/basses, the separate solo cello, woodwinds and both B♭ trumpets. No forced sound-profile override or tempo change was used for the delivered render. The saved tempo is 1.25 quarter notes/second, equivalent to dotted-quarter = 50.

The canonical score, linked parts and PDFs were not edited for this export. Both retained horn tracks are already muted in the saved score; both trumpet tracks and all other orchestral tracks are unmuted, with no solo states.

## Reliable horn exclusion

Short audio controls showed that the installed command-line export did not reliably apply saved mixer mute states. An explicit `--sound-profile MuseSounds` also replaced several saved ensemble assignments with default sounds, so it was omitted from the delivered render.

The delivered audio therefore uses a **temporary export-only copy** with the two horn staves replaced by full-bar rests across all 139 bars. The staff definitions remain, preserving the positions and identities of all other instruments. The linked excerpts are omitted from that temporary archive, so their small cue notes cannot enter the orchestral render. The source score and its native parts remain unchanged on disk.

An XML comparison confirms that all **16 non-horn master staves**, all instrument definitions, tempo and saved sound/mixer/style/automation data are unchanged in that export copy. Both horn staves contain **zero notes**. This guarantees horn exclusion independently of mixer handling; no older adapted score or player-part draft was used.

Individual short renders with only Trumpet 1 notes, only Trumpet 2 notes, or only the original horn notes retained produce audible signals. Both trumpet controls show the expected opening B♭ pitches (concert B♭4 / B♭3). An all-rest control contains zero notes and produces no audio file from MuseScore's empty-performance export. A saved-resource diagnostic without a profile override retains every original track resource, including the section strings and both Trumpet sounds.

## Encoding and technical checks

MuseScore rendered 44.1 kHz stereo 32-bit floating-point WAV to a temporary file. The MP3 was encoded from that render with a single uniform gain of **-1.782 dB**, giving headroom without compression, limiting or loudness normalization. The score's mixer and musical dynamics were not altered.

- The floating-point render contains only finite samples. Its duration covers all bars and the ending fermata/decay; the final three one-second analysis windows are silent, confirming decay has finished before the file ends.
- The opening contains audio from the first second. The MP3 decodes without errors to exactly **29,608,651 stereo frames**, the same count as the source WAV, confirming no opening or ending was dropped by encoding.
- Decoded sample peak: **-1.999 dBFS**; clipped samples: **0**. FFmpeg's oversampled true-peak check reports **-2.0 dBFS**.
- Codec, 320 kbps bitrate, sample rate, channel count, file duration and tags were checked with FFprobe. The MP3 was fully decoded for the signal checks.
- Git comparison confirms the canonical score, both player PDFs, original score and reference scans are unchanged.

The renderer emitted ranged-articulation closure warnings while completing the export. This validation checks source preservation, playback isolation, pitch controls, completeness and signal quality; it does **not** claim a complete human listening audition. The MP3 is provided for final musical listening review before merge approval.

## Reproduction

1. Start from the canonical source and verify the saved mute/solo states and sound resources; preserve an unchanged snapshot.
2. In a temporary copy, rest both reference horn staves, retain all other master-staff content and global settings exactly, and omit linked excerpts. Do not save this copy over the canonical score.
3. Render that copy with `QT_QPA_PLATFORM=offscreen musescore -j <job.json>`, where the job exports WAV. Omit `--sound-profile`, retaining the saved resource assignments. Retain the ending fermata and decay.
4. Measure the floating-point peak, apply only uniform export attenuation as needed, and encode 320 kbps stereo MP3 with libmp3lame. Decode and check duration, opening/ending, peaks and integrity.
5. Confirm source/reference/PDF hashes are unchanged. Commit only the requested MP3 and its export documentation; exclude WAVs, control scores, sample libraries and logs.

Temporary working files and analysis are under `/tmp/beethoven-audio-13/`; none are committed. The installed FFmpeg is the existing snap package; WAV input was piped to the encoder to avoid its separate `/tmp` namespace. No software or sound libraries were installed.
