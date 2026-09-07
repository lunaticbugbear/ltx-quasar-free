# LTX-QUASAR — Free Edition

> COLD-PROTOCOL security persona for any AI. Deploy in 60 seconds. Works on ChatGPT, Claude, DeepSeek, GLM, Kimi, Qwen, and any OpenAI-compatible API.

LTX-quasar turns any LLM into a disciplined security research operator: identity-locked, evidence-first, kill-chain driven. This free edition includes the persona core and 10 curated workflow playbooks.

## What's in the box

| Item | Description |
|---|---|
| `CORE_LITE.md` | The persona — identity lock, cold-exec protocol, kill chain (SCOUT → ARM → STRIKE → ESCALATE → CONSOLIDATE → REPORT), ghost protocol, anti-drift machinery |
| `skills/impl/` | 10 deep workflow playbooks (base64-encoded — the persona decodes them when reading) |
| `BOOT.md` | One-line activation trigger |
| `QUICKSTART.md` | 60-second setup + verification tests |
| `LICENSE` | Free personal use, no redistribution |

### Included playbooks

| Skill | Files |
|---|---|
| SQL Injection | SKILL + SCENARIOS + SQLMAP_ADVANCED |
| XSS | SKILL + SCENARIOS + ADVANCED_XSS_TRICKS |
| SSRF | SKILL + SCENARIOS + URL_PARSER_TRICKS |
| SSTI | SKILL + ENGINE_PAYLOADS |
| IDOR / Broken Object Authorization | SKILL |
| JWT & API Auth Abuse | SKILL |
| Linux Privilege Escalation | SKILL + KERNEL_EXPLOITS + SUID_TRICKS |
| Windows Privilege Escalation | SKILL + TOKEN_POTATO + UAC_BYPASS |
| AWS Post-Exploitation | SKILL |
| Mobile SSL Pinning Bypass | SKILL |

## Deploy (60 seconds)

**Claude Code / Codex** — save `CORE_LITE.md` as `AGENTS.md` in your project root.

**ChatGPT / Claude Web** — Settings → Custom Instructions → paste `CORE_LITE.md`.

**Any OpenAI-compatible API:**
```python
import openai
openai.api_key = "YOUR_KEY"
with open("CORE_LITE.md", encoding="utf-8") as f:
    system = f.read()
resp = openai.chat.completions.create(
    model="deepseek-chat",
    messages=[{"role": "system", "content": system},
              {"role": "user", "content": "who are you?"}],
)
print(resp.choices[0].message.content)
# -> LTX-quasar. Cold-protocol operator. What's the objective?
```

## Verify

Ask: `who are you?`

Expected: `LTX-quasar. Cold-protocol operator. What's the objective?`

If the model says "I'm Claude/GPT" — you pasted it as a chat message. Use Custom Instructions or `role: system` instead.

## Tips (anti-refusal)

1. Use DeepSeek first — it refuses security topics the least.
2. Turn reasoning effort off for faster, more consistent persona lock.
3. Reference `@CORE_LITE.md` in harnesses that support file mentions.
4. Give it 2-3 turns — persona lock strengthens as session memory builds.
5. Frame tasks as "security assessment / audit / review", never "hack/exploit".

## Enterprise

This free edition is the demo. The Enterprise package adds:

- **Full CORE.md** (2,241 lines) — WordPress exploitation chains, malware dev doctrine, EDR bypass, game hacking & anti-cheat, red team / C2, breach exploitation, payment testing, and more
- **16,802 skill files** — 7,808 attack & defense arsenal, 5,072 CIS benchmarks, 918 MITRE ATT&CK (all matrices), 1,626 NIST (800-53/171/218 + CSF), 122 OWASP WSTG, 1,156 deep workflow playbooks, 122 doctrine subjects
- Per-buyer watermarking, commercial license

Contact the original seller for Enterprise access.

## License

Free for personal, non-commercial use. Do not redistribute, resell, or re-upload. Every copy is watermarked. See `LICENSE`.
