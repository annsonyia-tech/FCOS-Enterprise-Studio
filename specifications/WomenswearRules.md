# 15. Visual Garment Measurement Rules

## 15.1 Measurement Evidence Hierarchy

Garment lengths shall be determined using the following priority:

Excel
↓

Catalog Description
↓

Visual AI

Higher-priority evidence shall always take precedence.

---

## 15.2 Women's Reference Model Height

When Visual AI is required to estimate garment lengths, FCOS shall assume the following standard reference model height:

**Women = 5 ft 4 in (163 cm)**

All visual garment length estimation shall be performed relative to this reference model.

---

## 15.3 Components to Measure

FCOS shall visually estimate the following garment component lengths independently when they are not available in the Excel workbook or Catalog Description:

### Upper Garments

- Blouse Length
- Choli Length
- Long Choli Length
- Kurti Length
- Kurta Length
- Tunic Length
- Top Length
- Peplum Length
- Jacket Length
- Cape Length
- Kaftan Length
- Gown Length
- Dress Length

### Lower Garments

- Lehenga Length
- Skirt Length
- Palazzo Length
- Pant Length
- Sharara Length
- Gharara Length
- Dhoti Length
- Churidar Length
- Salwar Length

Each garment component shall be measured independently.

---

## 15.4 Length Normalization

All apparel component lengths shall be displayed as standardized **2-inch ranges**.

Examples:

12 Inches → 10–12 Inches

16 Inches → 14–16 Inches

20 Inches → 18–20 Inches

22 Inches → 20–22 Inches

40 Inches → 38–40 Inches

42 Inches → 40–42 Inches

44 Inches → 42–44 Inches

51 Inches → 50–52 Inches

The actual measurement shall be represented within the displayed range.

---

## 15.5 Exceptions

The following measurements shall **not** be normalized and shall retain their exact catalog values:

- Saree Length
- Dupatta Length
- Fabric Cut Lengths
- Blouse Piece Length

Examples:

Saree Length: 5.50 Meter

Dupatta Length: 2.20 Meter

Blouse Piece Length: 0.80 Meter

---

## 15.6 Confidence Rule

Visual garment lengths shall only be generated when the garment is sufficiently visible.

If confidence is insufficient and no higher-priority evidence exists, omit the length attribute rather than estimating or inventing a value.

---

## 15.7 Validation

The Validation Engine shall verify that:

- Excel values are never overridden by Visual AI.
- All apparel lengths follow the standardized 2-inch normalization rule.
- Saree Length, Dupatta Length, and Fabric Cut Lengths retain their exact catalog measurements.
- Each garment component is measured independently.
