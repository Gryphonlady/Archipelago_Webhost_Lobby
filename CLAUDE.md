# CLAUDE.md — Archipelago Webhost Lobby Project State

## Current Status
Environment setup is complete. No Python conversion work has started yet.
Next step: Study the Rust source code and plan the Python conversion.

## What Has Been Done
- Python 3.11.9 confirmed installed
- Git 2.47.0 installed and configured
- Archipelago Webhost Lobby repo cloned to `C:\Coding\Archipelago_Webhost_Lobby` on `dev` branch
- Archipelago fork cloned to `C:\Coding\Archipelago`
- Virtual environments created for both repos
- Launcher scripts created at `C:\Coding\start_dev.ps1` and `C:\Coding\start_archipelago.ps1`
- GitHub Actions enabled on Archipelago fork
- All dependencies installed via `requirements.txt` and `ModuleUpdate.py`
- Local Archipelago web server confirmed working at `http://127.0.0.1`
- `config.yaml` created for local development (not committed — already in `.gitignore`)
- `NOTES.md` added to Archipelago fork and pushed to trigger baseline `unittests` workflow
- Baseline `unittests` workflow run initiated to confirm fork health before any changes

## Local Server Configuration
- `config.yaml` lives at `C:\Coding\Archipelago\config.yaml`
- Never commit this file — it is already in `.gitignore`
- Key settings: `PORT: 5000`, `DEBUG: true`, `HOST_ADDRESS: "127.0.0.1"`
- Database file `ap.db3` is auto-created on first server start
- Background worker database errors on first startup are harmless

## How to Start the Local Server
1. Run `start_archipelago.ps1` to open a venv-activated PowerShell in `C:\Coding\Archipelago`
2. Run `python WebHost.py`
3. Open browser to `http://127.0.0.1`
4. Stop with Ctrl+C when done

## How to Work on Conversion Code
1. Run `start_dev.ps1` to open a venv-activated PowerShell in `C:\Coding\Archipelago_Webhost_Lobby`
2. Edit files in VS Code
3. Commit after each working feature with a meaningful message

## Key Decisions Made
- Working on `dev` branch of Archipelago_Webhost_Lobby repo
- Conversion code will eventually be integrated into the Archipelago fork before PR
- `NOTES.md` tracks design decisions and converted features
- `CLAUDE.md` (this file) tracks current project state for Claude context

## Current Focus
Environment setup complete. Baseline unittests workflow triggered on Archipelago fork.
Next session: examine Rust source code to understand what the Webhost Lobby does
before writing any Python.

## Converted Features
None yet.

## Known Environment Quirks
- `_speedups` C++ module is not compiled — falling back to pure Python is fine for development
- Python 3.11.9 produces a security warning in ModuleUpdate.py — acceptable for local dev