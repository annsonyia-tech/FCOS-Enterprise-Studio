# FCOS AI Studio Enterprise
# Menswear Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Fashion Intelligence Engine

---

# 1. Purpose

This document defines all processing, classification, measurement, and output rules specific to Men's Wear within FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden by this document.

---

# 2. Scope

FCOS shall support and classify all current and future Men's Wear products using the Enterprise Evidence Hierarchy.

Supported categories include, but are not limited to:

Traditional Wear

- Kurta
- Kurta Pajama
- Kurta Set
- Sherwani
- Achkan
- Bandhgala
- Pathani Suit
- Dhoti Kurta
- Jacket Kurta Set
- Waistcoat Kurta Set
- Angrakha Kurta

Indo-Western

- Indo-Western Sherwani
- Indo-Western Kurta
- Layered Kurta
- Asymmetric Kurta
- Draped Kurta
- Jacket Kurta
- Cape Kurta

Western Wear

- Shirt
- T-Shirt
- Polo T-Shirt
- Sweatshirt
- Hoodie
- Jacket
- Blazer
- Waistcoat
- Suit
- Tuxedo

Bottom Wear

- Pajama
- Churidar
- Pant
- Trousers
- Jeans
- Cargo Pants
- Dhoti
- Salwar

Future menswear product types shall automatically inherit FCOS universal architecture.

---

# 3. Evidence Hierarchy

All menswear attributes shall be resolved using:

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Higher-priority evidence shall never be overwritten by lower-priority evidence.

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

Visual construction shall always take precedence over generic naming.

---

# 5. Body Size Rules

Body Size Label

Chest Size

Examples

Chest Size: 38–44 Inches

Chest Size: 40–46 Inches

Default

38–46 Inches

Letter sizes shall be converted to standardized measurement ranges whenever reliable mappings are available.

---

# 6. Colour Rules

Colour shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

Visual AI shall never override a colour explicitly provided in the Excel or Catalog Description.

---

# 7. Fabric Rules

Component-specific fabrics shall always be maintained.

Examples

Kurta Fabric

Jacket Fabric

Waistcoat Fabric

Pant Fabric

Pajama Fabric

Dhoti Fabric

Inner Fabric

Never merge multiple fabrics into a single field.

---

# 8. Garment Component Detection

FCOS shall independently detect:

- Kurta
- Jacket
- Waistcoat
- Shirt
- Blazer
- Pant
- Pajama
- Churidar
- Dhoti
- Salwar
- Inner Layer
- Scarf (when supplied)

Each component shall retain its own fabric and length information.

---

# 9. Construction Detection

Examples include:

- Straight
- Panelled
- Angrakha
- Asymmetric
- Gathered
- Layered
- Jacket Layered
- Cape Attached
- Front Open
- Side Slit
- High-Low
- Structured

Construction describes structural engineering rather than visual styling.

---

# 10. Silhouette Detection

Examples include:

- Straight
- Slim
- Regular
- Relaxed
- Tailored
- Oversized
- Circular
- Flared

Silhouette describes how the garment falls on the body.

---

# 11. Fit Detection

Include Fit only when explicitly provided or confidently inferred without contradicting visible evidence.

Examples:

- Slim Fit
- Regular Fit
- Relaxed Fit
- Tailored Fit
- Comfort Fit

Otherwise omit.

---

# 12. Sleeve Detection

FCOS shall detect all sleeve styles.

Examples:

- Half Sleeves
- Elbow Sleeves
- Three-Quarter Sleeves
- Full Sleeves
- Roll-Up Sleeves
- Cuffed Sleeves
- Sleeveless

Sleeve Style shall always end with "Sleeves".

Never output generic sleeve names.

---

# 13. Neck and Collar Detection

Examples:

- Mandarin Collar
- Band Collar
- Shirt Collar
- Spread Collar
- Camp Collar
- Button Down Collar
- Round Neck
- V Neck
- Henley Neck

Collars and neck styles shall be detected independently where applicable.

---

# 14. Pattern & Work Detection

Examples:

Pattern

- Self
- Plain
- Solid
- Striped
- Checked
- Floral Printed
- Paisley Printed
- Ajrakh Printed
- Bandhani Printed
- Ikat Woven
- Geometric Printed

Work

- Thread Embroidery
- Resham Embroidery
- Zari Embroidery
- Mirror Work
- Machine Embroidery
- Foil Print
- Digital Print
- Sequins

Only include supported evidence.

---

# 15. Visual Garment Measurement Rules

## 15.1 Measurement Hierarchy

Garment lengths shall be determined using:

Excel

↓

Catalog Description

↓

Visual AI

---

## 15.2 Reference Model Height

When Visual AI is required, FCOS shall assume:

**Men = 5 ft 10 in (178 cm)**

This reference shall be used for visual garment measurement.

---

## 15.3 Components to Measure

Upper Garments

- Kurta Length
- Shirt Length
- Jacket Length
- Blazer Length
- Waistcoat Length
- Sherwani Length
- Achkan Length

Lower Garments

- Pant Length
- Pajama Length
- Churidar Length
- Dhoti Length
- Salwar Length

Each component shall be measured independently.

---

## 15.4 Length Normalization

All apparel lengths shall be displayed as standardized 2-inch ranges.

Examples

42 Inches

↓

40–42 Inches

44 Inches

↓

42–44 Inches

51 Inches

↓

50–52 Inches

---

## 15.5 Confidence Rule

Visual measurements shall only be generated when confidence is sufficient.

If confidence is insufficient and no higher-priority evidence exists, omit the attribute.

Never invent measurements.

---

## 15.6 Validation

Validation Engine shall verify:

- Excel values are never overridden.
- Visual measurements follow 2-inch normalization.
- Each garment component is measured independently.

---

# 16. Occasion Detection

Examples

- Casual Wear
- Office Wear
- Festive Wear
- Wedding
- Reception
- Haldi
- Mehendi
- Sangeet
- Cocktail
- Traditional Ceremony

---

# 17. Style Type

Examples

- Contemporary Classic
- Modern Ethnic
- Heritage Elegance
- Festive Luxury
- Minimal Luxe
- Royal Heritage
- Indo-Western Fusion

---

# 18. Design Aesthetic

Examples

- Regal Heritage
- Contemporary Minimalism
- Royal Opulence
- Artisan Craft
- Modern Glamour
- Timeless Elegance
- Vintage Revival

---

# 19. Category Type Examples

Examples

- Designer Kurta
- Kurta Pajama
- Designer Kurta Set
- Sherwani
- Achkan
- Bandhgala
- Jacket Kurta Set
- Indo-Western Sherwani
- Waistcoat Kurta Set
- Casual Shirt
- Formal Shirt
- Designer Blazer

---

# 20. Ready-to-Wear Classification

Automatically determine:

- Ready to Wear
- Semi-Stitched
- Customized
- Made to Measure
- Unstitched

using the FCOS Evidence Hierarchy.

---

# 21. Menswear Output Rules

The Universal FCOS Output Specification shall apply.

Menswear outputs shall generate:

- SEO Product Name
- Universal Style Information
- Individual Description
- Care Instruction
- Delivery Information
- Validation Report
- Excel Output

---

# 22. Menswear Validation Rules

The Validation Engine shall ensure:

- 5–8 word SEO Product Name
- Unique Product Name
- Correct Product Classification
- Correct Component Detection
- Correct Chest Size
- Correct Length Normalization
- Correct Style Information Order
- 150–180 word Description
- Valid HTML Structure
- No Hallucinated Attributes
- 1:1 Image-to-Row Mapping
- Zero Validation Errors
