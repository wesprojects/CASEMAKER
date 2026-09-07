# CASEMAKER

Parametric case goods designer that turns a cabinet model into shop-ready CNC programs, nested DXF sheets, 3D models, and assembly manuals.

---

## Usage

Launch the app at **[wesprojects.github.io/CASEMAKER](https://wesprojects.github.io/CASEMAKER)**.

1. Pick a sample product from the dropdown, or set the case dimensions and add parts.
2. Add shelves, dividers, doors, and drawer stacks; hardware and hole patterns update as you work.
3. Use the left rail — PLAN, PANELS, NEST, DRILL, 3D, ASSY — to review the model and export.

Runs in a current desktop browser; Chrome is recommended. Projects save and load as portable files.

## Overview

CASEMAKER designs case goods and produces the manufacturing output for them. A case is defined by its dimensions, structure, and contents — shelves, dividers, doors, drawer stacks — and the application derives everything downstream: hole patterns, hardware placement, machine programs, and documentation.

Every output is generated from one model, so panel drawings, CNC programs, nested sheets, 3D exports, and the assembly manual cannot disagree with each other.

## Features

**Parametric case design**
Width, height, depth, stock and back thickness, kick height and inset, top overhang. Add shelves, dividers, doors, and drawer stacks; parts and hardware recalculate on every change. Seven production presets ship with the app (bookcase, storage cabinet, lateral file, box/box/file, hutch, and more).

**Automatic hardware and joinery**
Cam nuts, cam pins, dowels, shelf pegs, floor glides, concealed hinges, pull handles, lock cylinders, and drawer slides are placed by rule from the case geometry — including construction standards such as concealed hinge cups seating in the door's 35 mm pocket and lock bores registered to the pull-hole centerline. Hardware appears in the model, the drawings, the bill of materials, and the 3D export.

**Panel drawings**
Per-panel views showing every bore, groove, and notch at finished size, drawn as the face sits up on the machine. Color-coded by hole type with a cut list per panel.

**CNC output**
Complete drilling programs for CNC #1 (Hendrick HSR, OSAI 10 control). Includes an on-screen toolpath simulator with run/pause, single-step, variable speed, scrubbing, and a live DRO reading move number, drill count, plane, and X/Y/Z position — driven by the same waypoints written to the `.nc` file.

**Nested DXF sheets**
Sheet layouts per stock type. One DXF per sheet, R12, inch units. Outlines, grooves, text, and each bore diameter on separate named layers at finished size.

**3D export**
COLLADA (`.dae`), OBJ, and binary STL output in inches or millimetres, with or without hardware. Hardware exports as its true modeled geometry — watertight, no stray edges — so imports into SketchUp and other CAD tools are clean.

| Format | Structure | Use |
| --- | --- | --- |
| `.dae` | One named component per part, placed by node transform | SketchUp, CAD assembly work |
| `.obj` | One named object per part | General 3D tools, rendering |
| `.stl` | Single flattened solid, binary | Slicers, mesh tools, 3D printing, viewers |

All three carry the same geometry: every bore, groove, and notch subtracted at finished size. STL is written from the audited COLLADA scene, then flattened to world coordinates with degenerate facets removed and unit-length facet normals, so the file loads cleanly in slicers and mesh tools. Exports are blocked if the geometry audit fails, so a malformed file is never written.

**Assembly manual**
Printable manual generated from the drilled holes: hardware table, parts list, and one figure per assembly step.

**Cut sheets and BOM**
Operator cut sheets as PDF, and a bill of materials counting every panel, part, and piece of hardware in the case.

**Project files**
Save and load complete jobs — geometry, contents, hardware selections, and settings — as portable project files.
