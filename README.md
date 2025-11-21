# DIYRaman – Open Hardware Raman Spectrometer 

An open, modular Raman spectrometer you can build, understand, and modify –  with documentation aimed at hobbyists, educators, and low-resource labs.

![Full Assembly in Overpressure Glove Box without Cuvette](assets/images_pictures/Overview-Video-Pic_1_1400px_JPG.jpg)

The goal is to make Raman spectroscopy **replicable, affordable, and well-documented**, so that motivated builders – including those without access to expensive equipment – can build a working system for:

- broad substance and drug identification *(qualitative, exploratory)*,
- basic materials identification,
- teaching optics and spectroscopy.


 Built from cost-efficient parts and repurposed components:
 
- a surplus spectrometer module [(B&W Tek - eBay](https://www.ebay.com/itm/143989529085)),
- a cheap 532nm laser pointer,
- 3D-printed parts,
- various used components.


For performance and reproducibility, essential optics had to be purchased new from Thorlabs and Edmund Optics – the most costly portion of this build:

- Dichroic Mirror (DMLP550 - Thorlabs, 230$)
- Longpass Filter (FELH0550 - Thorlabs, 170$)
- (Optional) Bandpass Filter (#65640 - Edmund Optics, 95$)

A detailed overview of all the used parts and cost can be found under `/bom/BOM (Bill of Materials).md`


This repository contains:

- **Build documentation** (step-by-step with images),
- **Hardware design files** (3D models and Fusion CAD files),
- **Software** for acquisition and visualisation,
- **BOMs** with parts, essential properties and alternatives.

> 💡 This README is a *project overview*. Detailed build instructions can be found in `docs/` and the dedicated pages (Basic Assembly, Glove Box, Linear Stage, Full Assembly, …).


---

## Who is this for?

![](assets/images_pictures/Video-Pic_Setup_4_1400px_JPG.jpg)

DIYRaman is designed for:

- 🛠️ **Makers & hobbyists** with a 3D printer and basic electronics skills  
- 📚 **Teachers & students** who want a hands-on, explainable spectrometer  
- 🌍 **Low-resource labs** where commercial Raman devices are inaccessible  
- 💊 **Curious experimenters** exploring qualitative screening and comparison


You should be comfortable with:

- basic hand tools,
- 3d-printing,
- following technical step-by-step instructions,
- handling lasers safely - or receive guidance from someone.

> ⚠️ **Not a certified analytical instrument**  
> DIYRaman is a learning and research tool. It is **not validated** for clinical, regulatory, or forensic decisions and only yields broad qualitative results.

---

## What can it do?

The completed Raman build offers:

- **Stokes region** above ~600 cm⁻¹  
- solids / liquids in a cuvette-type sample holder  
- qualitative & educational use (comparison, teaching, demos)  
- extensible design (alternative spectrometers, lasers, mechanics)


> 🧪 **Drug / counterfeit screening**  
> The system can be used for *exploratory, educational* screening of unknowns (e.g. counterfeit pills) but **must not** be treated as a validated forensic tool. **Always cross-check with certified methods!**

---

## Project status

> **Early open release — Work in progress**

Hardware and docs are under active development. Conventions, part numbers, files, and instructions may change.

Current module status:

- ✅ **Basic Raman Optical Assembly** – documented and buildable  
- ✅ **Overpressure Glove Box** – documented and buildable  
- 🟡 **Linear Translation Stage** – documented, design still being adjusted  
- 🟡 **Spectrometer Unit** – usable, documentation in progress  
- 🟠 **Full Raman Optical Assembly** – documentation in progress  
- 🔴 **First Acquisition & Software / GUI** – unpublished  

Breaking changes may occur; expect adjustments until the first tagged release.

---

## Repository structure (WiP – early draft)

```text
assets/
  images_animated/
  images_infographic/
  images_picked/
  images_pictures/
  images_print-orientation/

bom/
  BOM.csv                 # Incomplete; updated in respective instruction!
  
docs/
  instructions/           # Step-by-step build docs

parts/                    # .STL-files for 3D-printing
  basic-assembly/
  glovebox/

results/                  # Captured example spectra

software/                 # Planned



LICENSES/
  CERN_OHL_S_V2.txt
  CC-BY-SA-4.0.txt
  MIT.txt
```

 
- Build *instructions* in `docs/instructions/`.  
- Hardware *source files* in `parts/`.
- All *images* and supporting graphics in `assets/`.
- Complete BOM in `bom/` and respective instruction.  
- License texts in `LICENSES/`.

---

## Build path (recommended)

A suggested build order for new users:

1. **Spectrometer Setup**  
   – Become comfortable with the operation of the spectrometer unit .  
2. **Overpressure Glove Box**  
   – Keep dust away from optics and make laser alignment safer.  
3. **Basic Raman Optical Assembly**  
   – Align the basic backscattering optical path.  
   - *Acquire your first rough spectrum.*  
3. **Linear Translation Stage**  
   – Add fine focus control for the focusing optics.  
4. **Full Raman Optical Assembly**  
   – Add motorisation, translation stage, and refinements.  
   - *Acquire your first usable Raman spectrum.*  
5. **Calibration** *(planned)*  
   – Calibrate wavelength axis and intensity where feasible.  
6. **Upgrade options** *(planned)*  
   – Alternative optics, higher-quality mechanics, software features.


![](../../assets/images_pictures/Overview-Video-Pic_3_1400px_JPG.jpg)

---

## Contributing

Contributions are very welcome – especially from people building the system.

You can help by:

- reporting unclear or missing steps in the docs,  
- proposing improved or more accessible part choices,  
- designing mechanical variants (e.g. alternative mounts, stages),  
- improving the GUI / firmware,  
- sharing example spectra and calibration tips.

---

## Teaching & research use

If you use DIYRaman in teaching, workshops, or research:

- Consider contributing your **findings, documentation, worksheets, or demos** back to the project.  
- If you publish work based on DIYRaman, please cite it so others can find it.

Until the first proper release is published, you can use the following citation: 

> **DIYRaman - Open Hardware Raman Spectrometer (Github),**   
> *Jacob Busshart, DIYraman.com*


---

## Acknowledgements

This project builds on the shared knowledge and contributions of the open-hardware community. Some particularly helpful references and inspirations:

- [OpenRaman.org](https://www.open-raman.org/) & [ThePulsar.be](https://www.thepulsar.be/article/diy-raman-spectroscopy/) (Luc)  
- [PhysicsOpenLab.org – Backscattering Raman system](https://physicsopenlab.org/2022/04/22/backscattering-raman-system/)  
- [Laserpointerforums.com – B&W Tek spectrometer thread](https://laserpointerforums.com/threads/b-w-tech-spectrometer-473-module-setup-mods-info.101467/)

If you adapt or extend this design, please consider releasing your variant as open hardware too – especially if it makes the system easier to build in your local context.


---

## Licensing – open hardware setup

DIYRaman separates licenses for **hardware**, **documentation**, and **software**.  
This follows common open-hardware practice and simplifies reuse.


**Hardware**: 
All **hardware design files** in this repository (mechanical CAD, STLs, STEP files, electronics schematics and layouts) are licensed under:
**CERN-OHL-S v2**
`LICENSES/CERN_OHL_S_V2.txt` 

**Documentation**: 
All **build instructions, diagrams, and written documentation** in this repository are licensed under: 
**Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**
`LICENSES/CC-BY-SA-4.0.txt`

**Software**: 
All **software** in this repository (code and firmware) is licensed under:
**MIT License**
`LICENSES/MIT.txt`


---

*NOTE: Some parts of the written documentation has been formatted or translated using AI.*

![](../../assets/images_pictures/Video-Pic_Setup_3_1400px_JPG.jpg)
