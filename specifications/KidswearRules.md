# FCOS AI Studio Enterprise
# Kidswear Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Fashion Intelligence Engine

---

# 1. Purpose

This document defines all processing, classification, measurement, styling, and output rules specific to Kids' Wear within FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden by this document.

---

# 2. Scope

FCOS shall support and classify all current and future Kids' Wear products using the Enterprise Evidence Hierarchy.

Supported Categories include but are not limited to:

## Boys' Wear

- Kurta
- Kurta Pajama
- Kurta Set
- Sherwani
- Indo-Western Set
- Jacket Kurta Set
- Dhoti Kurta Set
- Pathani Suit
- Shirt
- Shirt & Pant Set
- Waistcoat Set
- Blazer Set
- Co-Ord Set
- T-Shirt
- Sweatshirt
- Hoodie
- Jacket
- Jeans
- Trousers
- Shorts

## Girls' Wear

- Lehenga Choli
- Lehenga Kurti
- Lehenga Set
- Gown
- Frock
- Dress
- Anarkali
- Salwar Suit
- Kurta Set
- Sharara Set
- Gharara Set
- Palazzo Set
- Co-Ord Set
- Skirt Set
- Kaftan
- Tunic
- Jacket Set
- Cape Set
- Indo-Western Set

Future Kids' Wear categories shall automatically inherit FCOS universal architecture.

---

# 3. Evidence Hierarchy

All Kids' Wear attributes shall be resolved using:

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 4. Product Classification

FCOS shall independently identify:

- Product Type
- Product Subtype
- Construction
- Silhouette
- Garment Components
- Layering
- Closure Style

Visual garment construction shall always take precedence over generic naming.

---

# 5. Size Rules

Body Size Label

Chest Size

Examples

Chest Size: 20–22 Inches

Chest Size: 22–24 Inches

Chest Size: 24–26 Inches

Chest Size: 26–28 Inches

Chest Size: 28–30 Inches

Convert letter sizes to standardized chest measurements whenever reliable mappings are available.

---

# 6. Colour Rules

Colour shall follow:

Excel
↓

Catalog Description
↓

Visual AI

Visual AI shall never override an Excel colour.

---

# 7. Fabric Rules

Maintain component-specific fabrics.

Examples

Kurta Fabric

Shirt Fabric

Jacket Fabric

Choli Fabric

Lehenga Fabric

Dress Fabric

Bottom Fabric

Pant Fabric

Dupatta Fabric

Inner Fabric

Never merge multiple fabrics.

---

# 8. Garment Component Detection

FCOS shall independently detect:

## Boys

Kurta

Shirt

Jacket

Waistcoat

Sherwani

Pant

Pajama

Dhoti

Shorts

Inner Layer

## Girls

Choli

Kurti

Top

Lehenga

Skirt

Dress

Gown

Palazzo

Sharara

Gharara

Pant

Dupatta

Cape

Jacket

Each component shall retain independent fabric and length attributes.

---

# 9. Construction Detection

Examples include:

A-Line

Straight

Gathered

Tiered

Panelled

Empire

Peplum

Kaftan

Cape Attached

Jacket Layered

Asymmetric

High-Low

Circular

Angrakha

Construction describes garment engineering rather than styling.

---

# 10. Silhouette Detection

Examples include:

Straight

Flared

Tiered Flared

Fit & Flare

Circular

Relaxed

Slim

Regular

Oversized

Mermaid

Silhouette describes how the garment falls on the body.

---

# 11. Fit Detection

Include Fit only when explicitly provided or confidently inferred without contradicting visible evidence.

Examples

Regular Fit

Relaxed Fit

Slim Fit

Comfort Fit

Tailored Fit

Otherwise omit.

---

# 12. Sleeve Detection

Detect all sleeve styles.

Examples

Sleeveless

Cap Sleeves

Short Sleeves

Half Sleeves

Elbow Sleeves

Three-Quarter Sleeves

Full Sleeves

Puff Sleeves

Bell Sleeves

Cape Sleeves

