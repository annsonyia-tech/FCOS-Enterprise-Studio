# FCOS Enterprise Studio

# Universal Style Information Specification

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

This specification defines the Universal Style Information Engine used by FCOS Enterprise Studio.

The Style Information Engine standardizes product attributes into a consistent, human-readable, enterprise-grade format suitable for ecommerce catalogs.

It supports Women's Wear, Men's Wear, Kids Wear, Jewellery, Ethnic Wear, Indo-Western Wear, Fusion Wear, Western Wear, and all future product categories.

This specification governs only Style Information generation.

---

# Evidence Hierarchy

All Style Information attributes shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence always overrides lower-priority evidence.

Unsupported attributes shall be omitted.

---

# Universal Style Information Format

Style Information shall always be generated as a single uninterrupted line.

Format:

[BODY_SIZE_LABEL]: [NORMALIZED_SIZE], Colour: [COLOUR], [COMPONENT_FABRICS], [COMPONENT_LENGTHS], Construction: [CONSTRUCTION], Silhouette: [SILHOUETTE], Fit: [FIT], Sleeve Style: [SLEEVE_STYLE], Sleeve Length: [SLEEVE_LENGTH], Neck Style: [NECK_STYLE], Pattern Detail: [PATTERN], Work Detail: [WORK], Occasion: [OCCASION], Stitching Status: [STATUS], Style Type: [STYLE_TYPE], Design Aesthetic: [DESIGN_AESTHETIC], Category Type: [CATEGORY_TYPE], Product Subtype: [PRODUCT_SUBTYPE]

---

# Field Order

The following sequence is mandatory.

1. Size
2. Colour
3. Fabric Details
4. Length Details
5. Construction
6. Silhouette
7. Fit
8. Sleeve Style
9. Sleeve Length
10. Neck Style
11. Pattern Detail
12. Work Detail
13. Occasion
14. Stitching Status
15. Style Type
16. Design Aesthetic
17. Category Type
18. Product Subtype

No field may appear out of order.

---

# Size Rules

Women's Apparel

Use:

Bust Size

Examples

Bust Size: 32–42 Inches

Bust Size: 40–44 Inches

---

Men's Apparel

Use:

Chest Size

Examples

Chest Size: 38–42 Inches

---

Kids Apparel

Use:

Chest Size

---

Non-Fitted Products

Use:

Free Size

Examples

Free Size: 38–42 Inches

Free Size: 38–46 Inches

Sizes shall always follow MeasurementRules.md.

---

# Colour Rules

Colour shall always be taken from:

Excel Workbook

↓

Catalog Description

Visual AI shall only determine Colour when both are unavailable.

Only the primary commercial colour shall be used.

---

# Fabric Rules

List every primary garment component separately.

Examples

Kurta Fabric

Bottom Fabric

Dupatta Fabric

Choli Fabric

Lehenga Fabric

Blouse Fabric

Saree Fabric

Pant Fabric

Jacket Fabric

Cape Fabric

Lining Fabric

Inner Fabric

Only documented fabrics shall be included.

---

# Length Rules

Only applicable garment lengths shall be included.

Examples

Kurta Length

Kurti Length

Dress Length

Blouse Length

Choli Length

Lehenga Length

Pant Length

Palazzo Length

Sleeve Length

Dupatta Length

Saree Length

Length normalization shall follow MeasurementRules.md.

Saree Length and Dupatta Length shall retain the actual catalog measurement.

---

# Construction

Construction describes the structural engineering of the garment.

Examples

A-Line

Tiered

Panelled

Gathered

Empire

Angrakha

Peplum

Kaftan

Jacket Layered

Cape Attached

High-Low

Circular

Asymmetric

Straight Cut

Include only when confidently identified.

---

# Silhouette

Silhouette describes how the garment falls on the body.

Examples

Straight

Flared

Fit & Flare

Mermaid

Relaxed

Slim

Oversized

Circular

Regular

Include only when supported by evidence.

---

# Fit

Fit describes body fitting.

Examples

Regular Fit

Relaxed Fit

Comfort Fit

Tailored Fit

Slim Fit

Oversized Fit

Include only when confidently identified.

---

# Sleeve Style

Examples

Sleeveless

Cap Sleeves

Short Sleeves

Half Sleeves

Elbow Sleeves

Three-Quarter Sleeves

Full Sleeves

Bell Sleeves

Cape Sleeves

Puff Sleeves

Bishop Sleeves

