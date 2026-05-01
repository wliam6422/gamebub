# Yampad v3 CAD Rebuild and Validation

## Overview

This project recreates and validates the **Yampad v3 case** using Python CAD scripts.

Reference project:
[https://github.com/mattdibi/yampad](https://github.com/mattdibi/yampad)

Reference STEP file used:

```text
case/3D Print/yampad_v3-Fusion360.step
```

The reference STEP file contains **2 main parts**:

1. **Plate**
2. **Base**

The goal of this project is to rebuild both parts with Python code and validate the generated assembly against the original reference STEP model.

---

## Reference Model

The reference model comes from the open-source **Yampad** project by `mattdibi`.

Yampad is an open-source mechanical macropad/numpad project with a 3D-printable case, PCB, firmware, and assembly files.

For this CAD task, only the following file is used as the reference:

```text
yampad_v3-Fusion360.step
```

---

## Project Structure

Recommended folder structure:

```text
project/
│
├── reference/
│   └── yampad_v3-Fusion360.step
│
├── script/
│   ├── plate.py
│   ├── base.py
│   ├── assembly.py
│   └── validation.py
│
├── output/
│   ├── plate.step
│   ├── base.step
│   ├── assembly.step
│   └── assembly.stl
│
└── README.md
```

---

## Script Details

### 1. Plate Script

```text
script/plate.py
```

Creates the top plate part of the Yampad case.

Main purpose:

* Build the plate geometry
* Add switch cutouts
* Add required holes and edge details
* Export the generated plate model

---

### 2. Base Script

```text
script/base.py
```

Creates the bottom base part of the Yampad case.

Main purpose:

* Build the base body
* Add internal cavity / shell features
* Add screw holes and mounting details
* Export the generated base model

---

### 3. Assembly Script

```text
script/assembly.py
```

Combines the generated plate and base into one assembly.

Main purpose:

* Import or create both parts
* Align plate and base
* Create the final complete case assembly
* Export final STEP / STL output

---

### 4. Validation Script

```text
script/validation.py
```

Compares the generated assembly against the reference STEP file.

Main checks:

* Bounding box size comparison
* Center alignment comparison
* Volume comparison
* Volume-based symmetric difference comparison

---

## Validation Result

Latest validation result:

```text
--- Volume Comparison ---
Design volume     = 96777.811 mm³
Reference volume  = 96812.141 mm³
Volume difference = -34.330 mm³
Volume difference = -0.035 %

--- Symmetric Difference ---
Volume-based symmetric diff = 0.035 %
Symmetric diff (volume-based) = 0.035 %
  Design volume    = 96777.811 mm³
  Reference volume = 96812.141 mm³
  Difference       = -34.330 mm³

=== RESULT SUMMARY ===
Size check        : PASS ✅  (diff: 0.040 mm)
Center check      : PASS ✅  (diff: 0.000 mm)
Volume check      : PASS ✅  (diff: -0.035 %)
Symmetric diff    : PASS ✅  (diff: 0.035 %)
```

---

## Validation Summary

| Check                | Result | Difference |
| -------------------- | -----: | ---------: |
| Size check           | PASS ✅ |   0.040 mm |
| Center check         | PASS ✅ |   0.000 mm |
| Volume check         | PASS ✅ |   -0.035 % |
| Symmetric difference | PASS ✅ |    0.035 % |

The generated model is very close to the reference model.

The final volume difference is only:

```text
34.330 mm³
```

This is approximately:

```text
0.035 %
```

So the CAD rebuild can be considered successfully validated.

---

## Requirements

Install Python CAD dependencies:

```bash
pip install build123d ocp-vscode
```

Optional dependencies may be needed depending on your validation script:

```bash
pip install cadquery numpy
```

---

## How to Run

### 1. Generate Plate

```bash
python script/plate.py
```

### 2. Generate Base

```bash
python script/base.py
```

### 3. Generate Assembly

```bash
python script/assembly.py
```

### 4. Run Validation

```bash
python script/validation.py
```

---

## Expected Output

After running all scripts, the output folder should contain generated CAD files such as:

```text
plate.step
base.step
assembly.step
assembly.stl
```

---

## Notes

* The reference STEP file has two separate solids: plate and base.
* The Python project rebuilds both parts separately.
* The assembly script combines both generated parts.
* The validation script compares the final assembly with the original reference STEP file.
* Current validation passes size, center, volume, and symmetric difference checks.

---

## License

This project is based on CAD reference files from the open-source Yampad project.

Original Yampad repository:
[https://github.com/mattdibi/yampad](https://github.com/mattdibi/yampad)

Check the original repository license before redistribution or modification.
