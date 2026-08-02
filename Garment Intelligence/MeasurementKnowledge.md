# FCOS Enterprise
## Measurement & Size Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Measurement & Size Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, validate, and present garment measurements consistently across Women's Wear, Men's Wear, Kids' Wear, Jewellery (where applicable), Ethnic Wear, Indo-Western Wear, and Western Wear.

Measurements are independent of:

• Product Type
• Product Subtype
• Pattern
• Work Detail
• Design Aesthetic
• Style Type

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine measurements only when higher-priority evidence is unavailable.

---

# Universal Measurement Rules

Measurements shall always follow the Evidence Hierarchy.

Never allow Visual AI to overwrite Excel.

Never estimate measurements when reliable evidence is unavailable.

If confidence is insufficient

↓

Omit the measurement.

Never output NA, Unknown, or placeholders.

---

# Size Rules

Women's Apparel

↓

Bust Size

Men's Apparel

↓

Chest Size

Kids' Apparel

↓

Chest Size

Sarees, Dupattas and other non-fitted products

↓

Free Size where applicable

---

# Size Normalization

Convert supplier sizing into standardized measurement ranges whenever reliable measurements exist.

Examples

36"

↓

36–40 Inches

40"

↓

40–44 Inches

44"

↓

44–48 Inches

Free Size

↓

38–42 Inches

Free Size upto 46

↓

38–46 Inches

If multiple sizes exist

Example

36, 38, 40, 42

↓

Bust Size:
36–42 Inches

---

# Length Normalization

All apparel component lengths shall be displayed as standardized 2-inch ranges.

Formula

Display Length

↓

Actual Length − 1 inch

to

Actual Length + 1 inch

Examples

12"

↓

10–12 Inches

14"

↓

12–14 Inches

20"

↓

18–20 Inches

22"

↓

20–22 Inches

42"

↓

40–42 Inches

51"

↓

50–52 Inches

---

# Length Exceptions

Do NOT normalize

Saree Length

Dupatta Length

Fabric Cut Length

Blouse Piece Length

These retain manufacturer measurements.

Examples

Saree Length:
5.50 Meter

Dupatta Length:
2.20 Meter

Blouse Piece:
0.80 Meter

---

# Measurement Categories

## Upper Garment

Bust Size

Chest Size

Shoulder

Armhole

Sleeve Length

Sleeve Opening

Kurta Length

Kurti Length

Top Length

Shirt Length

Jacket Length

Blouse Length

Choli Length

Cape Length

Kaftan Length

Dress Length

Gown Length

---

## Lower Garment

Waist

Hip

Rise

Inseam

Outseam

Bottom Length

Pant Length

Palazzo Length

Trouser Length

Sharara Length

Gharara Length

Dhoti Length

Skirt Length

Lehenga Length

---

## Saree

Saree Length

Blouse Piece Length

---

## Dupatta

Dupatta Length

Dupatta Width

---

## Jewellery

Chain Length

Pendant Length

Bracelet Length

Bangle Diameter

Ring Size

Earring Length

---

# Measurement Units

Supported Units

Inches

Centimetres (CM)

Meters

Millimetres (MM)

Never mix units.

Preserve manufacturer units whenever available.

---

# Visual Measurement Rules

Visual AI may estimate only

Garment Length

Sleeve Length

Cape Length

Jacket Length

Dress Length

Kurta Length

Kurti Length

Lehenga Length

Pant Length

Only when Excel and Catalog Description are unavailable.

---

# Validation Rules

Measurements must

Be positive

Use consistent units

Follow normalization rules

Match product category

Never exceed realistic garment proportions

---

# Style Information Rules

Include only applicable measurements.

Examples

Bust Size

Kurti Length

Sleeve Length

Lehenga Length

Never include irrelevant fields.

---

# Confidence Rules

High Confidence

↓

Output measurement.

Medium Confidence

↓

Output only if not contradicted.

Low Confidence

↓

Omit measurement.

Never invent values.

---

# Examples

Women's Kurti

Bust Size:
40–44 Inches

Kurti Length:
44–46 Inches

Sleeve Length:
16–18 Inches

---

Men's Kurta

Chest Size:
42–46 Inches

Kurta Length:
40–42 Inches

Sleeve Length:
22–24 Inches

---

Lehenga

Bust Size:
38–42 Inches

Choli Length:
14–16 Inches

Lehenga Length:
40–42 Inches

Dupatta Length:
2.20 Meter

---

Saree

Free Size:
38–42 Inches

Saree Length:
5.50 Meter

Blouse Piece Length:
0.80 Meter

---

# Future-Proof Rule

FCOS shall support any commercially accepted garment measurement using:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown measurement terminology shall be normalized using accepted apparel industry standards.

---
Enterprise Recommendations (FCOS v2.2)

I recommend adding five advanced sections that will make this engine production-ready:

1. Product-Specific Measurement Profiles ⭐⭐⭐⭐⭐

Instead of one generic list, define required measurements by product type.

Example:

Product	Required Measurements
Saree	Saree Length, Blouse Piece Length
Lehenga	Bust Size, Choli Length, Lehenga Length, Dupatta Length
Kurta	Chest/Bust Size, Kurta Length, Sleeve Length
Sherwani	Chest Size, Sherwani Length, Sleeve Length
Dress	Bust Size, Dress Length, Sleeve Length
2. Measurement Validation Matrix ⭐⭐⭐⭐⭐

Define realistic ranges for each measurement.

Example:

Blouse Length: 10–24 Inches
Choli Length: 12–24 Inches
Kurti Length: 24–52 Inches
Lehenga Length: 34–46 Inches
Saree Length: 5.50–6.50 Meters

This helps catch supplier errors.

3. Size Label Mapping ⭐⭐⭐⭐⭐

Normalize labels consistently.

Supplier	FCOS
XS	32–34 Inches
S	34–36 Inches
M	36–38 Inches
L	38–40 Inches
XL	40–42 Inches
XXL	42–44 Inches
4. Measurement Relationships ⭐⭐⭐⭐☆

Use relationships to improve validation.

Examples:

Kurti Length should generally exceed Choli Length.
Sleeve Length cannot exceed Garment Length.
Dupatta Length is independent of Lehenga Length.
5. Custom Stitching Measurements ⭐⭐⭐⭐⭐

Keep these as internal tailoring attributes, not Style Information:

Shoulder
Armhole
Front Neck Depth
Back Neck Depth
Bicep
Wrist
Waist
Hip
Thigh
Knee
Calf
Inseam
Outseam

These are invaluable for made-to-measure workflows but should not clutter the standard ecommerce output.
