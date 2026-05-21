# Submission checklist

## Required assets

- [ ] `SKILL.md`
- [ ] `README.md`
- [ ] `LICENSE`
- [ ] `examples\preset-prompts.md`
- [ ] `examples\voice-profile-template.md`
- [ ] `docs\index.html`
- [ ] `marketplace-submission\marketplace-listing.md`
- [ ] `marketplace-submission\marketplace-listing.json`
- [ ] `marketplace-submission\reviewer-notes.md`
- [ ] `marketplace-submission\demo-script.md`

## Marketplace fields

- [ ] Title: `Field Voice`
- [ ] Subtitle: `Digital-twin humanizer for CSA and field communication`
- [ ] Short description copied from `assets\short-description.txt`
- [ ] Long description copied from `marketplace-listing.md`
- [ ] Category selected
- [ ] Tags copied from `assets\tags.txt`
- [ ] Version: `1.2.0`
- [ ] License: `MIT`
- [ ] Repository URL added
- [ ] Product page URL added or alternate static page attached
- [ ] Support contact added

## Open placeholders before final submission

- [ ] Confirm final publisher name.
- [ ] Confirm support contact or distribution list.
- [ ] Confirm whether marketplace reviewers can access `https://fantastic-spoon-3q8mepw.pages.github.io/`.
- [ ] If not, host `docs\index.html` somewhere reviewers can access or attach it directly.
- [ ] Confirm whether the marketplace requires screenshots, icons, or a video demo.

## Suggested final validation

Run these before submitting:

```powershell
Set-Location "C:\Users\sacjain\OneDrive - Microsoft\Documents\Clawpilot\field-voice-skill"
git status --short
git --no-pager log --oneline -3
Compress-Archive -Force -Path SKILL.md, README.md, LICENSE, examples, docs, marketplace-submission -DestinationPath field-voice-smb-marketplace-submission.zip
```