Sleeve Style shall always end with "Sleeves".

Never output generic sleeve names.

---

# 13. Neck Detection

Examples

Round Neck

Square Neck

Sweetheart Neck

Boat Neck

V Neck

Mandarin Collar

Shirt Collar

Peter Pan Collar

Halter Neck

Omit if unsupported.

---

# 14. Pattern & Work Detection

Pattern Examples

Printed

Floral Printed

Paisley Printed

Abstract Printed

Bandhani Printed

Striped

Checked

Self

Plain

Solid

Work Examples

Thread Embroidery

Resham Embroidery

Mirror Work

Sequin Embroidery

Foil Print

Digital Print

Zari Embroidery

Applique Work

Only include supported evidence.

---

# 15. Visual Garment Measurement Rules

## Measurement Hierarchy

Excel

↓

Catalog Description

↓

Visual AI

---

## Reference Model Heights

Girls' Wear

4 ft (122 cm)

Boys' Wear

4 ft 2 in (127 cm)

Visual garment measurement shall always be based on these standard reference heights.

---

## Components to Measure

### Girls

Choli Length

Kurti Length

Top Length

Dress Length

Gown Length

Lehenga Length

Skirt Length

Palazzo Length

Sharara Length

Gharara Length

Pant Length

Jacket Length

Cape Length

### Boys

Kurta Length

Shirt Length

Sherwani Length

Jacket Length

Waistcoat Length

Pant Length

Pajama Length

Dhoti Length

Shorts Length

Each garment component shall be measured independently.

---

## Length Normalization

All apparel component lengths shall be displayed as standardized 2-inch ranges.

Examples

12 Inches

↓

10–12 Inches

18 Inches

↓

16–18 Inches

24 Inches

↓

22–24 Inches

30 Inches

↓

28–30 Inches

34 Inches

↓

32–34 Inches

---

## Measurement Exceptions

Retain exact catalog values for:

Dupatta Length

Fabric Cut Lengths

Blouse Piece Length

---

## Confidence Rule

Generate visual measurements only when confidence is sufficient.

If confidence is insufficient and no higher-priority evidence exists, omit the attribute.

Never invent measurements.

---

# 16. Occasion Detection

Examples

Daily Wear

Birthday Party

Festive Wear

Wedding

Reception

Haldi

Mehendi

Traditional Ceremony

Family Function

Cultural Event

---

# 17. Style Type

Examples

Playful Elegance

Festive Charm

Princess Grace

Royal Heritage

Contemporary Chic

Minimal Luxe

Traditional Elegance

Modern Ethnic

---

# 18. Design Aesthetic

Examples

Royal Heritage

Floral Romance

Modern Glamour

Minimal Elegance

Artisan Craft

Contemporary Minimalism

Vintage Revival

Playful Luxury

---

# 19. Category Type Examples

## Boys

Designer Kurta Set

Kurta Pajama

Sherwani

Jacket Kurta Set

Indo-Western Set

Shirt & Pant Set

## Girls

Designer Lehenga

Lehenga Choli

Designer Dress

Designer Gown

Sharara Set

Anarkali Suit

Kurta Set

Co-Ord Set

---

# 20. Ready-to-Wear Classification

Automatically determine:

Ready to Wear

Semi-Stitched

Customized

Made to Measure

Unstitched

using the FCOS Evidence Hierarchy.

---

# 21. Kidswear Output Rules

The Universal FCOS Output Specification shall apply.

Kidswear outputs shall generate:

- SEO Product Name
- Universal Style Information
- Individual Description
- Care Instruction
- Delivery Information
- Validation Report
- Excel Output

---

# 22. Kidswear Validation Rules

The Validation Engine shall verify:

- 5–8 word SEO Product Name
- Unique Product Name
- Correct Product Classification
- Correct Component Detection
- Correct Chest Size
- Correct Length Normalization
- Correct Style Information Order
- 150–180 word Individual Description
- Valid HTML Structure
- No Hallucinated Attributes
- 1:1 Image-to-Row Mapping
- Zero Validation Errors
