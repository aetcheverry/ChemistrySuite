
# Chemistry Suite

A modular suite of chemical tools built with **PyQt6**, designed for chemists and researchers. This application provides calculators and reference tools for common laboratory tasks, all in a user-friendly graphical interface.

---

## 1) Features
Calculators:
- **Dilution Calculator**: 	Compute volumes for solution preparation.
- **DOSY NMR Calculator**: 	Estimate diffusion coefficients and viscosity corrections.
- **Elemental Analysis**: 	Compare calculated vs experimental elemental composition.
- **Isotopic Distribution**: 	Generate isotopic patterns for molecules.

Reference Data:
- **Solvent Properties**: 	Search and view physical properties of solvents.
- **Solvent Miscibility**: 	Interactive miscibility matrix with hover tooltips.
- **NMR Impurities**: 		Reference common solvent impurities in NMR spectra.

---

## 2) Folder Structure
```
ChemistrySuite/
├─ main.py
├─ widgets/           # UI components
├─ logic/             # shared helpers & calculations
├─ lib/               # static datasets
├─ resources/         # icons, home_page.html
└─ instructions/      # help pages (HTML)
```

---

## 3) Installation
Clone the repository and install dependencies:
```
bash
git clone https://github.com/aetcheverry/ChemistrySuite.git
cd ChemistrySuite
```

---

## 4) Usage
Run the application:
```
python main.py
```

---

## 5) Requirements

- Python 3.10+
- PyQt6
- PyQt6-WebEngine (optional for rich help pages)
- requests (for update checks)

---

## 6) License
This project is licensed under the MIT License - see the LICENSE file for details.

---

## 7) Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 8) Roadmap (future updates)

- BVS calculator  
- Diamagnetic corrections
- TLC stains
- Unit converter
- Graph plotter (quick XY plotter with import/export)
- Sketcher (2D molecule sketch)
- 3D visualiser (basic model rendering)
- Simple geometry optimiser
