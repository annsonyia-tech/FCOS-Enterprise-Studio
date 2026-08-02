# FCOS Enterprise
## Sleeve Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Sleeve Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe sleeve styles and sleeve lengths across Women's Wear, Men's Wear, Kids' Wear, Ethnic Wear, Indo-Western Wear, and Western Wear.

Sleeve Style and Sleeve Length are independent attributes.

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Sleeve Style and Sleeve Length only when higher-priority evidence is unavailable.

---

# Definition

## Sleeve Style

Sleeve Style describes the structural design, shape, or construction of the sleeve.

Examples

✔ Puff Sleeves

✔ Bell Sleeves

✔ Cape Sleeves

✔ Bishop Sleeves

✔ Raglan Sleeves

NOT

✘ Full Sleeves

✘ Half Sleeves

These describe Sleeve Length.

---

## Sleeve Length

Sleeve Length describes how far the sleeve extends on the arm.

Examples

✔ 6–8 Inches

✔ 10–12 Inches

✔ 20–22 Inches

NOT

✘ Puff Sleeves

✘ Bell Sleeves

---

# Sleeve Style Categories

## Basic Sleeves

Set-in Sleeves

Regular Sleeves

Kimono Sleeves

Raglan Sleeves

Dolman Sleeves

Batwing Sleeves

Cape Sleeves

Extended Shoulder Sleeves

Dropped Shoulder Sleeves

---

## Volume Sleeves

Puff Sleeves

Balloon Sleeves

Bishop Sleeves

Leg-of-Mutton Sleeves

Juliet Sleeves

Lantern Sleeves

Gigot Sleeves

---

## Flared Sleeves

Bell Sleeves

Trumpet Sleeves

Angel Sleeves

Butterfly Sleeves

Flutter Sleeves

Petal Sleeves

---

## Traditional Sleeves

Churidar Sleeves

Roll-Up Sleeves

Tab Sleeves

Slit Sleeves

Layered Sleeves

Cape Attached Sleeves

Cold Shoulder Sleeves

Open Shoulder Sleeves

---

## Designer Sleeves

Ruffle Sleeves

Tiered Sleeves

Pleated Sleeves

Gathered Sleeves

Smocked Sleeves

Ruched Sleeves

Cut-Out Sleeves

Asymmetric Sleeves

Detachable Sleeves

Embroidered Sleeves

Sheer Sleeves

Mesh Sleeves

Lace Sleeves

---

## Sleeveless Variants

Sleeveless

Strap Sleeves

Spaghetti Strap

Broad Strap

One Shoulder

Off Shoulder

Halter Neck (No Sleeves)

Tube

---

# Sleeve Length Rules

Convert all sleeve lengths into standardized 2-inch ranges.

Examples

Actual

4"

↓

4–6 Inches

6"

↓

6–8 Inches

8"

↓

8–10 Inches

10"

↓

10–12 Inches

12"

↓

12–14 Inches

18"

↓

18–20 Inches

22"

↓

20–22 Inches

24"

↓

22–24 Inches

---

# Sleeve Length Categories

Very Short

4–6 Inches

Short

6–8 Inches

Half

8–10 Inches

Elbow

10–12 Inches

Three Quarter

16–18 Inches

Long

20–22 Inches

Full

22–24 Inches

---

# Detection Rules

Use Excel.

↓

If unavailable

Use Catalog Description.

↓

If unavailable

Use Visual AI.

↓

If unavailable

Use Fashion Reasoning.

Never overwrite Excel.

---

# Occlusion Rule

Sleeve Style may be inferred when partially hidden by:

• Dupatta

• Saree Pallu

• Hair

• Jewellery

• Jacket

• Cape

• Pose

• Draping

Inference must never contradict visible evidence.

---

# Normalization Rules

Normalize supplier wording.

Examples

Half Sleeve

↓

Half Sleeves

Elbow Sleeve

↓

Elbow Sleeves

Three Fourth Sleeve

↓