Batwing Sleeves

Balloon Sleeves

Kimono Sleeves

Do not use generic sleeve names.

Always end with "Sleeves" except Sleeveless.

---

# Sleeve Length

Include only when sleeves exist.

Examples

6–8 Inches

8–10 Inches

10–12 Inches

16–18 Inches

20–22 Inches

Never include Sleeve Length for Sleeveless garments.

---

# Neck Style

Examples

Round Neck

V Neck

Square Neck

Boat Neck

Sweetheart Neck

Scoop Neck

Halter Neck

Mandarin Collar

Shirt Collar

Keyhole Neck

Queen Anne Neck

Off Shoulder Neck

Cowl Neck

Do not invent unsupported necklines.

Always end with "Neck" unless the style is a collar.

---

# Pattern Detail

Describe the dominant visual pattern.

Examples

Floral Printed

Paisley Woven

Bandhani Printed

Ajrakh Printed

Heritage Motif Embroidered

Geometric Printed

Abstract Printed

Striped

Checked

Solid

Self Textured

If unavailable, omit.

---

# Work Detail

Describe decorative craftsmanship.

Examples

Zari Embroidery

Resham Embroidery

Mirror Work

Thread Embroidery

Gota Patti

Sequin Embroidery

Beadwork

Stone Work

Cut Dana

Dori Work

Foil Print

Digital Print

If unavailable, omit.

---

# Occasion

Include the most appropriate primary occasion.

Examples

Casual Wear

Office Wear

Daily Wear

Festive Wear

Wedding

Reception

Cocktail

Mehendi

Haldi

Sangeet

Party Wear

Vacation Wear

Temple Wear

---

# Stitching Status

Examples

Ready To Wear

Customizable

Semi-Stitched

Unstitched

Made To Order

Include only when applicable.

---

# Style Type

Style Type defines the fashion identity.

Examples

Heritage Elegance

Contemporary Chic

Modern Classic

Minimal Luxe

Festive Glamour

Artisan Luxury

Bohemian Charm

Timeless Grace

Indo-Western Fusion

---

# Design Aesthetic

Design Aesthetic defines the visual design language.

Examples

Regal Heritage

Modern Glamour

Minimal Elegance

Royal Opulence

Floral Romance

Vintage Revival

Contemporary Minimalism

Artisan Craft

---

# Category Type

Category Type identifies what the customer is purchasing.

Examples

Designer Lehenga

Designer Kurta Set

Printed Saree

Ready-To-Wear Saree

Anarkali Suit

Kaftan Dress

Sherwani

Men's Kurta Pajama

Jewellery Set

---

# Product Subtype

Product Subtype provides additional commercial classification.

Examples

Tiered Lehenga

Panelled Kurta

Straight Kurti

Printed Co-Ord Set

Gathered Dress

Cape Gown

Jacket Kurta Set

Include only when applicable.

---

# Universal Rules

FCOS shall always:

✓ Follow the exact field order.

✓ Generate a single uninterrupted line.

✓ Separate attributes using commas.

✓ Omit unavailable attributes.

✓ Never output NA, Unknown, Blank or placeholders.

✓ Never hallucinate unsupported attributes.

✓ Maintain terminology consistency across the catalog.

✓ Use evidence-based values only.

---

# Example

Bust Size: 40–44 Inches, Colour: Black, Choli Fabric: Kora Cotton, Lehenga Fabric: Kora Cotton, Choli Length: 20–22 Inches, Lehenga Length: 40–42 Inches, Construction: Gathered, Silhouette: Tiered Flared, Sleeve Style: Half Sleeves, Sleeve Length: 8–10 Inches, Neck Style: Square Neck, Pattern Detail: Heritage Motif Embroidered, Work Detail: Kutchi Patch Work, Occasion: Festive Wear, Stitching Status: Ready To Wear, Style Type: Artisan Luxury, Design Aesthetic: Heritage Luxury, Category Type: Designer Lehenga, Product Subtype: Tiered Lehenga

---
# Attribute Confidence Scoring

Construction: Gathered (Confidence: High)

Silhouette: Tiered Flared (Confidence: Medium)

Neck Style: Square Neck (Confidence: High)

Pattern Detail: Heritage Motif Embroidered (Confidence: Low)

---

# Scope

This specification governs only Style Information generation.

Related Specifications

- EvidenceHierarchy.md
- ProductNaming.md
- MeasurementRules.md
- DescriptionEngine.md
- Validation.md
