# 🎬 Film DCC Pipeline Template

A **standardized project structure** for **Film / 3D Animation production** using **DCC tools** (primarily **Autodesk Maya**).

This template is designed for:

* Short films
* Cinematic animation
* Animation reels
* Film-style pipelines (offline render)

It follows **studio-style pipeline thinking** while remaining **simple enough for solo artists**.

---

## 🎯 Goals

* Clear separation between **Assets** and **Shots**
* Scalable structure (small → large projects)
* Maya-friendly (reference-based workflow)
* Clean Git usage (no cache / render junk)
* Reusable as a long-term project template

---

## 🧩 Supported DCC Tools

* Autodesk **Maya** (2022+)
* Blender (compatible)
* Houdini (assets / FX)
* Substance Painter / Designer
* ZBrush (via export)

> ⚠️ This template is **NOT** for real-time engines (Unreal / Unity).

---

## 📁 Project Structure Overview

```
Film-Project/
│
├── 00_Docs/
│   ├── script/
│   ├── storyboard/
│   ├── animatic/
│   └── references/
│
├── 01_Assets/
│   ├── Characters/
│   ├── Props/
│   └── Environments/
│
├── 02_Shots/
│   ├── SH_001/
│   │   ├── layout/
│   │   ├── animation/
│   │   ├── lighting/
│   │   ├── render/
│   │   └── cache/
│   └── SH_002/
│
├── 03_Scenes/
│   ├── layout/
│   ├── animation/
│   ├── lighting/
│   └── render/
│
├── 04_Caches/
│   ├── alembic/
│   ├── ncache/
│   └── gpuCache/
│
├── 05_Renders/
│   ├── playblast/
│   ├── preview/
│   └── final/
│
├── 06_Compositing/
│   ├── nuke/
│   ├── aftereffects/
│   └── exports/
│
├── 07_Scripts/
│   ├── maya/
│   ├── python/
│   └── tools/
│
├── 08_Publish/
│   ├── assets/
│   └── shots/
│
├── .gitignore
├── .gitattributes
└── README.md
```

---

## 🧠 Pipeline Philosophy

### Asset-centric → Shot-centric

* **Assets** are built once and reused
* **Shots** reference assets (no duplication)
* Each shot represents a camera cut in the film

### Typical flow:

```
Model → Rig → Lookdev → Layout → Animation → Lighting → Render → Comp
```

---

## 🎥 Shot Naming Convention

```
SH_010_animation_v001.ma
SH_010_animation_v002.ma
SH_010_animation_final.ma
```

* `SH_###` : shot number
* `v###`   : version number
* `final`  : approved version only

---

## 🧱 Asset Structure Example

```
01_Assets/Characters/Hero/
├── model/
│   └── Hero_model_v003.ma
├── rig/
│   └── Hero_rig_v002.ma
├── textures/
└── lookdev/
```

Assets should be **referenced**, not duplicated into shots.

---

## 🧰 Git Workflow (Recommended)

Branches:

* `main` → stable / publish-ready
* `dev`  → daily work

Rules:

* Do NOT commit caches or renders
* Commit only clean `.ma`, scripts, and configs

---

## 🚫 What Not to Put in Git

* Render outputs (`.exr`, `.mov`)
* Simulation caches
* Autosave / temp files

(Handled via `.gitignore`)

---

## ✅ Who Is This Template For?

* Solo artists
* Film / Animation students
* Technical Artists
* Small animation teams

---

## 📌 License

Use freely for personal and commercial projects.
Modify as needed for your own pipeline.

---

## ✨ Notes

This template is meant to **grow with your skills**.
Feel free to extend it for:

* FX-heavy projects
* Multi-sequence films
* Studio-specific workflows

Happy animating 🎞️
