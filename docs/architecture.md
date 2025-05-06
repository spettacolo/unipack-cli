# Architettura del Progetto

Questo documento descrive i principali componenti di **unipack-cli**:

1. **CLI (`cli.py`)**
   Usa Typer per definire i comandi utente (`list`, `search`, `install`, ecc.).

2. **Core (`core/`)**
   - `base.py`: struttura dati `PackageInfo`, gestione cache SQLite/json.
   - `python.py`, `npm.py`, `crates.py`, …: moduli per interrogare API PyPI, npm, crates.io.

3. **TUI (`tui/`)**
   - `layout.py`: definizione pannelli (left/right/status).
   - `widgets.py`: widget personalizzati (lista, preview Markdown).
   - `events.py`: mappatura tasti e callback.

4. **Test (`tests/`)**
   Suite pytest per unit e integration test, con mock delle API.

5. **CI/CD (`.github/workflows/ci.yml`)**
   Pipeline per linting, test e validazione.