Three-Quarter Sleeves

Full Sleeve

↓

Full Sleeves

Puff Sleeve

↓

Puff Sleeves

Bell Sleeve

↓

Bell Sleeves

---

# Style Information Rules

Always output:

Sleeve Style:
Puff Sleeves

Sleeve Length:
10–12 Inches

Never combine the two fields.

---

# Sleeveless Rule

If Sleeve Style = Sleeveless

↓

Omit Sleeve Length completely.

Correct

Sleeve Style:
Sleeveless

Incorrect

Sleeve Style:
Sleeveless

Sleeve Length:
0 Inches

---

# Confidence Rule

If confidence is insufficient

↓

Omit Sleeve Style and Sleeve Length.

Never invent sleeve information.

---

# Universal Recognition Rule

FCOS shall recognize any commercially accepted sleeve construction supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown sleeve styles shall be normalized using the closest accepted fashion terminology.

---

# Examples

Example 1

Sleeve Style:
Bell Sleeves

Sleeve Length:
20–22 Inches

---

Example 2

Sleeve Style:
Puff Sleeves

Sleeve Length:
8–10 Inches

---

Example 3

Sleeve Style:
Cape Sleeves

Sleeve Length:
Omitted (Style extends as cape)

---

Example 4

Sleeve Style:
Sleeveless

Sleeve Length:
Omitted

---

Example 5

Sleeve Style:
Bishop Sleeves

1. Sleeve Construction Relationships ⭐⭐⭐⭐⭐ (Highly Recommended)

Some sleeve styles are only valid with certain garment constructions.

Example:

Construction	Common Sleeve Styles
Kaftan	Kimono Sleeves, Batwing Sleeves
Cape	Cape Sleeves
Peplum	Puff Sleeves, Bishop Sleeves
Blazer	Set-in Sleeves, Tailored Sleeves
Shirt	Roll-Up Sleeves, Buttoned Sleeves
Kurta	Full Sleeves, Three-Quarter Sleeves, Roll-Up Sleeves

FCOS should use these relationships to improve visual inference.

2. Sleeve by Product Type ⭐⭐⭐⭐⭐

Some sleeve styles are more common for specific products.

Example:

Product Type	Typical Sleeve Styles
Saree Blouse	Puff, Elbow, Cap, Sleeveless
Choli	Elbow, Puff, Full
Kurti	Three-Quarter, Full, Bell
Gown	Bishop, Puff, Cape
Kaftan	Kimono, Batwing
Sherwani	Full
Men's Kurta	Full, Roll-Up

This helps FCOS avoid unrealistic combinations.

3. Sleeve & Neck Compatibility ⭐⭐⭐⭐☆

Certain sleeve styles naturally pair with specific necklines.

Example:

Neck Style	Common Sleeve Styles
Boat Neck	Elbow, Full
Sweetheart Neck	Puff, Elbow
Mandarin Collar	Full, Roll-Up
Halter Neck	Sleeveless
Off Shoulder	Puff, Bishop
Shirt Collar	Full, Roll-Up

This improves inference when one attribute is partially obscured.

4. Sleeve Detection Confidence ⭐⭐⭐⭐⭐

Instead of simply "detect" or "omit," define confidence levels.

Example:

Confidence	Action
High	Output Sleeve Style and Sleeve Length
Medium	Output only if not contradicted by evidence
Low	Omit Sleeve Style and Sleeve Length

This makes FCOS more consistent and reduces incorrect guesses.

5. Commercial Sleeve Terminology ⭐⭐⭐⭐⭐

Normalize supplier wording to standard commercial terms.

Supplier Term	FCOS Output
3/4 Sleeve	Three-Quarter Sleeves
Full Sleeve	Full Sleeves
Half Sleeve	Half Sleeves
Bell Sleeve	Bell Sleeves
Puff Sleeve	Puff Sleeves
Cape Sleeve	Cape Sleeves

Sleeve Length:
22–24 Inches
