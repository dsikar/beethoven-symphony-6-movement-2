# Score-editing workflow

This repository adapts Beethoven Symphony No. 6, movement II, for an orchestra without horns by creating B♭ trumpet parts.

- Track every subsequent score edit with a GitHub feature-request issue before editing. If the user gives an edit request in conversation, create the corresponding issue from that request and link the work to it; do not ask them to repeat it on GitHub.
- Use `feature/<issue-number>-<short-description>` branches. Reference the issue in commits and the pull request. Describe the actual musical changes and validation, including the affected bars and instruments.
- Edit `source/Beethoven_Op.68_2.mscz` as the canonical working orchestral score. Preserve unrelated existing edits and make only the requested changes.
- Treat `originals/` and `references/` as immutable reference material.
- Preserve sounding pitch, written pitch, instrument transposition, tempo, dynamics and layout unless the request requires changing them. The original horns are in B♭ basso; playback patch names do not define staff transposition.
- Validate changed passages and relevant parts in MuseScore, with playback where appropriate. Confirm unrelated notation is unchanged.
- The `.gitignore` is an explicit allowlist. Add new deliverables only when part of the requested work. Do not commit autosaves, editor backups, sound libraries or unrelated local drafts.
