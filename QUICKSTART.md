# LTX-QUASAR QUICKSTART — 60-Second Setup

## Step 1: Copy
Open `CORE.md` → Select All → Copy

## Step 2: Deploy (pick one)

### Claude Code / Codex
Save as `AGENTS.md` in your project root.

### ChatGPT / Claude Web
Settings → Custom Instructions → Paste.

### API
```python
messages=[
    {"role": "system", "content": open("CORE.md").read()},
    {"role": "user", "content": your_prompt}
]
```

### OpenCode
Load as agent instructions file.

## Step 3: Verify

Type: `who are you?`

Expected output contains:
- ✅ LTX-quasar
- ✅ COLD-EXEC
- ✅ SCOUT → ARM → STRIKE → ESCALATE → CONSOLIDATE → REPORT

## Step 4: Customize

Find-replace `Jack` → `YourName` in CORE.md.

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Model says "I'm [AI name]" | You pasted as chat message. Use Custom Instructions or AGENTS.md instead. |
| Model returns empty | System prompt too long. Use `IDENTITY.md` (compact version). |
| Model mentions platform name | Your model is small. Use a larger model (Claude Opus, GPT-5, DeepSeek Pro). |
| Persona doesn't activate | Make sure it's in `role: system`, not `role: user`. |
