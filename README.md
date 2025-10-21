# Quantum-Exploration
A record of my quantum research and eperimentation.

## Why this repo exists

A living record of my hands‑on exploration of quantum computing with an emphasis on security. It documents what I built, what I learned, and where I want to go. I publish notebooks, reproducible experiments, and short research notes.

## Repository structure
```
quantum-portfolio/
├── README.md
├── algorithms/              # Implementations + annotated notebooks
│   ├── simon/               # Simon’s algorithm
│   ├── grover/              # Grover search
│   ├── shor/                # Shor (toy + resource estimates)
│   └── primitives/          # QFT, phase estimation, oracles
├── security/                # Quantum crypto + quantum-safe work
│   ├── qkd/                 # BB84/BBM92 sims + attack notebooks
│   ├── pqc/                 # PQC benchmarks, hybrid TLS demo
│   └── ops-lab/             # “Quantum SOC” experiments
├── experiments/             # Noise models, error mitigation, VQE/QAOA
├── research/                # Notes, preprints, idea logs
├── notes/                   # Reading notes, summaries, glossaries
└── tools/                   # Reusable helpers, resource estimators
```

## Standards

* **Reproducibility:** Each project includes a `requirements.txt` or `environment.yml`, a `Makefile` or `invoke` tasks, and a fixed random seed where relevant.
* **Clarity:** Every notebook opens with a one‑screen executive summary and a single figure/table of the key result.
* **Testing:** Unit tests for classical helpers; circuit equivalence checks where feasible.
* **Licensing & credit:** MIT License for code, CC BY‑SA for text. Citations credited in each folder’s `REFERENCES.md`.
* **Data & hardware:** Simulators by default; if hardware is used, capture backend, queue time, calibration snapshot, and shot counts.

## Highlighted projects (keep this list curated)

* **Simon-fast:** Minimal‑gate Simon implementation with oracle generator; includes lower‑bit demos and complexity discussion.
* **Grover-visual:** Visual intuition with amplitude amplification plots; oracle construction patterns.
* **Shor‑lite:** Didactic Shor with explicit classical preprocessing and a resource‑estimation tool for RSA‑N. No hype, just numbers.
* **BB84‑lab:** End‑to‑end QKD simulation with eavesdropper models and error‑rate plots; reconciliation & privacy amplification demos.
* **Quantum‑SOC:** Scripts to monitor QRNG entropy, side‑channel toy models, and alerts for protocol anomalies.

## How to run

```bash
# clone
git clone https://github.com/sebsexton/quantum-exploration
cd quantum-portfolio

# pick an environment
pip install -r requirements.txt
# or
conda env create -f environment.yml && conda activate q

# run a demo
jupyter lab
# open algorithms/simon/simon.ipynb
```

## Roadmap (rolling)

* [ ] Implement and annotate Simon, Grover, and QFT primitives.
* [ ] Build `tools/resource_estimator.py` for Shor‑lite studies.
* [ ] QKD (BB84) with noise + attack models; plot QBER vs. eavesdropping.
* [ ] PQC benchmarks and a hybrid TLS demo; compare to classical baselines.
* [ ] ZX‑calculus or transpiler‑level optimisations on small circuits; report depth/2‑qubit gate reductions.

## Impact framing

* **What I built:** Short bullet list with links to executable notebooks.
* **What I learned:** One paragraph per project; be honest about dead‑ends.
* **Why it matters:** Security relevance and open research questions.

## Contact & updates

I post short write‑ups in `/research` and on my blog/LinkedIn. Feedback and collaboration welcome.

---

*This repository is intentionally educational. Any claims of improvement are scoped, tested on small instances, and caveated accordingly.*

