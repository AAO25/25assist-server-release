# 25Assist server release

Release assets only. The [25Assist Server Manager](https://github.com/AAO25/25assist-server-manager) installs and
repairs America's Army 2.5 dedicated servers from here, so it needs nothing from SourceForge or AAO25.com and no 7-Zip.

| Asset | What it is |
|---|---|
| `server-files.json` | Every file of a complete server, per platform (`win`, `lin`), with its size and SHA-256 |
| `<sha256>.br` | One file, Brotli-compressed, named after the SHA-256 of its uncompressed content |
| `AAFiles.txt` | The wrapper's own game file list (the manager reads map names from it) |
| `mapvote-1.4.zip` | Optional: MapVote 1.4 (`mapvote.u`, `mapvote.ini`) |

The files are the AA 2.5 game data from [AAO25/25Assist-Releases](https://github.com/AAO25/25Assist-Releases),
the stock game server renamed to `serverx.exe` / `serverx`, the unchanged 8.23 server wrapper (`server.exe` /
`server-bin`), the `System/server` mod bundle (`server821.7z`) and `libstdc++.so.5` for Linux.

The manager reads `releases/latest/download/server-files.json`. A release with more than 900 assets is split:
the extra `files-<date>-N` releases hold assets only, and the main `files-<date>` release is marked latest.

Built with `tools/Publish-ServerFiles.ps1` in the manager repository.
