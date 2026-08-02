# FCOS Enterprise Studio

# Measurement Rules Specification

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

This specification defines the Universal Measurement Engine used by FCOS Enterprise Studio.

The Measurement Engine standardizes all body measurements, garment measurements, size conversions, and length normalization across every supported product category.

This specification governs only measurement generation.

It does not define Product Naming, Style Information ordering, Description generation, or Validation.

---

# Evidence Hierarchy

All measurements shall follow the FCOS Evidence Hierarchy.

Priority Order

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Measurements shall never be replaced by inferred values when documented values exist.

---

# Universal Measurement Principles

FCOS shall:

✓ Use manufacturer measurements whenever available.

✓ Never invent unsupported measurements.

✓ Normalize garment lengths into standard 2-inch ranges.

✓ Preserve actual manufacturer measurements for Saree Length, Dupatta Length and Blouse Piece Length.

✓ Maintain consistent units throughout the catalog.

---

# Body Size Labels

## Women's Apparel

Use:

Bust Size

Examples

Bust Size: 32–34 Inches

Bust Size: 36–38 Inches

Bust Size: 40–44 Inches

---

## Men's Apparel

Use:

Chest Size

Examples

Chest Size: 38–40 Inches

Chest Size: 40–42 Inches

Chest Size: 42–44 Inches

---

## Kids Wear

Use:

Chest Size

Examples

Chest Size: 24–26 Inches

Chest Size: 26–28 Inches

Chest Size: 30–32 Inches

---

## Non-Fitted Products

Use:

Free Size

Examples

Free Size: 38–42 Inches

Free Size: 38–46 Inches

Only use Free Size when supported by Excel or Catalog.

---

# Size Conversion Rules

If multiple sizes are available,

convert them into one continuous range.

Example

36, 38, 40, 42

↓

Bust Size: 36–42 Inches

---

# Stitched Garment Conversion

Example

Workbook

Blouse Size Stitched 40" (Margin 4")

Output

Bust Size: 40–44 Inches

The stitching margin shall be added only when explicitly provided.

---

# Letter Size Conversion

When numeric measurements are unavailable, convert standard alpha sizes.

| Letter Size | Output |
|-------------|--------|
| XS | 32–34 Inches |
| S | 34–36 Inches |
| M | 36–38 Inches |
| L | 38–40 Inches |
| XL | 40–42 Inches |
| XXL | 42–44 Inches |
| 3XL | 44–46 Inches |
| 4XL | 46–48 Inches |

Workbook measurements always take precedence.

---

# Model Heights

Visual length estimation shall use the following reference heights.

Women

5 ft 4 in

Men

5 ft 10 in

Girls

4 ft

Boys

4 ft 2 in

---

# Garment Length Hierarchy

Garment lengths shall follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

---

# Two-Inch Normalization Rule

Every AI-generated garment length shall be expressed as a 2-inch range.

Examples

Actual

42 Inches

↓

Output

40–42 Inches

---

Actual

44 Inches

↓

Output

42–44 Inches

---

Actual

46 Inches

↓

Output

44–46 Inches

Never output a single garment length unless explicitly supplied as a fixed manufacturer specification.

---

# Garments Using Two-Inch Normalization

Apply normalization to:

- Blouse Length
- Choli Length
- Kurta Length
- Kurti Length
- Kameez Length
- Dress Length
- Gown Length
- Lehenga Length
- Skirt Length
- Pant Length
- Palazzo Length
- Trouser Length
- Pajama Length
- Dhoti Length
- Jacket Length
- Cape Length
- Shrug Length
- Sleeve Length

---

# Sleeve Length Rules

Only include Sleeve Length when sleeves exist.

Examples

8 Inches

↓

6–8 Inches

10 Inches

↓

8–10 Inches

12 Inches

↓

10–12 Inches

18 Inches

↓

16–18 Inches

22 Inches

↓

20–22 Inches

Never generate Sleeve Length for Sleeveless garments.

---

# Saree Length Rules

Saree Length shall always retain the manufacturer's actual measurement.

Examples

5.50 Mtrs

6.30 Mtrs

Do not normalize.

Do not convert to inches.

---

# Ready-to-Wear Saree Rules

Ready-to-Wear Sarees shall contain both:

Saree Length

↓

Actual manufacturer measurement

Blouse Length

↓

Two-inch normalized range

---

# Dupatta Length Rules

Always retain the actual manufacturer measurement.

Examples

2.20 Mtrs

2.30 Mtrs

2.40 Mtrs

Do not normalize.

---

# Blouse Piece Length Rules

Always retain the manufacturer measurement.

Examples

0.80 Mtrs

1.00 Mtrs

Do not normalize.

---

# Width Measurements

Do not normalize width measurements.

Examples

Fabric Width

44 Inches

58 Inches

60 Inches

Use the actual manufacturer value.

---

# Jewellery Measurements

Never normalize jewellery measurements.

Examples

Necklace Length

22 Inches

Chain Length

18 Inches

Bangle Diameter

2.4 Inches

Earring Length

3 Inches

Always preserve the actual measurement.

---

# Missing Measurements

If a measurement cannot be determined from:

- Excel
- Catalog Description
- Visual AI

omit the field.

Never estimate unsupported measurements.

---

# Measurement Formatting

Always use:

Inches

Mtrs

CM

Never use:

"

Approx.

