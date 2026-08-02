# FCOS Enterprise
## Fashion Pattern Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Fashion Pattern Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, and classify garment patterns using the FCOS Evidence Hierarchy.

Evidence Priority

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may only determine Pattern Detail when higher-priority evidence is unavailable.

Pattern Classification Principles
A Pattern describes the dominant visual surface design of the garment.

A Pattern is different from Work Detail.

Pattern
↓

The visual design printed, woven, dyed, knitted or embroidered across the fabric.

Examples

Floral Print

Paisley Print

Bandhani

Ajrakh

Ikat

Checks

Stripes

Polka Dot

Geometric

Abstract

Animal Print

Heritage Motif

Ethnic Motif

Botanical

Digital Print

Ombre

Self Texture

Solid

Plain
Pattern Categories
Floral
Floral

Floral Print

Floral Digital Print

Floral Screen Print

Floral Foil Print

Floral Embroidered

Floral Woven

Floral Block Print

Floral Hand Printed

Floral Buti

Floral Vine

Floral Bouquet
Paisley
Paisley

Paisley Print

Paisley Woven

Paisley Embroidery

Paisley Buta

Paisley Motif
Geometric
Geometric

Chevron

Diamond

Hexagon

Triangle

Square

Abstract Geometry

Linear Geometry
Ethnic
Ajrakh

Bandhani

Bandhej

Leheriya

Ikat

Kalamkari

Bagru

Dabu

Batik

Warli

Madhubani

Pattachitra

Block Print

Sanganeri

Jaipuri Print

Kutchi Motif
Traditional Motifs
Peacock

Elephant

Temple

Mango

Lotus

Tree of Life

Paisley

Buti

Buta

Jaal

Mandala

Coin Motif

Ashrafi

Heritage Motif
Contemporary
Abstract

Brush Stroke

Colour Block

Tie Dye

Marble

Watercolour

Ink Splash

Graphic Print

Typography

Minimal Print

Gradient

Ombre
Surface
Solid

Plain

Self

Self Texture

Jacquard

Textured

Crinkle

Pleated Texture

Quilted

Ribbed

Cable Knit
Pattern Detection Rules
Use Excel first.

If unavailable

↓

Use Catalog Description.

If unavailable

↓

Use Visual AI.

If unavailable

↓

Use Fashion Reasoning.

Never overwrite Excel.
Pattern Normalization

Normalize supplier wording.

Examples

Bandhani Printed

↓

Bandhani Print

Floral Digital Printed

↓

Floral Digital Print

Paisley Woven Design

↓

Paisley Woven

Heritage Embroidery

↓

Heritage Motif Embroidered
Pattern + Work Separation

Never confuse Pattern with Work.

Example

Pattern

Bandhani Print

Work

Mirror Work

Correct Style Information

Pattern Detail

Bandhani Print

Work Detail

Mirror Work

NOT

Pattern Detail

Mirror Work
SEO Rules

For Product Name

If Pattern

=

Solid

Plain

Self

Missing

↓

Do NOT include Pattern.

Example

Black Solid Silk Saree

↓

Black Silk Saree
Style Information Rule

Always output

Pattern Detail

Bandhani Print

NOT

Bandhani

Always include the production technique when known.

Pattern Confidence Rule

If confidence is below threshold

↓

Omit Pattern Detail.

Never guess.

Future-Proof Rule

FCOS shall recognize any commercially valid textile pattern supported by:

Excel

Catalog

Visual AI

Fashion Reasoning

Unknown patterns shall be classified using the closest accepted commercial terminology.


---

# Pattern vs Work Examples

| Pattern Detail | Work Detail |
|---------------|------------|
| Bandhani Print | Mirror Work |
| Floral Print | Zari Embroidery |
| Paisley Woven | Resham Embroidery |
| Ajrakh Print | Thread Embroidery |
| Ikat Woven | Sequin Work |
| Heritage Motif Embroidered | Gota Patti |
| Abstract Digital Print | Foil Print |

---

## Enterprise Recommendation

This is only **one** of the FCOS knowledge engines. I recommend creating a matching knowledge file for each major fashion concept:

- `FabricKnowledge.md`
- `ConstructionKnowledge.md`
- `SilhouetteKnowledge.md`
- `SleeveKnowledge.md`
- `NeckKnowledge.md`
- `WorkKnowledge.md`
- `OccasionKnowledge.md`
- `StyleTypeKnowledge.md`
- `DesignAestheticKnowledge.md`
- `ProductTypeKnowledge.md`
- `ProductSubtypeKnowledge.md`

Together, these files form the **Universal Fashion Knowledge Base (UFKB)** that powers FCOS Enterprise, while your master prompt simply orchestrates how the knowledge is applied.
