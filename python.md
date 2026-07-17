# Python

## 1. Create virtual env and activate
```bash
python -m venv .venv
source .venv/bin/activate
```

---

## 2. Installing the requirements
```bash
pip install -r requirements.txt
```

---

## 3. Putting new dependencies in the requirements files (while activated)

```bas
source .venv\Scripts\activate
pip freeze > requirements.txt
```
