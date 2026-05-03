# nullapt skills

The official community skill index for [nullapt](https://github.com/nullapt/nullapt) — the private-first package manager for AI skills.

Browse all available skills at [nullapt.dev](https://nullapt.dev) or install directly from the CLI:

```bash
nullapt list            # browse
nullapt get web-search  # install
```

---

## Submitting a skill

1. **Fork** this repository
2. **Create** a directory under `skills/<your-skill-name>/`
3. **Add** an `index.json` file (see [schema](#indexjson-schema) below)
4. **Open a pull request** — CI will verify your manifest signature and permissions

### index.json schema

```json
{
  "name": "your-skill",
  "version": "1.0.0",
  "description": "What this skill does",
  "author": "your-github-username",
  "homepage": "https://github.com/you/your-skill-repo",
  "license": "MIT",
  "registry_url": "https://registry.nullapt.dev/v1/skills/your-skill",
  "tags": ["search", "productivity"],
  "permissions_summary": {
    "network": false,
    "filesystem": false,
    "env": []
  }
}
```

### Acceptance criteria

- Manifest must carry a valid Ed25519 signature
- `permissions_summary` must accurately reflect the `SKILL.json` permissions
- Skills requiring broad filesystem or env access require maintainer review
- No skills that exist solely to exfiltrate data or bypass sandboxing

---

## Official skills

| Name | Description | Network | Author |
|---|---|---|---|
| `web-search` | DuckDuckGo Instant Answers | `api.duckduckgo.com` | nullapt |
| `hello-skill` | Minimal greeting (starter template) | None | nullapt |

---

## Structure

```
skills/
  web-search/
    index.json
  hello-skill/
    index.json
```
