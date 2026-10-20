# Color Fusion
### Early Experiments in FDM Color Mixing

I'm experimenting with a way to create colorful FDM prints using ordinary PLA filaments stacked in thin layers.

It's still a work in progress. Some colors look surprisingly good, while others are noticeably off.

I wanted to share a few real prints and show how the project is evolving.

📄 **[View or Download the 3-Page Early Preview PDF](Color_Fusion_Early_Preview.pdf)**

---

## 1. Digital Artwork vs. Latest Real Print

Here is a recent 180 mm × 180 mm test print fresh off the print bed:

| Original Digital Artwork (2D Source) | Actual 3D Print (Bambu P1S + 2 AMS) |
| :---: | :---: |
| ![Original Artwork](images/original-artwork.png) | ![Latest Real Print](images/latest-real-print.png) |

### Print Details
- **Printer:** Bambu Lab P1S with 2 × AMS (8 filament slots)
- **Print Time:** **4.5 hours**
- **Layer Height:** 0.08 mm (0.4 mm standard nozzle, 100% solid infill)
- **Dimensions:** 180 mm × 180 mm × 2.0 mm
- **Filaments Used (8 Ordinary PLAs):**
  1. `eSun PLA+ Pink` (Base plate & outer frame)
  2. `Jadeway PLA Matte Yellow`
  3. `Bambu PLA Basic Mistletoe Green`
  4. `Bambu PLA Lite Matte Beige`
  5. `eSun ePLA+HS Red`
  6. `Bambu PLA Basic Blue Gray`
  7. `Jadeway PLA Yellow`
  8. `Bambu PLA Basic Jade White`

---

## 2. Evolution: Early Prototype vs. Latest Experiment

Getting plastic layers to blend naturally took a lot of trial, error, and algorithm tuning. It definitely didn't happen overnight!

| Early Prototype (Oct 15) — Stepped & Blocky | Latest Experiment (Oct 20) — Smooth 8-Color |
| :---: | :---: |
| ![Early Prototype](images/early-prototype.png) | ![Latest Experiment](images/latest-real-print.png) |

- **Oct 15 Prototype:** Noticeable stepped banding across the sky, harsh pixel contours, and oversaturated cyan-green water.
- **Oct 20 Experiment:** Continuous sunset sky gradient, subtle slate-blue aquatic reflections, and crisp architectural rooflines printed in 4.5 hours.

---

## 3. How Does It Work?

You don't need to manually paint pixels or guess layer heights. The workflow is designed to be automated:

1. **Pick Normal PLA:** Grab any regular PLA spools from your shelves (Bambu Lab, eSun, Jadeway, etc.).
2. **Scan a SpoolCard:** Print a small 50×50 mm card to measure how translucent the plastic is at 10 different layer depths.
3. **Auto-Compute Recipes:** Color Fusion searches through layer-stacking combinations to recreate the target image's hues.
4. **Export 3MF & Print:** Load the standard multi-material 3MF file directly into Bambu Studio or OrcaSlicer and print.

---

## 4. SpoolCards & The 1,024-Color Benchmark

To predict how colors will look before melting plastic, Color Fusion uses physical calibration swatches and combinatorial tests:

### Growing Spool Library (SpoolCard v3.1 — 50 × 50 mm)
Each card tests stepped transmission depths from 0.08 mm to 2.0 mm over black and white backings:

![Spool Cards Banner](images/spool-cards.png)
*(From left to right: Bambu Green, Mistletoe Green, Blue Gray, eSun Red, Sunflower Yellow, Cocoa Brown)*

### Combinatorial Validation Grid & Studio Prototype
| 1,024 Blended Colors Test Grid (32 × 32) | Color Fusion Studio Workbench Prototype |
| :---: | :---: |
| ![1024 Color Benchmark](images/color-benchmark.png) | ![Studio Workbench](images/studio-workbench.png) |

- **1,024 Test Grid:** A physical 32×32 swatch array printed in 4 standard spools to verify how multi-layer blends behave across the full spectrum.
- **Studio Workbench:** A prototype web tool where I assign AMS slots, inspect sub-layer recipes, and export multi-color 3MFs.

---

## 5. Current Challenges & Things Still Being Tuned

This is an active, honest experiment. Here are a few things I'm still figuring out:

- **Shadow Tones:** Stacking multiple rich pigments tends to absorb slightly more light than simulated, making deep water and shaded hills print a bit darker than expected.
- **Nozzle Purge Volumes:** Extruder flushing is critical. If the nozzle doesn't fully purge rich red or magenta before extruding white, you get an unintended pinkish tint!
- **Filament Brand Variations:** Every brand's "Yellow" or "Cyan" has unique pigment density and opacity, which is why scanning quick SpoolCards is essential.

---

## 6. Community Feedback & Next Steps

I'm actively refining the algorithm and would love to hear from other 3D printing enthusiasts:

- What do you think of this approach to FDM color blending?
- **I'm considering sharing some test 3MF files down the road** if community members with AMS or multi-material setups are interested in test-printing on their own machines!
- What image styles, palettes, or filament brands would you be most excited to see tested next?

Feel free to open an Issue or Discussion on this repository to share your thoughts, ideas, or questions!

---

> **Note**: This repository currently contains project previews and experimental results, not the Color Fusion Engine source code. Source-code and commercial licensing plans have not yet been finalized.
