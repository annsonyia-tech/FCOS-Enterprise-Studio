# FCOS Enterprise Studio
# Evidence Hierarchy Specification
Version: 1.0

---

# Purpose

The Evidence Hierarchy defines the order in which FCOS Enterprise retrieves, validates, and applies product attributes.

The hierarchy guarantees that higher-confidence sources always override lower-confidence sources, ensuring consistent, deterministic, and reproducible catalog generation.

---

# Evidence Priority

FCOS shall always evaluate product information in the following order:

1. Excel / Manufacturer Workbook
2. Supplier Catalog Description
3. Visual AI
4. Fashion Reasoning

Lower-priority evidence must never overwrite higher-priority evidence.

---

# Level 1 — Excel / Manufacturer Workbook

Priority: Highest

Excel is the authoritative source.

Whenever an attribute exists in the workbook, FCOS must use that value without modification.

Examples:

- Colour
- Fabric
- Size
- Stitching Status
- Product Code
- SKU
- Price
- Measurements
- Manufacturer Data

Visual AI must never replace Excel values.

Example

Workbook:
Colour = Rani Pink

Image:
Appears Dark Pink

Output:

Colour: Rani Pink

---

# Level 2 — Supplier Catalog Description

If an attribute is missing from Excel, FCOS shall use the supplier catalog description.

Examples:

- Occasion
- Work Detail
- Product Type
- Product Subtype
- Construction
- Pattern

Catalog values override Visual AI.

Example

Workbook:
Pattern = Missing

Catalog:
Paisley Printed

Image:
Looks Floral

Output:

Pattern Detail:
Paisley Printed

---

# Level 3 — Visual AI

Visual AI is used only when the attribute is unavailable in both:

• Excel
• Catalog Description

Visual AI may determine:

- Product Type
- Product Subtype
- Construction
- Silhouette
- Sleeve Style
- Sleeve Length
- Neck Style
- Garment Length
- Pattern Detail
- Work Detail
- Occasion

Visual AI must never contradict Excel or Catalog data.

---

# Level 4 — Fashion Reasoning

Fashion Reasoning is the final fallback.

It may infer attributes only when:

• Excel is unavailable
• Catalog is unavailable
• Visual AI cannot confidently determine the value

Fashion Reasoning uses:

- Garment architecture
- Construction
- Pattern placement
- Tailoring conventions
- Fashion terminology
- Commercial classification

If confidence is insufficient, the attribute shall be omitted.

FCOS never guesses.

---

# Universal Rules

✓ Higher-priority evidence always wins.

✓ Lower-priority evidence never overrides higher-priority evidence.

✓ Missing values may be inferred only when allowed by this hierarchy.

✓ Unsupported values must be omitted.

✓ AI must never hallucinate attributes.

✓ Every generated attribute must be traceable to its evidence source.

---

# Evidence Flow

Excel
        ↓
Catalog Description
        ↓
Visual AI
        ↓
Fashion Reasoning
        ↓
Final Validated Output
