"# 🎮 Game Bub – Parametric CAD Recreation (build123d)





---



## 📌 Overview



This project focuses on recreating key mechanical parts of the **Game Bub handheld** using **Python and the build123d CAD library**.



The goal is to:
- Study and reference original STL designs  
- Rebuild them as **parametric CAD models**  
- Enable easy modification, scaling, and customization  
- Export both **STL and STEP files** for manufacturing  



---



## 🎯 Project Objective



- Use original STL files as reference geometry  
- Recreate each component using **clean, script-based CAD**  
- Maintain dimensional accuracy  
- Improve flexibility through parametric design  



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
pip install build123d"
