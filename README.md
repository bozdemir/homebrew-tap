# bozdemir/homebrew-tap

Homebrew formulae for [bozdemir](https://github.com/bozdemir) projects.

## Usage

```bash
brew tap bozdemir/tap
brew install <formula-name>
```

## Formulae

### claude-usage-widget

Desktop widget and CLI that shows real-time Claude Code usage limits, cost, and analytics. Menu bar icon + floating OSD overlay. [Source →](https://github.com/bozdemir/claude-usage-widget)

```bash
brew install bozdemir/tap/claude-usage-widget

claude-usage                                # launches menu bar + OSD
claude-usage --version                      # print version
claude-usage --json                         # dump full UsageStats as JSON
claude-usage --field session_utilization    # print a single field
claude-usage --export csv --days 30         # export history as CSV
```

See the [full README](https://github.com/bozdemir/claude-usage-widget#readme) for configuration, themes, webhooks, and integrations.

## Updating a formula

After a new PyPI release lands, update the corresponding `Formula/*.rb`:

```bash
# 1. Grab the new tarball URL + SHA256 from PyPI
curl -sL https://pypi.org/pypi/claude-usage-widget/X.Y.Z/json |
  python3 -c "import json,sys; d=json.load(sys.stdin); u=[x for x in d['urls'] if x['packagetype']=='sdist'][0]; print(u['url']); print(u['digests']['sha256'])"

# 2. Edit Formula/claude-usage-widget.rb — bump url, sha256, and the
#    version string inside the test block.
# 3. Commit & push.
```

## License

MIT — see each formula for the licence of the upstream project.
