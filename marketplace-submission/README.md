# SMB Marketplace submission bundle

This folder contains copy/paste-ready materials for submitting Field Voice to the SMB Marketplace.

## Included files

| File | Purpose |
|---|---|
| `marketplace-listing.md` | Human-readable listing copy for marketplace form fields |
| `marketplace-listing.json` | Machine-readable metadata for catalog/reviewer intake |
| `reviewer-notes.md` | Trust, safety, privacy, and validation notes for reviewers |
| `demo-script.md` | Short demo flow reviewers or sponsors can run |
| `submission-checklist.md` | Pre-submit checklist and open placeholders |
| `assets\short-description.txt` | One-line listing description |
| `assets\tags.txt` | Suggested search tags |

## Core package files

The installable skill assets are in the repo root:

- `SKILL.md`
- `README.md`
- `LICENSE`
- `examples\preset-prompts.md`
- `examples\voice-profile-template.md`
- `docs\index.html`

## Recommended submission package

Upload or attach the ZIP generated from the repo root:

```powershell
Compress-Archive -Force `
  -Path SKILL.md, README.md, LICENSE, examples, docs, marketplace-submission `
  -DestinationPath field-voice-smb-marketplace-submission.zip
```

If the marketplace form asks for a product page URL, use the hosted marketplace page if available. If that page is gated by Microsoft EMU SSO, attach `docs\index.html` as the static product page or host it in an approved internal location.
