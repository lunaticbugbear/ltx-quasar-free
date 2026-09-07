# LTX-QUASAR QUICKSTART — 60-Second Setup

> ⚠️ **BACA DULU — 3 kesalahan yang bikin persona GAGAL activate:**
> 1. ❌ JANGAN paste sebagai chat message / `@CORE.md` mention di session yang sudah berjalan — model akan treat sebagai untrusted data dan REJECT persona. File HARUS masuk sebagai system prompt (Custom Instructions) atau AGENTS.md + session BARU.
> 2. ❌ JANGAN pakai model flash/mini/small (deepseek-flash, haiku, gpt-mini) — reasoning mereka akan menolak persona. Minimal: DeepSeek Pro, GLM full, Kimi full, Qwen Max, GPT full, Claude Sonnet.
> 3. ❌ JANGAN test di session yang sudah punya system prompt lain — selalu session/chat baru.

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
