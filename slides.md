---
marp: true
theme: gaia
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# From Prototype to Reproducible & Maintainable Medical AI

Thomas Boulier (MD, PhD) – Grenoble University Hospital, France

---

## Context: Why This Matters

- AI adoption in hospitals remains limited.
- Many ML models stop at the prototype stage.
- Key blockers:
  - Poor reproducibility
  - Fragile dependencies and workflows
  - Hard-to-maintain research code
- Scientific standards now require:
  - Published data, models, and code
  - One-command environment setup
  - End-to-end reproducibility (Heil et al., Nat Methods 2021)

---

## Reproducibility Starts at the Prototype Stage

- Code quality degrades over time.
- Prototyping practices influence:
  - research reproducibility
  - clinical deployability
  - startup viability
- Goal: simple habits that scale with time and teams.

---

## Objective of This Capsule

**Give 6 practical keys to move from exploratory code  
to reproducible, maintainable ML projects in healthcare.**

Not perfection — just realistic, impactful steps.

---

## A Simple Running Example

- The *"HelloWorld Deep Learning"* notebook  
- Well-written, clear, and fully reproducible  
- We use it only to illustrate:
  - modularisation
  - configuration
  - testing
  - maintainability

---

# The 6 Fundamental Building Blocks

---

## 1. Version Control

- Git for code history and collaboration  
- DVC (or equivalent) for large datasets  
- CI to automate tests and checks  
- **Aim:** stability and traceability

---

## 2. Environment Management

- Package managers (uv, pip, conda — any is fine)  
- Pin dependencies  
- Optional: containerisation (Docker)  
- **Aim:** rerun the project reliably in 6 months

---

## 3. Configuration

- Separate code and parameters  
- Use YAML / TOML / JSON  
- No hard-coded paths or hyperparameters  
- **Aim:** reproducibility + flexibility

---

## 4. Testing

- Unit tests (small functions)  
- Integration (small pipeline)  
- End-to-end (full script)  
- Automate with CI  
- **Aim:** confidence when changing code

---

## 5. Logging

- Structured logs instead of print()  
- INFO / DEBUG / ERROR levels  
- Helps debugging and auditing  
- **Aim:** understand what happened, and why

---

## 6. Modular Code

- Small, focused Python modules  
- Clear separation of responsibilities  
- Inspired by Clean Code & design patterns  
- **Aim:** readability, maintainability, reusability

---

## Demo (Optional)

```python
python main_script.py
```

A minimal example of a reproducible and maintainable workflow.

---

# Conclusion

- Reproducibility and maintainability are crucial  
  for research, clinical translation, and startups.
- This is a long-term learning process.  
- Perfection is unrealistic — **but these 6 blocks  
  already make a major difference.**

---

## References (Optional)

- Khuyen Tran — *Production-Ready Data Science*  
- Heil et al., *Reproducibility standards*, Nat Methods 2021  
- Varoquaux et al., *Reproducibility in ML for Health*, Nat Med 2022  
- Clean Code / Refactoring Guru  
