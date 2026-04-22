# upstream

Meta-project for active upstream source development under `RogerNavelsaker/*`.

This repo is the shared workspace entrypoint for upstream source repos and PR-carrying repos. It keeps source work separate from packaging and runtime-infra repos while still providing the same Flox, `direnv`, workspace, and helper-script experience.

## Repositories

| Repository | Focus |
| --- | --- |
| [overstory](https://github.com/RogerNavelsaker/overstory) | Active upstream source repo carrying Overstory PR branches and `dogfood` |
| [canopy](https://github.com/RogerNavelsaker/canopy) | Prompt-management source repo |
| [seeds](https://github.com/RogerNavelsaker/seeds) | Spec and planning source repo |
| [trellis](https://github.com/RogerNavelsaker/trellis) | Trellis source repo planned for upstream transfer |

## Scope

- Group active upstream repos separately from packaging repos
- Keep PR-carrying source work visible and easy to bootstrap
- Provide one workspace entrypoint for current upstream development

## Shared Workspace

- Preferred layout: clone this repo as `~/Repositories/@upstream` and keep the underlying repos as ignored child directories inside `@upstream/`
- Shell: Flox + `direnv` via [manifest.toml](/home/rona/Repositories/@upstream/.flox/env/manifest.toml) and [.envrc](/home/rona/Repositories/@upstream/.envrc)
- Workspace file: [upstream.code-workspace](/home/rona/Repositories/@upstream/upstream.code-workspace)
- Bootstrap missing child repos with `./scripts/bootstrap`
- Inspect workspace state with `./scripts/status`
- Submodules are intentionally not used

## Related Meta Projects

- [nixpkgs](https://github.com/RogerNavelsaker/nixpkgs) for packaged CLI wrappers
- [runtime-intel](https://github.com/RogerNavelsaker/runtime-intel) for code intelligence and runtime integration tooling
- [nix-repos](https://github.com/RogerNavelsaker/nix-repos) for Nix workspace tooling and shared infrastructure
