# 🎮 Game Bub – Parametric CAD Recreation (build123d)





---
## 📌 Overview

This project focuses on recreating key mechanical parts of the **Game Bub handheld** using **Python and the build123d CAD library**.

The goal is to:

- Study and reference original STL designs
- Rebuild them as **parametric CAD models**
- Enable easy modification, scaling, and customization
- Export both **STL and STEP files** for manufacturing
- View and inspect CAD models directly in VS Code using **ocp_vscode**

---

## 🎯 Project Objective

- Use original STL files as reference geometry
- Recreate each component using clean script-based CAD
- Maintain dimensional accuracy
- Improve flexibility through parametric design
- Generate both complete button arrays and separate single-button models

---

## 👁️ CAD Visualization

We integrated **OCP Viewer / ocp_vscode** with **VS Code** to preview and inspect the CAD models during development.

This helped us:

- View generated build123d models directly inside VS Code
- Check shape accuracy
- Verify fillets, cuts, curves, and button placement
- Compare generated parts with the original reference STL files

---

## 🔘 Button Reconstruction Workflow

In the original reference STL files, the following button files contained multiple buttons attached together:

- ShoulderButtonArray.stl
- FaceButtonArray.stl
- SideButtonArray.stl
- ExtButtonArray.stl

First, we recreated these button arrays same as the reference models.

After that, we separated them into individual single-button designs and created separate Python scripts for each single button.

This makes the design easier to edit, test, print, and reuse.

---







# 📂 Project Structure
## 📂 Reference Parts
├── Reference parts/
│ ├── Rear.stl
│ ├── Front.stl
│ ├── DpadButton.stl
│ ├── ExtButtonArray.stl
│ ├── FaceButtonArray.stl
│ ├── SideButtonArray.stl
│ └── ShoulderButtonArray.stl
## 📂 Generated parts
├── Generated parts/
│ ├── (Generated STL + STEP files)



## 📂 Scripts
├── scripts/
│ ├── front.py
│ ├── rear.py
│ ├── dpad.py
│ ├── shoulderbutton.py
│ ├── shoulder_button_left.py
│ ├── shoulder_button_right.py
│ ├── facebutton.py
│ ├── facebutton_single.py
│ ├── extbutton.py
│ ├── extbutton_single.py
│ ├── sidebutton.py
│ ├── sidebutton_single.py
│ ├── assembly.py
│ └── validation.py





---



## 🧱 Reference Files



The following STL files are used as reference models:



- Rear.stl  
- Front.stl  
- DpadButton.stl  
- ExtButtonArray.stl  
- FaceButtonArray.stl  
- SideButtonArray.stl  
- ShoulderButtonArray.stl  



All reference files are stored in the **Reference parts/** folder.



---



## ⚙️ Generated Output



All recreated models are exported to:



- **STL format** (for 3D printing)  
- **STEP format** (for CAD compatibility)  



Saved inside the **Generated parts/** folder.



---



## 🧠 Tools & Technologies



- Python  
- build123d (parametric CAD modeling)  
- ocp_vscode (optional visualization)  



---



## ▶️ Usage



1. Install dependencies:



bash
pip install build123d
