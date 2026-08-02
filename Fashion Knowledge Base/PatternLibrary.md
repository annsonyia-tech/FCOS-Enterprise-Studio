# FCOS Enterprise Studio

# Pattern Library

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Pattern Library defines the universal taxonomy for identifying and classifying garment patterns across all supported product categories.

It serves as the authoritative Fashion Knowledge Base for Pattern Recognition and shall be used by the Fashion Intelligence Engine whenever Pattern Detail is required.

This specification governs only Pattern Recognition.

---

# Evidence Hierarchy

Pattern recognition shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Pattern shall never be visually inferred when Excel or Catalog Description explicitly specifies it.

---

# Pattern Recognition Principles

FCOS shall identify the dominant visible pattern of the garment.

If multiple patterns exist, classify using the most visually dominant pattern unless otherwise specified in the catalog.

Only one primary Pattern Detail shall be emitted.

---

# Pattern Categories

## Solid

Description

No visible print, weave, motif or decorative pattern.

Examples

- Solid
- Plain
- Self
- Self Texture

SEO Rule

If Pattern is:

- Solid
- Plain
- Self
- Missing

Do NOT include Pattern in the Product Name.

---

## Floral

Examples

- Floral Printed
- Floral Embroidered
- Floral Woven
- Botanical Printed
- Rose Motif
- Tropical Floral

---

## Paisley

Examples

- Paisley Printed
- Paisley Woven
- Paisley Embroidered

---

## Heritage Motif

Examples

- Heritage Motif Embroidered
- Traditional Motif
- Temple Motif
- Royal Motif
- Mughal Motif

---

## Geometric

Examples

- Geometric Printed
- Geometric Woven
- Geometric Embroidered

---

## Abstract

Examples

- Abstract Printed
- Abstract Digital Print
- Contemporary Abstract

---

## Striped

Examples

- Vertical Stripes
- Horizontal Stripes
- Pin Stripes
- Multi Stripe

---

## Checked

Examples

- Checks
- Windowpane Checks
- Plaid
- Tartan
- Gingham

---

## Polka Dot

Examples

- Polka Dot Printed
- Micro Dot
- Large Dot

---

## Bandhani

Examples

- Bandhani Printed
- Bandhani Dyed
- Traditional Bandhani

---

## Leheriya

Examples

- Leheriya Printed
- Leheriya Dyed

---

## Ajrakh

Examples

- Ajrakh Printed
- Traditional Ajrakh

---

## Kalamkari

Examples

- Kalamkari Printed
- Kalamkari Hand Painted

---

## Ikat

Examples

- Ikat Woven
- Ikat Printed

---

## Block Print

Examples

- Hand Block Printed
- Wooden Block Print

---

## Digital Print

Examples

- Digital Printed
- Placement Print

---

## Foil Print

Examples

- Gold Foil Print
- Silver Foil Print
- Metallic Foil Print

---

## Animal Print

Examples

- Leopard Print
- Zebra Print
- Snake Print

---

## Ethnic Print

Examples

- Ethnic Printed
- Tribal Print
- Folk Print

---

## Botanical

Examples

- Leaf Printed
- Botanical Print
- Nature Inspired Print

---

## Ombre

Examples

- Ombre Dyed
- Gradient Printed

---

## Tie-Dye

Examples

- Tie Dye
- Shibori
- Resist Dye

---

## Chevron

Examples

- Chevron Printed
- Chevron Woven

---

## Marble

Examples

- Marble Printed
- Stone Effect Print

---

## Brocade

Examples

- Brocade Woven
- Jacquard Brocade

---

## Jacquard

Examples

- Jacquard Woven
- Textured Jacquard

---

## Textured

Examples

- Self Textured
- Woven Texture
- Crinkle Texture

---

# Pattern Classification Rules

When a pattern is supported by Excel or Catalog Description, use the documented value.

When unavailable, Visual AI may classify the dominant visible pattern.

Fashion Intelligence may refine terminology but shall never contradict higher-priority evidence.

---

# Multiple Patterns

If multiple patterns exist:

Determine the dominant commercial pattern.

Example

Floral print with zari embroidery

Pattern Detail

Floral Printed

Work Detail

Zari Embroidery

Pattern and Work shall never be merged.

---

# Pattern vs Work

Pattern defines the visual surface design.

Work defines decorative craftsmanship.

Examples

Pattern

Floral Printed

Work

Mirror Work

Correct

Pattern Detail: Floral Printed

Work Detail: Mirror Work

Incorrect

Pattern Detail: Floral Mirror Work

---

# Pattern Validation

Before output generation FCOS shall verify:

✓ Pattern supported by Evidence Hierarchy

✓ Pattern terminology standardized

✓ Pattern not duplicated in Work Detail

✓ Pattern correctly separated from Fabric

✓ Pattern omitted from Product Name when Solid, Plain, Self or Missing

✓ Pattern consistent across the catalog

---

# Future Extensibility

The Pattern Library shall support new pattern classifications without modifying the core architecture.

Examples include:

- Contemporary Designer Prints
- AI-Generated Textile Patterns
- Regional Weaving Motifs
- International Fashion Prints
- Future Commercial Pattern Types

All future patterns shall inherit the same classification framework.

---

# Related Specifications

- EvidenceHierarchy.md
- ProductNaming.md
- StyleInformation.md
- DescriptionEngine.md
- Validation.md
