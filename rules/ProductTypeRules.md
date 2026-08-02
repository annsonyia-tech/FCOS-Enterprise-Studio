# FCOS AI Studio Enterprise
# Product Type Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Product Type Intelligence Engine

---

# 1. Purpose

Defines the rules for determining, validating, normalizing, and outputting the Product Type within FCOS AI Studio Enterprise.

Product Type identifies the primary commercial product that the customer is purchasing.

This document defines processing rules only and contains no product taxonomy.

---

# 2. Evidence Hierarchy

Product Type shall always follow the enterprise evidence hierarchy:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Product Type Rules

Every product shall have exactly one Product Type.

Product Type shall represent the primary commercial product.

Examples

Lehenga

Saree

Kurta Set

Kurti

Dress

Sherwani

Necklace

Ring

Future product types automatically inherit these rules.

---

# 4. Product Type Detection

FCOS shall determine the Product Type before determining Product Subtype.

Processing order:

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
---

# 5. Product Type Priority

Product Type shall describe what the customer is purchasing rather than individual garment components.

Example

Lehenga with Choli and Dupatta

↓

Product Type

Lehenga

NOT

Choli

NOT

Dupatta

---

# 6. Construction Priority

If the product has a visually distinct construction that changes its commercial identity, FCOS shall promote that construction as the Product Type.

Examples

Ready-to-Wear Saree

Lehenga Saree

Cape Gown

Cape Dress

Kaftan Dress

Kaftan Kurta

Jacket Kurta Set

Peplum Kurta

Empire Dress

Angrakha Kurta

Tiered Dress

A-Line Kurti

Layered Lehenga

Shirt Dress

Wrap Dress

Future construction-based products shall automatically inherit this rule.

---

# 7. Hybrid Product Rules

Products containing multiple garment components shall be classified according to the dominant commercial product.

Examples

Lehenga + Choli + Dupatta

↓

Lehenga

Kurta + Pant + Dupatta

↓

Kurta Set

Kurta + Pajama

↓

Kurta Pajama

Sherwani + Churidar

↓

Sherwani

Future hybrid products shall follow the same principle.

---

# 8. Visual Detection Rules

Visual AI may determine Product Type only when:

Excel is unavailable.

Catalog Description is unavailable.

Visual confidence is sufficient.

If confidence is insufficient,

omit Product Type and report a validation error.

Never hallucinate Product Types.

---

# 9. Product Naming Integration

Product Type shall always appear at the end of the SEO Product Name.

Examples

Rani Pink Zari Embroidered Silk Blend Lehenga

Black Kutchi Patch Work Kora Cotton Tiered Lehenga

Green Floral Printed Cotton Kurta Set

Never use generic terms when a specific Product Type is confidently identifiable.

---

# 10. Style Information Integration

Product Type shall not appear inside Style Information.

Style Information shall end with:

Category Type

↓

Product Subtype

Product Type is represented by the Product Name.

---

# 11. Validation Rules

Validation Engine shall verify:

• Evidence hierarchy followed

• Correct Product Type selected

• Construction precedence correctly applied

• Hybrid products correctly classified

• Product Type consistent with Category

• Product Type consistent with Product Subtype

• No conflicting Product Types

• No hallucinated Product Types

---

# 12. Output Rules

Product Type shall be:

Human-readable

Commercially recognizable

SEO friendly

Luxury retail appropriate

Examples

Lehenga

Printed Saree

Kurta Set

Sherwani

Necklace

Never output internal identifiers or abbreviated names.

---

# 13. Future Compatibility

FCOS shall automatically support future Product Types, construction-based products, hybrid garments, and commercial fashion categories without requiring architectural changes.
