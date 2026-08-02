# FCOS AI Studio Enterprise
# Category Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Category Intelligence Engine

---

# 1. Purpose

Defines all rules for determining, validating, normalizing, and outputting the commercial product category within FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden.

---

# 2. Evidence Hierarchy

Category shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Category Rules

Every product processed by FCOS shall belong to one commercial category.

Examples

Women's Wear

Men's Wear

Kids' Wear

Jewellery

Future categories shall automatically inherit these rules.

---

# 4. Category Determination

FCOS shall determine the commercial category before determining Product Type or Product Subtype.

Category is the parent classification.

Product Type is the commercial product.

Product Subtype is the specialized product.

Example

Category

Women's Wear

↓

Product Type

Lehenga

↓

Product Subtype

Tiered Designer Lehenga

---

# 5. Women's Wear Categories

Examples

Saree

Lehenga

Salwar Suit

Kurta Set

Kurti

Dress

Gown

Co-Ord Set

Top

Bottom

Jumpsuit

Kaftan

Indo-Western

Fusion Wear

Future women's categories shall inherit these rules.

---

# 6. Men's Wear Categories

Examples

Kurta

Kurta Pajama

Sherwani

Bandhgala

Nehru Jacket

Waistcoat

Shirt

Trousers

Dhoti

Indo-Western

Future men's categories shall inherit these rules.

---

# 7. Kids' Wear Categories

Examples

Girls' Lehenga

Girls' Gown

Girls' Dress

Girls' Kurta Set

Boys' Kurta Pajama

Boys' Sherwani

Boys' Indo-Western

Future kids' categories shall inherit these rules.

---

# 8. Jewellery Categories

Examples

Necklace

Necklace Set

Pendant

Earrings

Jhumka

Chandbali

Bracelet

Ring

Anklet

Temple Jewellery

Bridal Jewellery

Future jewellery categories shall inherit these rules.

---

# 9. Category Validation

Validation Engine shall verify:

• Correct category selected

• Category supported by evidence

• Category consistent with Product Type

• Category consistent with Product Subtype

• No conflicting categories

---

# 10. Style Information Rules

Category Type shall always appear near the end of Style Information.

Sequence

...

Style Type

↓

Design Aesthetic

↓

Category Type

↓

Product Subtype

---

# 11. Output Rules

Category shall be human-readable.

Examples

Designer Lehenga

Printed Saree

Kurta Set

Bridal Jewellery Set

Never output internal category codes.

---

# 12. Future Compatibility

FCOS shall automatically support future commercial product categories without requiring architectural changes.
