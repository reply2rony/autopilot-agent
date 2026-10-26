# Autopilot Agent

A persistent agent, not a one-off script.

- Lives here: ~/workspace/autopilot-agent/
- Settings: settings.yaml — every tunable lives in one file. Edit it, or tell
  Vesper in chat ("set drafts to 1 per day", "switch to approval only"), and
  the next scheduled run uses the new value. No rebuild, no code change.
- Pipeline: Research -> Hooks -> Draft -> Quality check -> Post -> Reply -> Lead capture
- Quality check scores every draft (hook, originality, voice, accuracy,
  platform rules, offer fit). Below the threshold in settings.yaml, the draft
  is rewritten, never posted.
- Safety: Tiny Tales TV is excluded from automation. Rony Cn personal profile
  stays approval-gated (Meta API cannot auto-post to a personal profile like
  it can to a Page).
- State: run logs and the lead sheet live in this folder, so the agent
  remembers what it already posted, replied to, and captured.

## Platforms covered
- YouTube
- Instagram
- Facebook
- WhatsApp (1:1 follow-up only, never bulk marketing — bulk promo risks a ban)
- Google Sheet (lead capture destination)
