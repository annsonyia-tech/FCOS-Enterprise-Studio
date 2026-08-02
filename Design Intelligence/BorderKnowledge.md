# FCOS Enterprise
## Border Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Border Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe decorative borders across Women's Wear, Men's Wear, Kids' Wear, Ethnic Wear, Indo-Western Wear, and Jewellery where applicable.

Border is an independent decorative attribute.

Border is NOT:

• Pattern
• Work Detail
• Fabric
• Construction
• Silhouette

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Border only when higher-priority evidence is unavailable.

---

This deserves its own engine.

Examples

Temple Border

Contrast Border

Zari Border

Scalloped Border

Banarasi Border

Embroidered Border

Mirror Border

Lace Border

Fringed Border

Printed Border

Minimal Border

Heavy Bridal Border

Traditional Border

Kaddi Border

Gap Border

Retta Pettu

Korvai Border

Border is one of the strongest purchase drivers for sarees and lehengas.

---

# Definition

Border describes the decorative finishing or edging applied to garments.

Examples

✔ Temple Border

✔ Contrast Border

✔ Woven Zari Border

✔ Scalloped Border

NOT

✘ Floral Print

✘ Mirror Work

✘ Silk Blend

---

# Border Categories

## Woven Borders

Temple Border

Zari Border

Banarasi Border

Brocade Border

Jacquard Border

Kanchipuram Border

Patola Border

Contrast Woven Border

Self Woven Border

Gold Woven Border

Silver Woven Border

---

## Embroidered Borders

Thread Embroidered Border

Zari Embroidered Border

Resham Embroidered Border

Mirror Border

Sequin Border

Beaded Border

Pearl Border

Stone Border

Cutwork Border

Applique Border

---

## Printed Borders

Printed Border

Floral Border

Paisley Border

Bandhani Border

Ajrakh Border

Digital Printed Border

Block Printed Border

Ethnic Motif Border

---

## Lace Borders

Lace Border

Crochet Lace Border

Scalloped Lace Border

Net Lace Border

Decorative Lace Border

---

## Decorative Borders

Scalloped Border

Fringed Border

Tassel Border

Pom-Pom Border

Piping Border

Contrast Piping

Rolled Edge

Decorative Edge

---

## Traditional Indian Borders

Temple Border

Ganga Jamuna Border

Retta Pettu Border

Korvai Border

Rudraksha Border

Annam Border

Mayil Border

Mango Border

Coin Border

Peacock Border

Elephant Border

Checks Border

Floral Vine Border

---

# Border Placement

Border may appear on

Saree

Dupatta

Lehenga Hem

Skirt Hem

Kurta Hem

Kurti Hem

Sleeves

Neckline

Cape Edge

Jacket Edge

Shawl

Stole

---

# Border Normalization

Normalize supplier wording.

Examples

Temple Design Border

↓

Temple Border

Heavy Zari Border

↓

Zari Border

Contrast Weaving Border

↓

Contrast Woven Border

Golden Border

↓

Gold Woven Border

---

# Border Detection Rules

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

# Border vs Work

Correct

Border:
Temple Border

Work:
Zari Embroidery

Incorrect

Work:
Temple Border

---

# Border vs Pattern

Correct

Pattern:
Bandhani Print

Border:
Temple Border

Incorrect

Pattern:
Temple Border

---

# Multiple Border Rule

If multiple border styles exist

List major border first.

Examples

Temple Border with Contrast Border

Zari Border with Scalloped Edge

Mirror Border with Tassel Finish

---

# Style Information Rule

Border is NOT part of the standard Style Information.

Include Border only when

• Excel explicitly provides it

OR

• Catalog Description explicitly provides it

OR

• The border is a commercially significant design feature.

Otherwise

↓

Store internally.

---

# Description Rule

Use Border naturally in the editorial description.

Example

"...finished with an elegant temple border that enhances the traditional appeal."

---

# Confidence Rule

High Confidence

↓

Output Border.

Medium Confidence

↓

Output only if not contradicted.

Low Confidence

↓

Omit Border.

Never invent border styles.

---

# Universal Recognition Rule

FCOS shall recognize any commercially accepted decorative border supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown border terminology shall be normalized using the closest accepted commercial fashion terminology.

---

# Examples

Example 1

Border:
Temple Border

---

Example 2

Border:
Contrast Woven Border

---

Example 3

Border:
Scalloped Lace Border

---

Example 4

Border:
Mirror Border

---

Example 5

Border:
Retta Pettu Border
