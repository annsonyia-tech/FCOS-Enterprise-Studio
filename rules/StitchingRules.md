# FCOS AI Studio Enterprise
# Stitching Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Stitching Intelligence Engine

---

# 1. Purpose

Defines all stitching classification, normalization, validation, and output rules used by FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden.

---

# 2. Evidence Hierarchy

Stitching Status shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Stitching Classification

FCOS shall classify every applicable apparel product into one of the following categories:

Ready To Wear

Semi-Stitched

Unstitched

Customizable

Made To Measure

Stitching Available

Customized

Pre-Stitched

Future stitching categories shall automatically inherit these rules.

---

# 4. Category Applicability

Stitching Status applies only to apparel products.

Examples

Women's Wear

Men's Wear

Kids' Wear

Indo-Western

Fusion Wear

Western Wear

Do not apply Stitching Status to:

Jewellery

Accessories

Footwear

Scarves

Belts

Watches

Bags

---

# 5. Ready-To-Wear Rules

If the catalog indicates:

Readymade

Ready To Wear

RTW

Fully Stitched

Pre-Stitched

Normalize to:

Ready To Wear

---

# 6. Semi-Stitched Rules

If the catalog indicates:

Semi-Stitched

Partially Stitched

Semi Ready

Normalize to:

Semi-Stitched

---

# 7. Unstitched Rules

If the catalog indicates:

Unstitched

Dress Material

Fabric Only

Normalize to:

Unstitched

---

# 8. Customized Rules

If the catalog indicates:

Made To Measure

Custom Stitching

Customized

Tailoring Included

Normalize to:

Customizable

---

# 9. Unknown Stitching Status

If no reliable evidence exists,

omit Stitching Status.

Never infer stitching status without supporting evidence.

---

# 10. Style Information Rules

Include Stitching Status only when applicable.

Correct Position:

Occasion

↓

Stitching Status

↓

Style Type

---

# 11. Product Description Rules

Ready To Wear

Use:

"Designed for a perfect ready-to-wear experience and delivered worldwide in 7–10 days."

---

Semi-Stitched

Use:

"Custom-stitched to your exact measurements and delivered worldwide in 7–10 days."

---

Unstitched

Use:

"Custom-stitched to your exact measurements and delivered worldwide in 7–10 days."

---

Customizable

Use:

"Custom-stitched to your exact measurements and delivered worldwide in 7–10 days."

---

Jewellery

Do not use stitching text.

Use Jewellery Delivery Rules.

---

# 12. Care Instruction Rules

Ready To Wear

Dry clean only...

Customizable

Dry clean only...

Semi-Stitched

Dry clean only...

Unstitched

Dry clean only...

Jewellery follows Jewellery Rules.

---

# 13. Validation Rules

Validation Engine shall verify:

• Correct evidence hierarchy

• Correct normalization

• Apparel only

• Correct delivery text

• Correct care instruction

• Style Information placement

• No hallucinated stitching status

---

# 14. Output Rules

Style Information

Occasion

↓

Stitching Status

↓

Style Type

↓

Design Aesthetic

↓

Category Type

---

# 15. Future Compatibility

FCOS shall automatically support future stitching classifications without requiring architectural changes.
