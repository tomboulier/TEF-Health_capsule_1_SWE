---
marp: true
theme: default
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# From Prototype to Reproducible & Maintainable Scientific Code in Healthcare

Thomas Boulier (MD, PhD) – Grenoble University Hospital, France

---

## Context: Why This Matters


- AI in healthcare struggles to move beyond prototypes  
  ([Varoquaux *et al.*, Nat Med 2022](https://www.nature.com/articles/s41746-022-00592-y))
  
- Early-stage ML code often lacks reproducibility  
  ([Matthew B. A. McDermott *et al.*, Sci Transl Med 2021](https://www.science.org/doi/10.1126/scitranslmed.abb1655))  
- Typical blockers: unavailable data, unstable dependencies, unclear workflows,  
  hard-to-reproduce or hard-to-maintain code

**Goal of this capsule:**  
Practical steps toward reproducible and maintainable ML projects.

---

## A Simple Running Example

We start from the **“Hello World Deep Learning in Medical Imaging”** tutorial:   ([Lakhani *et al.*, J Digit Imaging 2018](https://link.springer.com/article/10.1007/s10278-018-0079-6))

- X-ray classification using transfer learning (InceptionV3)
- Well-written code, and *fully reproducible*  
- Shared as a Jupyter notebook with open data and source code:  
  https://github.com/paras42/Hello_World_Deep_Learning

We use it as a **running example** not to improve the model,  
but to show how a working prototype can evolve into code that is modular, testable, and easy to maintain as a team.



---

# The 6 Fundamental Building Blocks

1. Version Control  
2. Environment Management  
3. Configuration  
4. Testing  
5. Logging  
6. Modular Code

---

## 1. Use a Version Control System (VCS)

**Definition:** a system to track changes, restore previous states, and collaborate efficiently   ([Git documentation](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control))

- Git is the standard for code versioning  
- Git is not suited for large binaries or datasets  
  → tools like [DVC](https://dvc.org) or [Git LFS](https://git-lfs.com) handle data/models  

**Ressources:** [Pro Git Book](https://git-scm.com/book/en/v2), [The Version Control Book](https://lennartwittkuhn.com/version-control-book/), [Version Control with Git - a software carpentry lesson](https://swcarpentry.github.io/git-novice/)


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
