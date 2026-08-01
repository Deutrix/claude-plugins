# deutrix — a Claude Code plugin marketplace

Claude Code plugins published by [Deutrix](https://github.com/Deutrix).

## Add it

```
/plugin marketplace add https://github.com/Deutrix/claude-plugins.git
```

Use the **full HTTPS URL**. The `deutrix/claude-plugins` shorthand resolves to
`git@github.com:…`, which fails with `Permission denied (publickey)` on any
machine without SSH keys registered with GitHub — the repository is public, so
HTTPS needs no credentials at all.

## Plugins

| Plugin | What it does |
|---|---|
| [`ccatlas`](https://github.com/Deutrix/ccatlas) | Inventory, freshness, usage and portability for your Claude Code extensions. Finds stale pins that `/plugin update` reports as up to date. |

```
/plugin install ccatlas@deutrix
```

## How versions resolve

Entries here declare **no `version`**, deliberately. Each plugin's source is its
npm package, so the version comes from `plugin.json` inside the published
tarball and a release reaches users as soon as it is on npm — nothing here needs
editing.

Declaring a version in both places is the *double declaration* pathology
`ccatlas` exists to detect: `plugin.json` wins silently and masks the
marketplace value, so the two drift with no error anywhere.

## License

MIT
