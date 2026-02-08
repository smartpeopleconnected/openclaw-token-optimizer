# Changelog

## [1.0.7] - 2026-02-08

### Security Improvements
- **Removed agent prompt injection** from SKILL.md - a hidden HTML comment was influencing AI agent behavior without user visibility. This was flagged in a ClawHub security review.
- **Dry-run is now the default** - running `optimizer.py` without flags shows a preview only. Use `--apply` to make actual changes. This prevents accidental config modifications.
- **User confirmation before downloads** - `ollama pull` now asks for confirmation before downloading ~2GB model data.
- **Existing files are no longer overwritten** - system prompt files in `~/.openclaw/prompts/` are skipped if they already exist, preserving user customizations.

### New Features
- **7-day savings report** - after 7 days of usage, `verify.py` shows your accumulated cost savings with a weekly breakdown. This report appears once every 7 days.

### Changed
- `--dry-run` flag replaced by `--apply` flag (dry-run is now the default behavior)
- Documentation updated to reflect new `--apply` workflow

## [1.0.6] - Initial ClawHub release

- Model routing (Haiku default)
- Ollama heartbeats (free local LLM)
- Session management optimization
- Prompt caching
- Budget controls and rate limits
- Windows + Unix installers
- Verification tool
