FCOS AI Studio Enterprise
Visual Measurement Engine Specification
Version: 1.0
Status: Architecture Freeze
1. Purpose

Defines the universal visual garment measurement methodology for all apparel categories.

The Visual Measurement Engine shall estimate garment component lengths only when higher-priority evidence is unavailable and shall normalize apparel lengths into standardized 2-inch ranges while preserving manufacturer-provided measurements where applicable.

2. Measurement Evidence Hierarchy

All garment measurements shall follow:

Excel
↓

Catalog Description
↓

Visual AI

Higher-priority evidence shall never be overridden.

3. Reference Model Heights

When Visual AI performs garment measurement, FCOS shall assume the following standard reference heights.

Category	Reference Height
Women's Wear	5 ft 4 in (163 cm)
Men's Wear	5 ft 10 in (178 cm)
Boys' Wear	4 ft 2 in (127 cm)
Girls' Wear	4 ft (122 cm)

These reference heights shall be used only for proportional garment length estimation.

4. Apparel Components Eligible for Visual Measurement

FCOS shall estimate lengths independently for each visible garment component.

Examples include:

Women's Wear
Blouse
Choli
Kurti
Kurta
Top
Tunic
Jacket
Cape
Kaftan
Gown
Dress
Lehenga
Skirt
Palazzo
Sharara
Gharara
Pant
Dhoti
Churidar
Salwar
Men's Wear
Shirt
Kurta
Jacket
Blazer
Waistcoat
Sherwani
Achkan
Pant
Pajama
Churidar
Dhoti
Salwar
Boys' Wear
Kurta
Shirt
Sherwani
Jacket
Pant
Pajama
Dhoti
Girls' Wear
Choli
Kurti
Dress
Gown
Lehenga
Skirt
Palazzo
Pant

Each component shall be measured independently.

5. Length Normalization

All apparel lengths shall be normalized into 2-inch ranges.

Examples

Actual	Output
12"	10–12 Inches
14"	12–14 Inches
16"	14–16 Inches
18"	16–18 Inches
20"	18–20 Inches
22"	20–22 Inches
40"	38–40 Inches
42"	40–42 Inches
44"	42–44 Inches
6. Measurement Exceptions

The following measurements shall never be normalized and shall retain their catalog values exactly:

Saree Length
Dupatta Length
Blouse Piece Length
Fabric Cut Lengths
Shawl Length
Stole Length

Examples

Saree Length: 5.50 Meter
Dupatta Length: 2.20 Meter
Blouse Piece Length: 0.80 Meter
7. Confidence Rules

Visual measurement shall only be generated when:

The garment is sufficiently visible.
The component is identifiable.
The hemline is visible.
Major portions are not obscured.

If confidence is insufficient and no higher-priority evidence exists, the attribute shall be omitted rather than estimated.

8. Validation Rules

The Validation Engine shall verify:

Excel values are never overridden.
Visual measurements follow the 2-inch normalization rule.
Measurement exceptions retain exact values.
Each garment component is measured independently.
No measurements are generated when confidence is insufficient.
Changes to category rule files

Then simplify each category file to just reference this specification.

For example:

WomenswearRules.md
Visual garment measurement shall follow
VisualMeasurementEngine.md

Reference Model Height:
Women = 5 ft 4 in (163 cm)
MenswearRules.md
Visual garment measurement shall follow
VisualMeasurementEngine.md

Reference Model Height:
Men = 5 ft 10 in (178 cm)
KidswearRules.md
Visual garment measurement shall follow
VisualMeasurementEngine.md

Reference Model Height:
Girls = 4 ft (122 cm)

Boys = 4 ft 2 in (127 cm)
