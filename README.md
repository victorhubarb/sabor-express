# Sabor Express 🍽️

![Status](https://img.shields.io/badge/status-completed-green?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3-blue?style=for-the-badge&logo=python)

A terminal-based restaurant management system built in Python — my first Python project, focused on core language fundamentals, clean function design, and a polished terminal UI.

---

## Overview

Sabor Express simulates the backend of a food delivery platform. Restaurants can be registered, listed, and toggled between active and inactive states — all through a menu-driven terminal interface. The project was built to get comfortable with Python's core features: dictionaries, lists, functions with docstrings, f-strings, and exception handling. The terminal is cleared between screens using `os.system('clear')` for a cleaner user experience.

---

## Architecture

```
sabor-express/
└── app.py              # Entire application — data, business logic, and UI in one file
```

### Key Python Concepts Applied

| Concept | How it shows up |
|---|---|
| **Dictionaries** | Each restaurant is a `dict` with `nome`, `categoria`, and `ativo` keys |
| **List of dicts** | `restaurantes` is a global list of dicts — the app's main data structure |
| **Functions with docstrings** | `cadastrar_novo_restaurante()` has a full docstring documenting inputs and outputs |
| **f-strings** | Used throughout for dynamic output — including `ljust()` for aligned table columns |
| **Toggle with `not`** | `restaurante['ativo'] = not restaurante['ativo']` — flips the status in one line |
| **try/except** | `escolher_opcao()` wraps input parsing in try/except to handle non-integer input gracefully |
| **os.system('clear')** | Terminal is cleared between screens via `exibir_subtitulo()` for a cleaner UX |
| **`if __name__ == '__main__'`** | Standard Python entry point pattern |
| **Modular design** | Each feature is its own function — `cadastrar_novo_restaurante()`, `listar_restaurantes()`, `alternar_estado_restaurante()` |

---

## Features

- **Register Restaurant** — add a new restaurant with name and category; starts as inactive
- **List Restaurants** — displays all restaurants in a formatted table with name, category, and status
- **Toggle Status** — activate or deactivate a restaurant by name
- **Exit** — closes the application cleanly

---

## How to Run

**Prerequisites:** Python 3 installed

```bash
git clone https://github.com/victorhubarb/sabor-express.git
cd sabor-express

python app.py
```

---

## Author

**Victor Hugo Barbosa**
[GitHub](https://github.com/victorhubarb) · [LinkedIn](https://www.linkedin.com/in/victorhbarbosa/)
