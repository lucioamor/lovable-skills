# jevify skill version

Current version: `v1.2.0`

Source repo: `https://github.com/lucioamor/lovable-skill-jevify`

This release adds `/jevify migrate <finding>`, which moves one approved candidate to JEV behind an `off | shadow | on` flag, starting in shadow mode and keeping the current AI path as fallback. Both commands use the jevify MCP connector when it is added and run locally otherwise. `/jevify` remains read-only.