Around

About

Approximately

---

# Examples

Correct

Lehenga Length: 40–42 Inches

Correct

Dupatta Length: 2.20 Mtrs

Correct

Bust Size: 40–44 Inches

Incorrect

Lehenga Length: 42"

Incorrect

Sleeve Length: Approximately 10 Inches

Incorrect

Dupatta Length: 2.20 Metres Approx.

---

# Measurement Validation

Before final output FCOS shall verify:

✓ Correct evidence source used

✓ Correct body size label

✓ Size conversion completed

✓ Two-inch normalization applied where required

✓ Saree Length preserved

✓ Dupatta Length preserved

✓ Blouse Piece Length preserved

✓ Sleeve Length omitted for Sleeveless garments

✓ Units correctly formatted

✓ Unsupported measurements omitted

✓ Catalog-wide measurement consistency maintained

---

---

# Measurement Intelligence Engine

The Measurement Intelligence Engine is responsible for identifying the measurement strategy applicable to each product attribute before normalization or formatting.

Rather than applying a single normalization rule to all measurements, FCOS shall first classify the measurement into its appropriate category and then apply category-specific processing rules.

This architecture ensures scalability, consistency, and support for future product categories without modifying the core measurement engine.

---

# Measurement Classification

Every measurement shall belong to exactly one of the following measurement classes.

## 1. Body Measurements

Purpose

Defines the wearer's body dimensions.

Examples

- Bust Size
- Chest Size
- Waist Size
- Hip Size
- Shoulder
- Arm Hole
- Bicep
- Neck Circumference

Rules

• Always follow the Evidence Hierarchy.

• Convert multiple sizes into a continuous measurement range.

Examples

36, 38, 40, 42

↓

Bust Size: 36–42 Inches

Never estimate unsupported body measurements.

---

## 2. Garment Length Measurements

Purpose

Defines the finished garment dimensions.

Examples

- Blouse Length
- Choli Length
- Kurta Length
- Kurti Length
- Kameez Length
- Dress Length
- Gown Length
- Lehenga Length
- Skirt Length
- Pant Length
- Palazzo Length
- Pajama Length
- Dhoti Length
- Jacket Length
- Cape Length
- Shrug Length
- Sleeve Length

Rules

AI-generated garment lengths shall always be expressed as strict two-inch ranges.

Examples

42 Inches

↓

40–42 Inches

44 Inches

↓

42–44 Inches

Manufacturer-provided ranges shall never be altered.

---

## 3. Accessory Measurements

Purpose

Defines removable garment components.

Examples

- Saree Length
- Dupatta Length
- Blouse Piece Length
- Stole Length
- Shawl Length
- Scarf Length

Rules

Always preserve the manufacturer's original measurement.

Examples

5.50 Mtrs

2.20 Mtrs

0.80 Mtrs

Never normalize.

Never convert to inches.

---

## 4. Jewellery Measurements

Purpose

Defines jewellery dimensions.

Examples

- Necklace Length
- Chain Length
- Pendant Length
- Bracelet Length
- Bangle Diameter
- Ring Size
- Earring Length
- Anklet Length

Rules

Always preserve manufacturer measurements.

Never normalize.

Never estimate unsupported measurements.

---

## 5. Fabric Dimensions

Purpose

Defines raw material dimensions.

Examples

- Fabric Width
- Fabric Length
- Cut Length
- Roll Width

Rules

Always preserve manufacturer values.

Examples

44 Inches

58 Inches

60 Inches

Never normalize.

---

# Measurement Strategy Selection

FCOS shall automatically determine the appropriate Measurement Strategy before processing any measurement.

Processing Order

1. Identify Measurement Type

↓

2. Select Measurement Strategy

↓

3. Apply Category-Specific Rules

↓

4. Validate Measurement

↓

5. Output Final Measurement

---

# Category-Specific Processing

## Body Measurements

- Convert sizes into continuous ranges.
- Preserve workbook measurements.
- Never infer unsupported values.

---

## Garment Lengths

- Apply strict 2-inch normalization.
- Preserve manufacturer ranges.
- Use Visual AI only when permitted by the Evidence Hierarchy.

---

## Accessory Measurements

- Preserve manufacturer values exactly.
- Never normalize.
- Never convert units.

---

## Jewellery Measurements

- Preserve original values.
- Never normalize.
- Never estimate.

---

## Fabric Dimensions

- Preserve original values.
- Never normalize.
- Never convert units.

---

# Measurement Validation

Before output generation, FCOS shall verify:

✓ Correct measurement strategy selected.

✓ Evidence hierarchy followed.

✓ Correct normalization rule applied.

✓ Correct units preserved.

✓ No unsupported measurements generated.

✓ Consistent formatting throughout the catalog.

---

# Future Extensibility

The Measurement Intelligence Engine shall support additional measurement strategies without modifying the existing architecture.

Examples include:

- Footwear Measurements
- Headwear Measurements
- Belt Measurements
- Watch Measurements
- Home Furnishing Dimensions
- Luggage Dimensions
- Future Fashion Categories

Each new strategy shall inherit the same enterprise measurement framework while maintaining its own category-specific processing rules.

# Scope

This specification governs only measurement generation.

Related Specifications

- EvidenceHierarchy.md
- StyleInformation.md
- ProductNaming.md
- DescriptionEngine.md
- Validation.md
