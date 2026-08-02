# FCOS Enterprise Studio

# Evidence Hierarchy Specification

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Evidence Hierarchy defines how FCOS Enterprise Studio determines the authoritative source for every product attribute during catalog processing.

The objective is to ensure deterministic, repeatable, and enterprise-grade catalog generation by always selecting the highest-confidence evidence available.

Lower-priority evidence shall never overwrite higher-priority evidence.

---

# Evidence Priority Order

FCOS shall always evaluate product attributes in the following order:

Level 1
Excel / Manufacturer Workbook

↓

Level 2
Supplier Catalog Description

↓

Level 3
Visual AI

↓

Level 4
Fashion Intelligence Reasoning

---

# Level 1 — Excel / Manufacturer Workbook

Priority:
Highest

Excel is the primary source of truth.

Whenever an attribute exists in the workbook, FCOS shall use the workbook value without modification.

Workbook values always override Catalog Description, Visual AI, and Fashion Intelligence.

Typical workbook attributes include:

- Colour
- Fabric
- Size
- Bust Size
- Chest Size
- Stitching Status
- SKU
- Product Code
- Price
- Garment Measurements
- Saree Length
- Dupatta Length
- Blouse Piece Length
- Manufacturer Specifications

Example

Workbook

Colour = Rani Pink

Image appears Deep Pink

Output

Colour = Rani Pink

Visual colour analysis must never overwrite workbook colour.

---

# Level 2 — Supplier Catalog Description

Priority:
Second

When a required attribute is unavailable in Excel, FCOS shall use the Supplier Catalog Description.

Typical attributes include:

- Product Type
- Product Subtype
- Occasion
- Pattern
- Work Detail
- Construction
- Style Identity
- Design Information
- Marketing Description

Catalog Description always overrides Visual AI.

Example

Workbook

Pattern = Missing

Catalog

Paisley Printed

Visual AI

Floral Printed

Output

Pattern Detail = Paisley Printed

---

# Level 3 — Visual AI

Priority:
Third

Visual AI shall be used only when an attribute is unavailable in both:

• Excel

AND

• Catalog Description

Visual AI may determine:

- Product Type
- Product Subtype
- Construction
- Silhouette
- Garment Components
- Sleeve Style
- Sleeve Length
- Neck Style
- Garment Length
- Pattern Detail
- Work Detail
- Occasion
- Style Identity
- Design Aesthetic

Visual AI shall never contradict workbook or catalog information.

---

# Level 4 — Fashion Intelligence Reasoning

Priority:
Fourth

Fashion Intelligence is the final inference layer.

It may infer attributes only when:

- Excel is unavailable
- Catalog Description is unavailable
- Visual AI confidence is insufficient

Fashion Intelligence uses:

- Fashion construction rules
- Garment architecture
- Commercial classification
- Styling conventions
- Pattern placement
- Construction relationships
- Fashion terminology
- Industry best practices

If confidence is insufficient, the attribute shall be omitted.

FCOS never invents unsupported information.

---

# Attribute Resolution Rules

## Always Taken from Excel

When available, the following attributes shall always come from Excel:

- Colour
- Fabric
- Size
- Bust Size
- Chest Size
- Stitching Status
- Product Measurements
- Saree Length
- Dupatta Length
- Blouse Piece Length

Visual AI must never replace these values.

---

## Catalog Preferred Attributes

When unavailable in Excel:

- Product Type
- Product Subtype
- Pattern Detail
- Work Detail
- Occasion
- Construction
- Style Identity
- Design Aesthetic

shall be taken from Catalog Description.

---

## Visual AI Attributes

Visual AI may detect only when unavailable in both Excel and Catalog Description:

- Sleeve Style
- Sleeve Length
- Neck Style
- Construction
- Silhouette
- Garment Components
- Garment Length
- Pattern Detail
- Work Detail
- Product Type
- Product Subtype
- Occasion

Visual AI shall never modify existing workbook or catalog values.

---

# Colour Rule

Colour shall always be taken from:

Excel

↓

Catalog Description

Visual colour analysis shall only be used when both Excel and Catalog Description are unavailable.

---

# Fabric Rule

Fabric shall always be taken from:

Excel

↓

Catalog Description

Visual AI may estimate only when no documented fabric information exists.

---

# Measurement Rule

Measurements shall follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Examples:

- Bust Size
- Chest Size
- Sleeve Length
- Kurta Length
- Choli Length
- Lehenga Length

Saree Length and Dupatta Length shall always retain the original catalog measurement when available.

---

# Confidence Rules

FCOS shall generate an attribute only when sufficient evidence exists.

If confidence is insufficient:

- Do not estimate
- Do not invent
- Do not hallucinate

Omit the attribute.

---

# Conflict Resolution

If multiple sources disagree:

Higher-priority evidence always wins.

Example

Workbook

Fabric = Cotton Blend

Catalog

Silk Blend

Visual AI

Cotton

Output

Fabric = Cotton Blend

---

# Universal Evidence Principles

FCOS follows these principles:

✓ Excel is authoritative.

✓ Catalog Description supplements missing workbook data.

✓ Visual AI fills only verified gaps.

✓ Fashion Intelligence performs controlled inference.

✓ Unsupported attributes are omitted.

✓ No hallucinated values.

✓ Every generated attribute must be traceable to an evidence source.

✓ Higher-priority evidence always overrides lower-priority evidence.

---

# Evidence Resolution Workflow

Excel Workbook
        │
        ▼
Supplier Catalog Description
        │
        ▼
Visual AI Analysis
        │
        ▼
Fashion Intelligence Reasoning
        │
        ▼
Attribute Validation
        │
        ▼
Final Enterprise Output

---

# Scope

This document governs only evidence selection and attribute resolution.

The following specifications are maintained separately:

- ProductNaming.md
- StyleInformation.md
- MeasurementRules.md
- DescriptionEngine.md
- Validation.md
- SareeRules.md
- MenswearRules.md
- WomenswearRules.md
- KidswearRules.md
- JewelleryRules.md
