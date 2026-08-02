# FCOS AI Studio Enterprise
# Length Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Visual Measurement Engine

---

# 1. Purpose

Defines all garment length processing, visual estimation, normalization, validation, and output rules used by FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden.

---

# 2. Evidence Hierarchy

Garment lengths shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Length Rules

FCOS shall estimate garment lengths only when:

• Excel does not provide the measurement.

• Catalog Description does not provide the measurement.

• Visual confidence is sufficient.

If confidence is insufficient,

omit the attribute.

Never invent or hallucinate measurements.

---

# 4. Reference Model Heights

Women's Wear

5 ft 4 in (163 cm)

Men's Wear

5 ft 10 in (178 cm)

Boys' Wear

4 ft 2 in (127 cm)

Girls' Wear

4 ft (122 cm)

Visual estimation shall always use the appropriate reference height.

---

# 5. Length Normalization

AI-generated garment lengths shall always be expressed as strict 2-inch ranges.

Examples

Measured Length

42 Inches

↓

40–42 Inches

Measured Length

44 Inches

↓

42–44 Inches

Measured Length

38 Inches

↓

36–38 Inches

Measured Length

20 Inches

↓

18–20 Inches

Measured Length

16 Inches

↓

14–16 Inches

Measured Length

12 Inches

↓

10–12 Inches

Measured Length

10 Inches

↓

8–10 Inches

Measured Length

8 Inches

↓

6–8 Inches

Measured Length

6 Inches

↓

4–6 Inches

---

# 6. Garment Types Supported

FCOS shall support visual measurement for all apparel.

Examples

Kurta

Kameez

Top

Blouse

Choli

Lehenga

Skirt

Dress

Gown

Anarkali

Kaftan

Co-Ord Top

Co-Ord Bottom

Pant

Trouser

Palazzo

Dhoti Pant

Sharara

Gharara

Churidar

Pajama

Sherwani

Nehru Jacket

Waistcoat

Shirt

Jacket

Cape

Kidswear

Future garment types shall inherit these rules.

---

# 7. Fixed Manufacturer Measurements

The following shall never be visually estimated when manufacturer measurements exist.

Saree Length

Dupatta Length

Scarf Length

Stole Length

Shawl Length

These values shall always use the catalog measurement.

Examples

Saree Length

5.50 Meter

Dupatta Length

2.20 Meter

---

# 8. Sleeve Length Rules

Sleeve Length shall follow

Excel

↓

Catalog

↓

Visual AI

↓

Fashion Reasoning

Always output as a 2-inch range.

Examples

10 Inches

↓

8–10 Inches

12 Inches

↓

10–12 Inches

22 Inches

↓

20–22 Inches

If Sleeve Style is Sleeveless,

omit Sleeve Length completely.

---

# 9. Garment Component Length Rules

Each garment component shall be measured independently.

Examples

Blouse Length

Kurta Length

Kameez Length

Choli Length

Top Length

Lehenga Length

Pant Length

Trouser Length

Skirt Length

Dress Length

Sherwani Length

Jacket Length

Cape Length

---

# 10. Validation Rules

Validation Engine shall verify:

• Evidence hierarchy followed

• Correct reference model height used

• Correct 2-inch normalization

• No hallucinated measurements

• Saree and Dupatta retain manufacturer measurements

• Sleeve Length omitted for Sleeveless garments

• Component lengths correctly identified

---

# 11. Output Rules

All apparel lengths shall use inches.

Examples

Kurta Length

42–44 Inches

Lehenga Length

40–42 Inches

Pant Length

38–40 Inches

Blouse Length

18–20 Inches

Saree and Dupatta shall retain metric units supplied by the manufacturer.

Examples

Saree Length

5.50 Meter

Dupatta Length

2.20 Meter

---

# 12. Future Compatibility

FCOS shall automatically support future apparel categories, garment components, and measurement types without requiring architectural changes.
