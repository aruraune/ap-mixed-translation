# Azur Promilia (JP) English patch - text release (format 2)

Release: 2026-11-28 07:59 UTC+8 (game 1.0.2)

The launcher updater (AzurPromiliaJP-EnglishUpdater.zip) downloads these CSVs and builds the English
game files on the player's PC from the game's **original** files. `manifest.json` is signed
(`manifest.sig`, Ed25519) and pins, for each file, the original it must start from and the exact
result (SHA-256 and size); anything else is refused.

- `text/pool.csv` (jp, en): text for the string pool
- `text/statictext.csv` (key, jp, en): UI labels in the static text bundle
- `news/news.csv` (jp, en): news articles

Originals this release is built from (`.res` paths). The updater takes them from the game folder or its
`.apen-backup` when the SHA-256 matches, else downloads them from the game's own resource server
(`<host>/<file name>`, hosts below) and checks the SHA-256 again; an already patched file is never used.

Hosts: `https://pjs-static.azurpromilia.jp/project-3/jp/windows`, `https://pjs-static-back.azurpromilia.jp/project-3/jp/windows`

| File | Size | SHA-256 |
|---|---|---|
| `raw_base_package/BundleFiles/heqmts9lcjdvbupu0x2wpg.r` | 134,055,486 | `60e09fa31ac7e43e2a74cb7e722cf19b3331a188817125a086a57a17a34987ee` |
| `default_package/BundleFiles/h3y7ujukwn9qbhoqhzkkg.r` | 4,993,822 | `9771462bacb96c7ee544fe53d0d2a4e56e3576b1336d2a2ec6653bfef1a6a138` |

The `main` branch carries the older format-1 releases (prebuilt files) for updaters installed before.
