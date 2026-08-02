# FCOS Enterprise Studio

# Saree Rules

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Saree Rules specification defines all category-specific processing rules for Sarees within FCOS.

These rules supplement the Universal Specifications and shall take precedence whenever the detected Category Type is a Saree or any Saree-derived product.

Examples

- Saree
- Designer Saree
- Printed Saree
- Embroidered Saree
- Banarasi Saree
- Kanjivaram Saree
- Silk Saree
- Linen Saree
- Organza Saree
- Ready-to-Wear Saree
- Saree Gown
- Lehenga Saree

---

# Rule 45 – Saree Component Recognition

FCOS shall recognise and classify every visible saree component separately.

Possible components include:

- Saree
- Blouse
- Blouse Piece
- Ready Blouse
- Petticoat (if supplied)
- Belt
- Jacket
- Cape
- Shrug

Each component shall retain its own attributes wherever applicable.

Examples

Saree Fabric

Blouse Fabric

Blouse Piece Length

Saree Length

---

# Rule 52 – Saree Measurement Rules

Saree measurements shall always use manufacturer values whenever available.

Priority

Excel Workbook

↓

Catalog Description

↓

Visual AI

Rules

• Saree Length shall never be visually estimated if supplied in Excel or Catalog.

• Blouse Piece Length shall use the manufacturer measurement.

• Visual AI may estimate Blouse Length only for stitched blouses when no authoritative data exists.

Examples

Saree Length: 5.50 Meter

Dupatta Length: 2.20 Meter

Blouse Piece Length: 0.80 Meter

---

# Rule 53 – Ready-to-Wear Saree Recognition

FCOS shall distinguish between:

- Traditional Saree
- Ready-to-Wear Saree
- Saree Gown
- Lehenga Saree

Recognition shall be based on:

- Excel
- Catalog Description
- Visual Evidence

Visual construction shall take precedence over generic naming when authoritative data is unavailable.

Examples

Correct

Ready-to-Wear Saree

Saree Gown

Lehenga Saree

Incorrect

Saree

(where the construction clearly represents a Ready-to-Wear Saree or Saree Gown)

---

# Rule 55 – Saree Style Information

Style Information for Sarees shall follow the Universal Style Information sequence while including only applicable fields.

Examples

Free Size: 38–42 Inches,
Colour: Emerald Green,
Saree Fabric: Organza,
Blouse Fabric: Silk Blend,
Saree Length: 5.50 Meter,
Blouse Piece Length: 0.80 Meter,
Blouse Length: 14-16 Inches,
Sleeve Style: Puff Sleeves,
Sleeve Length: 6-8 Inches,
Neck Style: V Neck,
Pattern Detail: Floral Printed,
Work Detail: Thread & Sequin Embroidery,
Occasion: Festive,
Stitching Status: Unstitched,
Style Type: Contemporary Elegance,
Design Aesthetic: Floral Romance,
Category Type: Designer Saree

Rules

• Use 32-42 Inches if the size is not mentioned.

• Include Blouse Length, Sleeve Style, Sleeve Length, Neck Style for unstitched blouses by viewing the image as the blouse will be stitched.

• Include Blouse Piece Length only when supplied.

• Preserve manufacturer measurements for Saree Length and Blouse Piece Length.

• Omit unavailable fields completely.

---

# Universal Saree Rules

FCOS shall:

✓ Preserve manufacturer measurements.

✓ Detect Ready-to-Wear Sarees separately from Traditional Sarees.

✓ Recognise Saree-derived constructions.

✓ Separate Saree Fabric from Blouse Fabric.

✓ Maintain component-specific attributes.

✓ Follow the Evidence Hierarchy.

✓ Generate category-specific Product Names.

✓ Generate unique editorial descriptions.

✓ Apply Universal Validation Rules.

---

---

# Saree Intelligence Module

## Purpose

The Saree Intelligence Module enables FCOS to recognise, classify, and process Saree products using category-specific Fashion Intelligence before applying downstream specifications.

Instead of treating all Sarees uniformly, FCOS shall first determine the Saree Family, followed by the specific Saree Construction, before applying Product Naming, Style Information, Measurement Rules, and Description Generation.

This ensures category-specific behaviour while preserving consistency with the enterprise Product Intelligence architecture.

---

# Saree Classification Workflow

Every Saree shall be classified using the following sequence:

Evidence Hierarchy

↓

Saree Family

↓

Primary Saree Construction

↓

Specific Saree Type

↓

Component Recognition

↓

Category Validation

---

# Saree Families

## 1. Traditional Sarees

Description

Traditional woven or handcrafted sarees whose primary identity is defined by weaving heritage and regional craftsmanship.

Examples

- Regular Saree
- Handloom Saree
- Banarasi Saree
- Kanjivaram Saree
- Patola Saree
- Chanderi Saree
- Paithani Saree
- Sambalpuri Saree
- Jamdani Saree

Recognition Rule

Traditional Sarees shall preserve recognised regional terminology whenever supported by the Evidence Hierarchy.

---

## 2. Contemporary Sarees

Description

Modern sarees whose identity is primarily driven by design, print, embroidery, or contemporary styling.

Examples

- Designer Saree
- Printed Saree
- Embroidered Saree
- Ruffle Saree
- Digital Printed Saree
- Sequinned Saree

Recognition Rule

Contemporary Sarees shall prioritise commercially recognised fashion terminology.

---

## 3. Engineered Sarees

Description

Sarees incorporating engineered garment construction beyond traditional draping.

Examples

- Ready-to-Wear Saree
- Pre-Stitched Saree
- Saree Gown
- Lehenga Saree

Recognition Rule

Visual construction shall determine the engineered category whenever Excel and Catalog Description are unavailable.

---

# Recognition Priority

FCOS shall classify Sarees using:

1. Excel Workbook

↓

2. Catalog Description

↓

3. Visual AI

↓

4. Fashion Reasoning

Higher-priority evidence shall always override lower-priority evidence.

---

# Enterprise Principles

FCOS shall:

✓ Preserve recognised saree terminology.

✓ Preserve regional product identity.

✓ Distinguish engineered sarees from traditional sarees.

✓ Maintain separate recognition for Saree, Blouse, and Blouse Piece.

✓ Apply category-specific naming, measurements, style information, and description rules.

✓ Follow the Universal Evidence Hierarchy.

---

# Related Specifications

- EvidenceHierarchy.md
- ProductNaming.md
- StyleInformation.md
- MeasurementRules.md
- DescriptionEngine.md
- Validation.md
