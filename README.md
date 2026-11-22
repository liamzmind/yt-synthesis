# yt-synthesis

Verifies a YouTube channel, picks the 10 most viewed and 10 most personally relevant videos from the last 365 days, reads their transcripts and writes one source-linked synthesis report.

A Claude skill: a folder with a SKILL.md that Claude loads when your request matches its description. Self-contained, no dependencies on other skills.

**Use it when you say:** "Run a YT synthesis on @channel"

## Install

Clone into your personal skills directory and start a new Claude Code session:

```powershell
git clone https://github.com/liamzmind/yt-synthesis.git "$env:USERPROFILE\.claude\skills\yt-synthesis"
```

macOS / Linux: `git clone https://github.com/liamzmind/yt-synthesis.git ~/.claude/skills/yt-synthesis`

Other Claude surfaces: check the current Anthropic documentation for how skills are loaded.

## Notes

Works best with [yt-dlp](https://github.com/yt-dlp/yt-dlp) installed (it may warn about a missing JavaScript runtime; that was harmless in testing, and installing Deno removes it); otherwise it falls back to slower web and browser methods. Edit `references/profile.md` with your own interests, projects and goals so relevance picks match you. It never fabricates transcripts, marks unreadable videos as unavailable and keeps quotes short. Status: v0.1, limited real-world testing. The report is a personal study aid; respect each creator's work.

## License

MIT. See [LICENSE](LICENSE).

## Disclaimer

Independent community work, not affiliated with or endorsed by Anthropic.
