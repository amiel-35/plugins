# amiel-35 — Claude plugins

One marketplace for all my Claude plugins. / Une seule marketplace pour tous mes plugins Claude.

| Plugin | What it is | Repo |
|---|---|---|
| **ix-skills** | Cognitive atoms — critique, decision, explorer, fact-check… — and advisory postures (red-team, contrarian…). Gestures that apply to any content. | [amiel-35/ix-skills](https://github.com/amiel-35/ix-skills) |
| **ix-recipes** | Domain recipes built on ix-skills — HR, legal, finance, procurement, product, tech — and workflows chaining the atoms. Requires ix-skills (install both). | [amiel-35/ix-recipes](https://github.com/amiel-35/ix-recipes) |
| **ghost-council** | Philosophers' reasoning methods as skills (Socrates, Popper, Wittgenstein…), and `/council` to make them deliberate. | [amiel-35/ghost-council](https://github.com/amiel-35/ghost-council) |

## Install / Installer

Claude Code:

```bash
claude plugin marketplace add amiel-35/plugins
claude plugin install ix-skills@amiel-35
claude plugin install ix-recipes@amiel-35   # requires ix-skills
claude plugin install ghost-council@amiel-35
```

Restart Claude Code. Updates: `claude plugin marketplace update amiel-35`, then `claude plugin update <plugin>@amiel-35` (e.g. `ix-skills@amiel-35`).

Cowork / claude.ai: **"Add from repository"** with `amiel-35/plugins`. Not tested yet: the catalogue is confirmed to work with the Claude Code CLI only, Cowork acceptance is unverified.

Cowork / claude.ai : **« Ajouter depuis un dépôt »** avec `amiel-35/plugins`. Pas encore testé : le catalogue est confirmé avec la CLI Claude Code seulement, l'acceptation par Cowork n'est pas vérifiée.

## How it works / Fonctionnement

This repo holds only [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json). Each entry points at the `dist/` folder of the plugin's own repo (`git-subdir` source, `main` branch), so a plugin update ships from its repo with no change here.

Each plugin repo also stays a marketplace of its own (`claude plugin marketplace add amiel-35/ix-skills`, etc.). Install a plugin from one marketplace only — the same plugin installed from two marketplaces shows up twice.

Ce repo ne contient que le manifeste. Chaque entrée pointe sur le dossier `dist/` du repo du plugin : une mise à jour se publie depuis le repo du plugin, sans rien toucher ici. Chaque repo reste aussi sa propre marketplace ; installer un plugin depuis une seule marketplace à la fois.



## License

MIT, see [LICENSE](LICENSE).
