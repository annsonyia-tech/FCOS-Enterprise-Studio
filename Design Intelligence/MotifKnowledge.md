# FCOS Enterprise
## Motif Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Motif Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe decorative motifs appearing on garments, textiles, and jewellery.

A Motif represents the individual visual design element used within a pattern or decorative composition.

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Motif only when higher-priority evidence is unavailable.

---

# Definition

A Motif is a single decorative design element.

Examples

✔ Paisley

✔ Peacock

✔ Lotus

✔ Buti

✔ Elephant

NOT

✘ Floral Print

✘ Bandhani Print

✘ Zari Embroidery

---

# Motif Categories

## Floral Motifs

Rose

Lotus

Sunflower

Marigold

Lily

Tulip

Jasmine

Orchid

Cherry Blossom

Daisy

Floral Vine

Leaf

Palm Leaf

Fern

Lotus Bud

Lotus Vine

---

## Paisley Motifs

Paisley

Mango Paisley

Mini Paisley

Paisley Vine

Paisley Buta

---

## Nature Motifs

Leaf

Tree

Tree of Life

Vine

Branch

Cloud

Wave

Rain Drop

Mountain

Feather

Butterfly

Dragonfly

Bee

---

## Animal Motifs

Peacock

Elephant

Horse

Camel

Deer

Fish

Swan

Parrot

Lion

Tiger

Bull

Cow

Bird

Phoenix

---

## Temple & Religious Motifs

Temple

Kalash

Diya

Conch

Bell

Om

Swastik

Mandala

Yantra

Shankh

---

## Geometric Motifs

Diamond

Circle

Triangle

Hexagon

Chevron

Lattice

Grid

Star

Polygon

Honeycomb

---

## Heritage Motifs

Buti

Buta

Jaal

Jharokha

Mughal Motif

Rajput Motif

Persian Motif

Royal Crest

Coin

Ashrafi

Annam

Mayil

Rudraksha

Temple Coin

---

## Contemporary Motifs

Abstract

Brush Stroke

Minimal Icon

Typography

Art Deco

Modern Graphic

Line Art

---

## Children's Motifs

Stars

Moon

Cloud

Rainbow

Heart

Cartoon Animal

Toy

Balloon

Rocket

Dinosaur

---

# Motif Detection Rules

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

# Motif Normalization

Supplier wording

Peacock Design

↓

Peacock Motif

Lotus Design

↓

Lotus Motif

Paisley Design

↓

Paisley Motif

Floral Vine Design

↓

Floral Vine Motif

---

# Motif vs Pattern

Correct

Pattern Detail:
Floral Print

Motif:
Lotus

Incorrect

Pattern Detail:
Lotus

---

# Motif vs Work

Correct

Motif:
Peacock

Work Detail:
Zari Embroidery

Incorrect

Work Detail:
Peacock

---

# Multiple Motif Rule

If multiple motifs exist

List the primary commercial motif first.

Example

Paisley, Floral Vine

Example

Peacock, Lotus

Example

Elephant, Temple

---

# Style Information Rule

Motif is NOT part of the standard Style Information.

Include Motif only when:

• Excel explicitly provides it

OR

• Catalog Description explicitly provides it

OR

• The motif is a major commercial selling feature.

Otherwise

↓

Store internally.

---

# Description Rule

Use Motif naturally in the editorial description.

Example

"...adorned with graceful lotus motifs inspired by traditional Indian artistry."

Example

"...accentuated with intricately woven paisley motifs that enhance its regal character."

---

# Confidence Rule

High Confidence

↓

Output Motif.

Medium Confidence

↓

Output only if not contradicted.

Low Confidence

↓

Omit Motif.

Never invent motifs.

---

# Universal Recognition Rule

FCOS shall recognize any commercially accepted decorative motif supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown motifs shall be normalized using the closest accepted commercial fashion terminology.

---

# Examples
Example 1

Pattern:
Bandhani Print

Motif:
Buti

Work:
Mirror Work

---

Example 2

Pattern:
Floral Print

Motif:
Lotus

Work:
Thread Embroidery

---

Example 3

Pattern:
Paisley Woven

Motif:
Paisley

Work:
Zari Embroidery

---

Example 4

Pattern:
Ajrakh Print

Motif:
Geometric

Work:
None

---

Example 5

Pattern:
Solid

Motif:
Peacock

Work:
Stone Embroidery

Enterprise Recommendations (FCOS v2.2)

To make MotifKnowledge.md truly enterprise-grade, I recommend adding these five sections:

1. Motif by Product Type ⭐⭐⭐⭐⭐
Product Type	Common Motifs
Saree	Paisley, Lotus, Peacock, Buti, Jaal
Lehenga	Floral, Paisley, Peacock, Temple
Kurti	Floral, Leaf, Geometric
Sherwani	Paisley, Mughal, Royal Crest
Jewellery	Peacock, Lotus, Temple, Mango, Coin
2. Regional Motif Intelligence ⭐⭐⭐⭐⭐

Map motifs to regional textile traditions:

Banarasi → Kalga, Bel, Buta, Jaal
Kanchipuram → Peacock, Temple, Rudraksha, Mango
Patola → Elephant, Parrot, Floral
Kalamkari → Tree of Life, Peacock, Mythological
Ajrakh → Geometric, Star, Floral
3. Motif Placement ⭐⭐⭐⭐☆

Record where motifs appear:

All Over
Border
Pallu
Yoke
Sleeve
Hem
Neckline
Panel
Center Front
4. Motif Scale ⭐⭐⭐⭐☆

Support commercial descriptions such as:

Micro Motif
Small Motif
Medium Motif
Large Motif
Oversized Motif
5. Motif Density ⭐⭐⭐⭐⭐

Classify motif distribution:

Scattered
Sparse
Repeated
Dense
All-Over
Placement Design

Enterprise Recommendations (FCOS v2.2)

To make MotifKnowledge.md truly enterprise-grade, I recommend adding these five sections:

1. Motif by Product Type ⭐⭐⭐⭐⭐
Product Type	Common Motifs
Saree	Paisley, Lotus, Peacock, Buti, Jaal
Lehenga	Floral, Paisley, Peacock, Temple
Kurti	Floral, Leaf, Geometric
Sherwani	Paisley, Mughal, Royal Crest
Jewellery	Peacock, Lotus, Temple, Mango, Coin
2. Regional Motif Intelligence ⭐⭐⭐⭐⭐

Map motifs to regional textile traditions:

Banarasi → Kalga, Bel, Buta, Jaal
Kanchipuram → Peacock, Temple, Rudraksha, Mango
Patola → Elephant, Parrot, Floral
Kalamkari → Tree of Life, Peacock, Mythological
Ajrakh → Geometric, Star, Floral
3. Motif Placement ⭐⭐⭐⭐☆

Record where motifs appear:

All Over
Border
Pallu
Yoke
Sleeve
Hem
Neckline
Panel
Center Front
4. Motif Scale ⭐⭐⭐⭐☆

Support commercial descriptions such as:

Micro Motif
Small Motif
Medium Motif
Large Motif
Oversized Motif
5. Motif Density ⭐⭐⭐⭐⭐

Classify motif distribution:

Scattered
Sparse
Repeated
Dense
All-Over
Placement Design
