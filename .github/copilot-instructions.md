# Copilot Instructions for tp2-py

## Project Overview
This repository is a Python-based workspace focused on analyzing banking transactions for fraud prevention. The main logic is implemented in Jupyter notebooks, with a custom Python virtual environment located in `ambiente/`.

## Key Files & Structure
- `main.ipynb`: Central notebook for exercises and analysis. All main logic and outputs are here.
- `ambiente/`: Contains the Python virtual environment. Use the Python executable in `ambiente/Scripts/python.exe` for all commands.

## Developer Workflow
- **Environment Activation**: Always activate the virtual environment before running code or installing packages:
  - PowerShell: `./ambiente/Scripts/Activate.ps1`
- **Notebook Execution**: Edit and run cells in `main.ipynb`. All exercises and analysis should be performed here.
- **Package Management**: Use `pip` from the virtual environment (`ambiente/Scripts/pip.exe`) to install packages. Avoid installing globally.

## Coding Patterns & Conventions
- Variables and logic should be written in Portuguese, matching the exercise requirements (e.g., `tipo_transacao`, `valor_transacao`).
- Follow the exercise instructions in markdown cells for business logic and output requirements.
- Use clear, concise code in notebook cells. Avoid unnecessary complexity.
- Output messages must match exactly as specified in the exercise markdown.

## Integration Points
- No external APIs or services are integrated. All logic is self-contained in the notebook.
- Dependencies are managed locally in `ambiente/Lib/site-packages/`.

## Example: Transaction Analysis Pattern
```python
ANO_2_DIGITOS = 25  # Example: last two digits of birth year
TIPO_TRANSACAO = "transferência"
VALOR_TRANSACAO = 30000.00

if VALOR_TRANSACAO > 1000 * ANO_2_DIGITOS and TIPO_TRANSACAO == "transferência":
    print("Alerta: verificar origem da transferência")
elif TIPO_TRANSACAO == "saque":
    print("Alerta: confirmar com o cliente")
else:
    print("Transação normal")
```

## Troubleshooting
- If a package is missing, install it using the environment's pip.
- If the kernel is not detected, ensure the environment is activated and restart VS Code.

---

For questions or unclear conventions, review the markdown instructions in `main.ipynb` or ask for clarification.
