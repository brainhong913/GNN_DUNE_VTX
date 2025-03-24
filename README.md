# GNN_DUNE_VTX

Documentation on how to generate training samples and apply a Graph Neural Network (GNN) for vertex reconstruction (vtx reco) in DUNE.  
All source code is provided and tested with **LArSoft v10_04_06**.

---

## 🧰 Local Setup

Before starting, please read the official LArSoft setup guide:  
🔗 https://larsoft.org/to-set-up-and-run-larsoft/

You will need to set up:
- `duneana`
- `larpandoracontent`

After setup, you should see a `srcs/` directory.

To use this package:
- Replace your local `srcs/` with the one from this repository.

---

## 🛠 Example Commands

### 📌 Generate `.data` graph files
```bash
lar -c atm-training-extract.fcl -s detsim.root
```

### 📌 Generate subrun-event ID table
```bash
lar -c eid.fcl -s detsim.root
```

### 📌 Generate `truth_eid` ROOT file
(Describe your usage here if applicable.)

---

## ☁️ Submit Jobs (Batch/Grid)

Please refer to the job submission instructions here:  
🔗 https://gitlab.in2p3.fr/pgranger/atmo_gen

You will likely need:
- `larsoft_graph_V1_2025.tar.gz`
- A corresponding YAML config file

Typical jobs:
- `Reco`: Generate `.data` graph files for U, V, W views
- `SubrunList`: Generate a ROOT file to correct subrun/event ID mismatches
- `AnaTree`: Generate anatree output (optionally merge with `hadd`)

---

## 📦 Outputs Produced

1. `.data` — raw graph input files  
2. `eid.root` — aligns event IDs with anatree files  
3. `anatree.root` — merge multiple files into one `merged.root` if needed

---

## 🐍 Python Access

If you prefer not to regenerate data, you can find pre-generated samples here:
```
/exp/dune/app/users/ichong/3views_graph_data
```

---

## 📓 Python Notebooks

For Python notebooks and tools, visit the companion repo:  
🔗 https://github.com/brainhong913/GNN_DUNE_VTX_Python

