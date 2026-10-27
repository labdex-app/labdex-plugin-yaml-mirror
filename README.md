# YAML mirror

A [labdex](https://github.com/reykimedev/labdex) plugin. Writes the whole inventory as YAML to a file after every change, optionally committing it to a git repository there.

**Version** 1.0 · **Works with** labdex >=1.3,<2 · **Plugin id** `yaml-mirror`

> [!WARNING]
> Built with AI, for home labs only: labdex and its plugins were written largely with an AI
> coding assistant (Claude), directed and reviewed by a human. They haven't had an independent
> security audit and may contain security problems. Run them on a trusted home network.

## Install

It ships with labdex: **Plugins › Marketplace**, then *Install* (nothing is downloaded). Updates arrive through the official Marketplace (signed with the labdex project key).

## Settings

| Setting | Notes |
| --- | --- |
| File path | Inside the container; mount it as a volume |
| Commit to git | The folder must already be a git repository |
| Commit author |  |

## Actions

- **Write now** (run)

## Releasing

Bump `version` in `plugin.yaml`, add a `## <version>` section to `CHANGELOG.md`, commit, then
publish a GitHub release tagged `v<version>` (web UI, or `gh release create v<version> --target main --notes ""`).
The release workflow signs the plugin with the `LABDEX_SIGNING_KEY` secret and attaches `yaml-mirror-<version>.zip` to a GitHub release.
