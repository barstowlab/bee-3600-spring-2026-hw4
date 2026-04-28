# CBB-Butanol Pathway Analysis

Metabolic flux balance analysis for 1-butanol production from CO₂ using the Calvin-Benson-Bassham (CBB) cycle combined with butanol biosynthesis pathways.

## 📋 Overview

This project performs **stoichiometric flux balance analysis** to determine the resource requirements for producing 1-butanol from CO₂. The pathway combines:

- **Calvin-Benson-Bassham (CBB) cycle** - CO₂ fixation into sugars
- **Glycolysis** - Sugar breakdown  
- **Butanol biosynthesis pathway** - Acetyl-CoA to 1-butanol conversion

### Key Results

To produce **1 unit of butanol**, the engineered pathway requires:
- ⚡ **14 ATP** (energy input)
- 🔋 **12 NADH** (reducing power)
- 🌱 **4 CO₂** (carbon source - net consumption)

## 📦 Requirements

```bash
numpy
scipy
matplotlib
```

## 🗂️ Project Structure

```
CBB-butanol/
├── utils/
│   ├── __init__.py          # Package initialization
│   ├── balanceUtils.py      # Core flux balance analysis
│   ├── specutils12.py       # Utility functions
│   └── vectorOutput4.py     # Data export utilities
└── CBB-butanol-master.ipynb # Main analysis notebook
```

## 🔬 Methodology

The analysis uses:
1. **Stoichiometric matrix** representation of 23 biochemical reactions
2. **Flux balance optimization** to solve for steady-state metabolite concentrations
3. **Resource calculation** per unit of target product (butanol)

## 📊 Key Functions

### `balanceUtils.py`
- `SolveFluxBalanceEquation()` - Solves metabolic flux balance
- `ConvertIndexedSMatrix()` - Processes stoichiometric matrices
- `GetResourcesVector()` - Calculates resource requirements

## 🎓 Applications

This type of analysis is essential for:
- Synthetic biology pathway design
- Metabolic engineering optimization
- Biofuel production feasibility studies
- Understanding resource constraints in biosynthesis
