# Sabor Express

A terminal app in Python for managing a list of restaurants: register one, list them, and switch each between active and inactive. It was my first Python project.

The menu, prompts and messages are in Portuguese.

## What it does

```
1. Cadastrar restaurante            register: name and category, starts inactive
2. Listar restaurante               table with name, category and status
3. Alternar estado do restaurante   look one up by name and flip active/inactive
4. Sair                             exit
```

The list starts with three sample restaurants. Data lives in memory, so it resets every time the program closes.

Everything is in `app.py`. Each restaurant is a dict (`nome`, `categoria`, `ativo`) in one list, and every menu action is its own function. The code uses f-strings with `ljust()` for the table columns, a docstring on the register function, and `not` to flip the status.

## Run it

Requires Python 3.12 or newer (the f-strings reuse the same quote type inside the expression, which older versions reject). The screen clearing uses `clear`, so it works on macOS and Linux. On Windows, change it to `cls`.

```bash
git clone https://github.com/victorhubarb/sabor-express.git
cd sabor-express
python3 app.py
```

## Known gaps

- Nothing is saved to disk.
- The menu calls `main()` again after every action, so a long session keeps stacking calls. A `while` loop would be cleaner.
- `escolher_opcao()` uses a bare `except`, which hides any error, not only bad input.
- Duplicate names are allowed, and the toggle matches names exactly (case-sensitive).

---

Victor Hugo Barbosa · [GitHub](https://github.com/victorhubarb) · [LinkedIn](https://www.linkedin.com/in/victorhbarbosa/)
