# FCOS Enterprise
## Neck Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Neck Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe neckline styles across Women's Wear, Men's Wear, Kids' Wear, Ethnic Wear, Indo-Western Wear, and Western Wear.

Neck Style is independent of:

• Product Type
• Product Subtype
• Construction
• Silhouette
• Sleeve Style
• Pattern
• Work Detail

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Neck Style only when higher-priority evidence is unavailable.

---

# Definition

Neck Style describes the structural opening or collar treatment around the neckline.

Examples

✔ Round Neck
✔ V Neck
✔ Sweetheart Neck
✔ Mandarin Collar

NOT

✘ Deep Neck
✘ Embroidered Neck

These describe depth or decoration rather than the neckline style.

---

# Neck Categories

## Basic Necklines

Round Neck

Crew Neck

Jewel Neck

Boat Neck

Square Neck

V Neck

Deep V Neck

Wide V Neck

U Neck

Scoop Neck

Sweetheart Neck

Queen Anne Neck

Keyhole Neck

Notched Neck

Split Neck

Plunging Neck

---

## Traditional Indian Necklines

Pot Neck

Princess Neck

Paan Neck

Leaf Neck

Closed Round Neck

High Round Neck

---

## Collar Styles

Mandarin Collar

Band Collar

Chinese Collar

Nehru Collar

Shirt Collar

Peter Pan Collar

Stand Collar

Spread Collar

Convertible Collar

Notched Collar

---

## Contemporary Necklines

Off Shoulder

One Shoulder

Asymmetric Neck

Cold Shoulder

Halter Neck

Cowl Neck

Mock Neck

Turtleneck

High Neck

Funnel Neck

Boat High Neck

---

## Designer Necklines

Scalloped Neck

Illusion Neck

Cape Neck

Draped Neck

Layered Neck

Twisted Neck

Wrapped Neck

Cross Over Neck

Envelope Neck

---

## Kids Wear

Round Neck

Boat Neck

Collared Neck

Square Neck

V Neck

Mandarin Collar

---

# Neck Detection Rules

Use Excel.

↓

If unavailable

Use Catalog Description.

↓

If unavailable

Use Visual AI.

↓

If unavailable

Use Fashion Reasoning.

Never overwrite Excel.

---

# Occlusion Rule

Neck Style may be inferred when partially hidden by:

• Dupatta

• Saree Pallu

• Jewellery

• Hair

• Cape

• Jacket

• Shawl

Inference must never contradict visible evidence.

---

# Neck Normalization Rules

Normalize supplier wording.

Examples

Round

↓

Round Neck

Boat

↓

Boat Neck

Sweet Heart

↓

Sweetheart Neck

Chinese Collar

↓

Mandarin Collar

Band Collar

↓

Mandarin Collar

---

# Neck Depth Rule

Neck Style and Neck Depth are different attributes.

Example

Neck Style:
Sweetheart Neck

Front Neck Depth:
6 Inches

Back Neck Depth:
10 Inches

Neck Depth should not be included in Style Information unless the catalog explicitly requires it.

---

# Collar vs Neck Rule

Examples

Mandarin Collar

↓

Neck Style

NOT

Construction

---

# Style Information Rule

Always output

Neck Style:
Square Neck

Never combine with neck depth or decorative details.

---

# Confidence Rule

High Confidence

↓

Output Neck Style.

Medium Confidence

↓

Output only if not contradicted by visible evidence.

Low Confidence

↓

Omit Neck Style.

Never invent neckline styles.

---

# Universal Recognition Rule

FCOS shall recognize any commercially accepted neckline or collar style supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown neck styles shall be normalized using the closest accepted commercial fashion terminology.

---

# Examples

Example 1

Neck Style:
Round Neck

---

Example 2

Neck Style:
Sweetheart Neck

---

Example 3

Neck Style:
Mandarin Collar

---

Example 4

Neck Style:
Boat Neck

---

Example 5

Neck Style:
Halter Neck

Enterprise Recommendations (FCOS v2.2)

I recommend adding these sections to make NeckKnowledge.md even stronger:

1. Neck by Product Type ⭐⭐⭐⭐⭐
Product Type	Common Neck Styles
Saree Blouse	Sweetheart, Square, Boat, Round, V
Choli	Sweetheart, Square, Round
Kurti	Round, V, Boat, Mandarin Collar
Men's Kurta	Mandarin Collar, Band Collar, Round Neck
Sherwani	Mandarin Collar
Gown	Sweetheart, Halter, Off Shoulder, One Shoulder
Kaftan	Boat, V, Round

This improves inference accuracy.

2. Neck & Sleeve Compatibility ⭐⭐⭐⭐☆

Examples:

Neck Style	Common Sleeve Styles
Sweetheart Neck	Puff, Elbow
Boat Neck	Elbow, Full
Mandarin Collar	Full, Roll-Up
Halter Neck	Sleeveless
Off Shoulder	Puff, Bishop
3. Neck & Construction Compatibility ⭐⭐⭐⭐⭐

Examples:

Construction	Common Neck Styles
Angrakha	V Neck, Overlap Neck
Kaftan	Boat Neck, V Neck
Peplum	Sweetheart, Square
Jacket Kurta	Mandarin Collar
Anarkali	Round, Sweetheart, V
4. Neck Decoration Recognition ⭐⭐⭐⭐⭐

Keep this as an internal intelligence attribute, not a mandatory Style Information field.

Examples:

Embroidered Neckline
Mirror Work Neckline
Zari Border Neckline
Lace Neckline
Beaded Neckline
Scalloped Edge
Piped Neckline
Contrast Neck Facing

These details can enrich the editorial description without cluttering Style Information.

5. Neck Depth Intelligence ⭐⭐⭐⭐⭐

If Excel provides:

Front Neck Depth
Back Neck Depth

Store them internally as separate attributes.

Use them for:

Blouse stitching
Custom tailoring
Made-to-measure workflows

Do not include them in the standard Style Information unless you decide to create a dedicated Custom Stitching Profile in FCOS.
