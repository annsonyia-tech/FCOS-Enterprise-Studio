# FCOS AI Studio Enterprise
# Product Subtype Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Product Subtype Intelligence Engine

---

# 1. Purpose

Defines the rules for determining, validating, normalizing, and outputting the Product Subtype within FCOS AI Studio Enterprise.

Product Subtype identifies the most specific commercially recognizable variant of a Product Type.

This document defines processing rules only and contains no product taxonomy.

---

# 2. Evidence Hierarchy

Product Subtype shall always follow the enterprise evidence hierarchy:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Product Subtype Rules

Every Product Type may have zero or one Product Subtype.

Product Subtype shall only be assigned when confidently supported by available evidence.

If no reliable evidence exists, omit Product Subtype.

Never invent or hallucinate Product Subtypes.

---

# 4. Processing Order

FCOS shall determine product classification using the following hierarchy:

Department

↓

Category

↓

Product Type

↓

Product Subtype

↓

Construction

↓

Silhouette

↓

Pattern

↓

Work

---

# 5. Product Subtype Determination

Product Subtype shall describe the most specific commercially recognized variation of the Product Type.

Examples

Product Type

Lehenga

↓

Possible Product Subtypes

Tiered Lehenga

Panelled Lehenga

Bridal Lehenga

Printed Lehenga

Designer Lehenga

Cape Lehenga

Layered Lehenga

---

Product Type

Saree

↓

Possible Product Subtypes

Ready-to-Wear Saree

Pre-Draped Saree

Designer Saree

Printed Saree

Embroidered Saree

Ruffle Saree

Lehenga Saree

---

Product Type

Kurta Set

↓

Possible Product Subtypes

Straight Kurta Set

Anarkali Kurta Set

A-Line Kurta Set

Jacket Kurta Set

Peplum Kurta Set

Cape Kurta Set

---

# 6. Construction Priority

When a visually distinct construction changes the commercial identity of the product, it shall become the Product Subtype.

Examples

Tiered Lehenga

Panelled Lehenga

Layered Lehenga

Ready-to-Wear Saree

Cape Kurta Set

Jacket Kurta Set

Kaftan Dress

Empire Dress

Angrakha Kurta

High-Low Dress

Future construction-based subtypes shall automatically inherit these rules.

---

# 7. Silhouette Priority

Silhouette shall influence Product Subtype only when it forms part of the accepted commercial product name.

Examples

A-Line Kurti

Fit & Flare Dress

Mermaid Gown

Empire Dress

Tiered Dress

Do not create Product Subtypes using silhouette alone unless recognized commercially.

---

# 8. Hybrid Product Rules

Hybrid garments shall use the commercially accepted Product Subtype.

Examples

Lehenga Saree

Cape Lehenga

Jacket Kurta Set

Fusion Kurta Set

Peplum Lehenga

Future hybrid products shall automatically inherit these rules.

---

# 9. Visual Detection Rules

Visual AI may determine Product Subtype only when:

• Excel does not provide Product Subtype.

• Catalog Description does not provide Product Subtype.

• Visual confidence is sufficient.

If confidence is insufficient,

omit Product Subtype.

Never infer unsupported Product Subtypes.

---

# 10. Product Naming Integration

Product Subtype shall be included in the SEO Product Name only when required by the Naming Rules.

Naming hierarchy:

Unique Colour

↓

Colour + Pattern + Work + Fabric + Product Type

Duplicate Colour

↓

Colour + Pattern + Work + Fabric + Product Subtype + Product Type

Still Duplicate

↓

Colour + Pattern + Work + Fabric + Product Subtype + Design Aesthetic + Product Type

When Pattern is Solid, Plain, Self, or Missing:

↓

Colour + Work + Fabric + Product Type

Construction-based Product Types shall replace the standard Product Type whenever they represent the commercial identity of the product.

---

# 11. Style Information Integration

Product Subtype shall appear as the final field in Style Information.

Sequence:

...

Style Type

↓

Design Aesthetic

↓

Category Type

↓

Product Subtype

---

# 12. Validation Rules

Validation Engine shall verify:

• Evidence hierarchy followed

• Product Subtype supported by evidence

• Product Subtype consistent with Product Type

• Product Subtype consistent with Category

• Construction precedence correctly applied

• Hybrid products correctly classified

• No conflicting Product Subtypes

• No hallucinated Product Subtypes

---

# 13. Output Rules

Product Subtype shall be:

Commercially recognizable

Human-readable

SEO friendly

Luxury retail appropriate

Examples

Tiered Lehenga

Ready-to-Wear Saree

Jacket Kurta Set

Cape Gown

Printed Kurta Set

Designer Sherwani

Never output internal identifiers or abbreviations.

---

# 14. Future Compatibility

FCOS shall automatically support future Product Subtypes, construction-based variants, silhouette-based variants, hybrid garments, regional variants, and emerging fashion terminology without requiring architectural changes.
