# Linear Translation Stage

![Linear translation stage – assembled](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%202.jpg)

%% Alle gedruckten Teile des Modells revisen, vor allem die Rods zu fixieren und Teile zu minimieren + dimensional accuracy der rod holes zu gewährleisten. 
+ überall noch step by step mittels DXF in Illustrator, analog zu Basic Assembly %%

Build a compact linear translation stage for fine axial adjustment of the focusing optics in the [Full Raman Optical Assembly](Full%20Raman%20Optical%20Assembly.md).

This stage uses:

- Two smooth metal rods as linear guides  
- A micrometer screw for precise movement  
- Two compression springs to pre-load the moving stage  

The design is simple to print and tune, and accurate enough to focus the final lens or fibre position onto the spectrometer input.

> [!NOTE] Where this stage is used  
> In the recommended build path, this translation stage sits underneath the **Focusing Assembly** [Focusing Assembly](Basic%20Raman%20Optical%20Assembly.md#Focusing%20Assembly) in the [Full Raman Optical Assembly](Full%20Raman%20Optical%20Assembly.md).  
> It is **not** required for the [Basic Raman Optical Assembly](Basic%20Raman%20Optical%20Assembly.md) but strongly recommended for comfortable fine focus adjustment.

---

## Parts and Materials

### Sourced parts

| Part                          | Qty | Specification / notes                                                              |
| ----------------------------- | --- | ---------------------------------------------------------------------------------- |
| Micrometer screw              | 1×  | ~10–15 mm travel, with mounting nut/collar                                         |
| Metal rods, ⌀ 6 mm            | 2×  | ≥ 55 mm length, straight, smooth surface                                           |
| Compression springs, ⌀ ≥ 6 mm | 2×  | Inner diameter slightly larger than 6 mm; stiffness chosen for light pre-load      |
| M3.5 screw + washer + nut     | 4×  | ≥ 20 mm length (for mounting the stage to the main baseplate or frame)             |
| Sandpaper                     | –   | ~150–240 grit for fine tuning of rod holes                                         |
| (Optional) Lubricant          | –   | Light machine oil or PTFE/silicone-based lubricant for rods and sliding interfaces |

> [!NOTE] Micrometer choice  
> Any mechanical micrometer head with ~10–15 mm travel is suitable. The exact scale, brand and knob style are not critical as long as the body fits the printed holder.

---

### 3D-printed parts

> [!NOTE] STL files  
> All STL files are provided in the project repository. The BOM IDs below are used consistently across the documentation.

| BOM-ID | Part name (.stl)              | Qty | Recommended print orientation                     | Notes                                                                 | Preview |
| ------ | ----------------------------- | --- | ------------------------------------------------- | --------------------------------------------------------------------- | ------- |
| 011    | `LinearStage_Base_STL`        | 1×  | Hole grid facing the build plate                  | Rod holes oversized (~⌀ 6.65 mm) to compensate vertical printing      | ![LinearStage_Base](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%204.jpg) |
| 012    | `LinearStage_Stage_STL`       | 1×  | Rod holes facing the build plate                  | Rod holes sized (~⌀ 6.2 mm) for a snug but movable fit                | ![LinearStage_Stage](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%203.jpg) |
| 013    | `LinearStage_Frontplate_STL`  | 1×  | Flat face down, holes facing up                   | Optional stiffening / front support plate (recommended)               | ![LinearStage_Frontplate](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%207.jpg) |

> [!TIP] Suggested print settings  
> - Material: PETG-CF or regular PETG for stiffness and wear resistance  
> - Layer height: 0.2 mm  
> - Perimeters: ≥ 3 walls  
> - Infill: 30–40 % grid or gyroid  
> - Supports: Not required in the recommended orientations

---

## Preparing the Printed Parts

Good rod fit is critical for smooth and repeatable motion. Before full assembly, verify and tune the fit of the rods in both the base and the moving stage.

### Step 1 – Base (BOM 011, rod fit)

For the base, the rods should press in firmly and not move once installed.

1. Measure the rod diameter with digital callipers to confirm ~⌀ 6.0 mm.  
2. Push each rod all the way through the rod holes in `LinearStage_Base_STL`:

   ![Checking rod fit in the base](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%205.jpg)

   - You should feel noticeable, even resistance as the rod enters the holes.  
   - Once inserted, the rods should not wobble or rattle in the base.

3. If the rods **do not fit at all**:  
   - Lightly sand the inside of the rod holes with rolled-up sandpaper.  
   - Clean the dust and test the fit again. Repeat until the rod can be pressed through with firm pressure.

> [!WARNING] Sanding fibre-reinforced filaments  
> When sanding PETG-CF or similar materials, wear appropriate PPE (at least a particle mask). Fine fibres and plastic dust can be harmful if inhaled, especially with repeated exposure.

4. If the rods have **visible play**:  
   - First confirm that the rods are actually ⌀ 6.0 mm (cheap rods can vary).  
   - If rods are correct, consider slightly shrinking the holes in your CAD/source file or using slicer hole compensation to reduce the effective hole size, then re-print the base.

> [!TIP] Print seam settings  
> If your slicer allows it, use **random seam positioning** for this part. This avoids a single pronounced seam ridge inside the hole that can interfere with accurate rod fit.



---

### Step 2 – Stage (BOM 012, sliding fit)

The stage must slide smoothly on the rods with minimal play.

1. Insert a rod into one of the holes in `LinearStage_Stage_STL` and push it through:

   ![Checking rod fit in the stage](../../assets/images_picked/Linear-Translation-Stage/Linear%20Translation%20Stage%20Part%20-%20Desktop%20-%206.jpg)

   - The rod should move with slight resistance but **not** bind or jam.  
   - A small amount of stiffness is acceptable and often improves after some movement or light lubrication.

2. Repeat for the second rod hole. Both rods should slide similarly.

3. If the fit is **too tight or jerky**:  
   - Very lightly sand the inside of the rod holes.  
   - Clean the dust and test again.

4. If the fit is **very loose** and the stage can tilt on the rods, consider:  
   - Reducing the hole size in the source file or with slicer hole compensation, then re-printing, or  


> [!INFO] Clean after sanding  
> After sanding, remove dust with compressed air or a vacuum and wipe the parts with a damp paper towel. Loose particles can increase friction and wear over time.

---

## Assembly

![Exploded view and motion of the linear stage](../../assets/images_animated/Animation_LinearStage%20v6_1_aGIF_256px.gif)

Once the printed parts are tuned for proper rod fit, you can assemble the stage.

### Step 3 – Install the micrometer screw

1. Insert the **micrometer head** into the central opening of `LinearStage_Base_STL` from the front.  
2. Use the nut supplied with the micrometer to secure it against the base.  
3. Make sure that:  
   - The micrometer axis is aligned with the central recess in the `LinearStage_Stage_STL`. 
   - The micrometer body does not collide with the rods or springs over the full range of motion.

> [!TIP] Avoid overtightening the micrometer nut  
> Tighten only until the micrometer body does not move when you try to rotate or pull it by hand. Over-tightening can warp the printed base or damage the micrometer threads.

---

### Step 4 – Install rods and stage

![Assembly animation – base, rods, stage, springs](../../assets/images_animated/Animation_LinearStage_Assembly_512px_DIYraman_GIF.gif)

1. Insert both ⌀ 6 mm rods from the **same side** of the `LinearStage_Base_STL`. Push them approximately **one third** of the way in.  
2. Position the `LinearStage_Stage_STL` so that its central recess faces the **tip of the micrometer screw**.  
3. Carefully align the two rod holes in the stage with the rods and slide the stage onto the rods.  
4. Make sure the micrometer tip sits in the central recess of the stage or contacts the intended push surface.  
5. Push the rods further through the base and stage until they protrude slightly on the opposite side, leaving room for the springs.

> [!WARNING] Do not force misaligned rods  
> If the rods do not slide through the stage easily, remove the stage and check alignment. Forcing misaligned rods can crack the printed part or bend the rods.

---

### Step 5 – Add the springs

1. Slide one compression spring onto each rod.  
   - It is often easiest to place the spring on the rod first and then compress it into the recess between base and stage.  
2. Seat each spring so it sits **between the base and the stage** in the intended recess, providing a light pushing force against the stage.  
3. Push the rods fully into the base until:  
   - The springs are slightly pre-loaded (compressed a few millimetres), and  
   - The rods are fully seated in both ends of the base.

4. Gently turn the micrometer screw to move the stage through its travel:  
   - The stage should move smoothly with no sudden jumps.  
   - There should be minimal backlash (lost motion) when reversing direction.  
   - The springs should stay seated and not buckle.

5. Apply a **small amount of lubricant** to the rods if needed to improve the feel of the motion.

---

### Step 6 – Optional: Front plate (BOM 013)
%% Frontplate anders implementieren, wobei print orientation hier schon essenziell ist, wenn die Stage vertikal gedruckt wird - vor allem für die Rod holes. Eventuell die Base anders gestalten, um beide Seiten flush aber in richtiger Orientierung geprinted zu haben %%
1. Align `LinearStage_Frontplate_STL` with the corresponding holes on the front of the `LinearStage_Base_STL`.  
2. Fix the front plate with four suitable screws (e.g. M3.5 with washers and nuts), tightening evenly.  
3. Verify that:  
   - The rods remain parallel and properly seated.  
   - The stage still moves freely over the desired range.  
   - The micrometer tip remains correctly engaged with the stage.

The front plate increases stiffness at the front end of the rods and reduces the risk of flex when the stage changes direction.

---

## Mounting to the Raman Baseplate

In the **Full Raman Optical Assembly**, this stage is mounted beneath the focusing optics module.

1. Identify the mounting pattern for the translation stage on your Raman baseplate (see [Full Raman Optical Assembly](Full%20Raman%20Optical%20Assembly.md)).  
2. Disassemble the desired `Defaultholder` that holds the focusing lens by sliding it off the assembly rods.
3. Use four screws to mount the optic holder to the stage.
4. Place the assembled linear translation stage on the baseplate and align the mounting holes.  
5. Use four screws and nuts to fasten the stage - using an L-bracket - to the baseplate.  
6. Tighten all screws evenly, then verify that the stage still moves smoothly, no screw heads interfere, and that the micrometer remains accessible from the desired side.

> [!NOTE] Orientation on the baseplate  
> Mount the stage so that the micrometer is accessible from the front or side you find most convenient when adjusting. The exact orientation is not critical as long as the axis of motion aligns with the optical axis of the focusing optics.

---

## Design Notes and Tuning

For this design, part of the micrometer’s total travel is intentionally used to:

- Pre-load the springs (so the stage is always pressed firmly against the micrometer tip), and  
- Avoid fully compressing the springs at the end of travel (to keep motion smooth and predictable).

In practice, the **useful travel** of the stage is around **5 mm**, which is more than sufficient for fine focus adjustment of the final lens (or fibre input) in the [Full Raman Optical Assembly](Full%20Raman%20Optical%20Assembly.md).

The spring pre-load:

- Reduces backlash when reversing micrometer direction  
- Keeps the stage under constant tension  
- Improves repeatability of small position changes

> [!NOTE] Tuning the feel  
> You may need to experiment with different springs and pre-load amounts.  
> - Too little tension → noticeable backlash and vague response when reversing.  
> - Too much tension → high torque required on the micrometer, especially near travel limits.  
> Aim for a point where the stage moves smoothly and repeatably with moderate turning force.


---

## Related

- [Build an Overpressure Glove Box](Overpressure%20Glove%20Box.md)  
- [Basic Raman Optical Assembly](Basic%20Raman%20Optical%20Assembly.md)  
- [Full Raman Optical Assembly](Full%20Raman%20Optical%20Assembly.md)  
