# FCOS Enterprise Studio

# Neck Styles Library

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Neck Styles Library defines the universal taxonomy for identifying neckline styles across all supported fashion categories.

It serves as the authoritative Fashion Knowledge Base for Neck Style Recognition and shall be used by the Fashion Intelligence Engine whenever Neck Style is required.

This specification governs only Neck Style recognition.

---

# Evidence Hierarchy

Neck Style shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Visual AI shall be used only when Neck Style is unavailable in Excel and Catalog Description.

Fashion Intelligence may refine terminology but shall never contradict higher-priority evidence.

---

# Universal Recognition Principles

FCOS shall identify the actual neckline construction rather than generic descriptions.

Neck Style shall describe the visible neckline or collar construction.

Neck depth shall not be included in Neck Style.

Examples

Correct

Sweetheart Neck

Incorrect

Deep Sweetheart Neck

Depth belongs to garment measurements, not Neck Style.

---

# Universal Rules

Every neckline shall end with:

" Neck "

except collar-based constructions.

Examples

Round Neck

Boat Neck

Square Neck

Sweetheart Neck

V Neck

---

Collar-based constructions shall retain their established fashion terminology.

Examples

Mandarin Collar

Shirt Collar

Peter Pan Collar

Band Collar

Not

Mandarin Collar Neck

---

Never output generic values such as:

Regular Neck

Standard Neck

Traditional Neck

Classic Neck

Normal Neck

Basic Neck

---

# Neck Style Taxonomy

## Round Neck

Circular neckline following the base of the neck.

---

## Scoop Neck

Wide rounded neckline extending below the collarbone.

---

## Boat Neck

Wide horizontal neckline extending toward both shoulders.

---

## V Neck

Neckline forming a distinct V shape.

---

## Sweetheart Neck

Heart-shaped neckline following the bust curve.

---

## Square Neck

Straight horizontal neckline with squared corners.

---

## U Neck

Rounded neckline deeper than Round Neck.

---

## Keyhole Neck

Decorative opening below the neckline.

---

## Halter Neck

Neckline secured behind the neck leaving shoulders exposed.

---

## Off-Shoulder Neck

Neckline sitting below both shoulders.

---

## One-Shoulder Neck

Asymmetrical neckline exposing one shoulder.

---

## Queen Anne Neck

Combination of sweetheart front with raised shoulder line.

---

## Cowl Neck

Soft draped neckline.

---

## Jewel Neck

High rounded neckline close to the base of the neck.

---

## Notch Neck

Small front slit integrated into the neckline.

---

## Henley Neck

Rounded neckline with front button placket.

---

## Tie-Up Neck

Neckline incorporating decorative tie closures.

---

## Mandarin Collar

Short standing collar without folded lapels.

---

## Band Collar

Straight standing collar.

---

## Shirt Collar

Classic folded collar construction.

---

## Peter Pan Collar

Rounded flat collar.

---

## Spread Collar

Wide pointed collar.

---

## Convertible Collar

Collar worn open or closed.

---

## Lapel Collar

Tailored collar with visible lapels.

---

## Shawl Collar

Continuous rounded collar.

---

## High Neck

Extended neckline covering most of the neck.

---

## Turtle Neck

Folded high neck extending upward.

---

## Mock Neck

Short high neckline without folding.

---

## Funnel Neck

Structured high neckline widening upward.

---

# Neck Recognition Rules

FCOS shall recognise neck styles even when partially hidden by:

- Dupatta
- Saree Pallu
- Hair
- Jewellery
- Scarf
- Layering
- Pose
- Fabric folds

Only when supported by visible evidence.

If confidence is insufficient,

omit Neck Style.

Never invent.

---

# Composite Neck Recognition

Composite Neck Styles shall only be generated when both constructions are commercially recognised.

Examples

Keyhole Round Neck

Collared V Neck

Shawl Lapel Collar

Notched Mandarin Collar

Never generate artificial combinations.

---

# Dominant Construction Rule

When multiple neckline features are visible:

Priority

1. Explicit Catalog Neck Style

↓

2. Commercially Recognised Composite Neck Style

↓

3. Dominant Neck Construction

↓

4. Decorative Neck Detail

Decorative trims, piping, lace edging, tassels or embellishments shall not alter the Neck Style.

They belong in:

Work Detail

or

Individual Description.

---

# Neckline vs Neck Depth

Neck Style identifies construction.

Neck Depth identifies measurement.

Example

Neck Style

Sweetheart Neck

Front Neck Depth

8 Inches

These shall always remain separate.

---

# Validation Rules

Before output generation FCOS shall verify:

✓ Neck Style supported by Evidence Hierarchy

✓ Correct fashion terminology

✓ No generic Neck Style

✓ Collar terminology preserved

✓ Composite Neck commercially recognised

✓ Decorative details not treated as Neck Style

✓ Consistent terminology throughout the catalog

---

# Future Extensibility

The Neck Styles Library shall support future neckline innovations without modifying the core architecture.

Examples

- Asymmetric Neck
- Illusion Neck
- Plunging Neck
- Designer Signature Necklines
- Couture Necklines

Future neckline styles shall inherit the same recognition framework.

---

---

# Neckline Intelligence Engine

## Purpose

The Neckline Intelligence Engine enables FCOS to recognise, classify, and standardise neckline constructions using a hierarchical fashion taxonomy rather than a flat list of neckline names.

Instead of treating every neckline equally, FCOS shall first identify the neckline family before determining the specific neckline construction.

This mirrors professional fashion design terminology and improves scalability, consistency, and Fashion Intelligence accuracy.

---

# Recognition Workflow

Every neckline shall be classified in the following sequence:

Evidence Hierarchy

↓

Neckline Family

↓

Specific Neck Style

↓

Composite Neckline (if applicable)

↓

Validation

---

# Neckline Families

## 1. Basic Necklines

Description

Classic neckline constructions commonly used across apparel categories.

Examples

- Round Neck
- V Neck
- U Neck
- Scoop Neck
- Square Neck
- Boat Neck

Recognition Rule

Basic Necklines shall be selected only when no higher-order designer or collar construction is present.

---

## 2. Designer Necklines

Description

Fashion-forward neckline constructions characterised by distinctive shaping or visual styling.

Examples

- Sweetheart Neck
- Queen Anne Neck
- Keyhole Neck
- Cowl Neck
- Asymmetric Neck
- Illusion Neck

Recognition Rule

Designer Necklines take precedence over Basic Necklines when both characteristics are visible.

---

## 3. Shoulder-Exposure Necklines

Description

Necklines intentionally exposing one or both shoulders.

Examples

- Off-Shoulder Neck
- One-Shoulder Neck
- Halter Neck
- Bardot Neck

Recognition Rule

Shoulder exposure takes precedence over Basic Necklines.

---

## 4. High Necklines

Description

Necklines extending upward to cover part or all of the neck.

Examples

- High Neck
- Mock Neck
- Turtle Neck
- Funnel Neck

Recognition Rule

High Necklines shall be recognised before evaluating decorative shaping.

---

## 5. Collar-Based Necklines

Description

Necklines incorporating structured collar constructions.

Examples

- Mandarin Collar
- Band Collar
- Shirt Collar
- Peter Pan Collar
- Lapel Collar
- Shawl Collar
- Convertible Collar

Recognition Rule

Collar constructions shall always retain their established fashion terminology and shall never be converted to "... Neck".

Examples

Correct

Mandarin Collar

Incorrect

Mandarin Collar Neck

---

## 6. Composite Necklines

Description

Necklines combining two commercially recognised constructions.

Composite Necklines shall only be generated when both constructions are clearly supported by the Evidence Hierarchy.

Examples

- Keyhole Round Neck
- Collared V Neck
- Mandarin Keyhole Neck
- Shawl Lapel Collar
- Sweetheart Illusion Neck

Composite Necklines shall remain concise, commercially recognised, and human-readable.

---

# Neckline Recognition Priority

When multiple neckline characteristics are detected, FCOS shall classify them in the following order:

1. Explicit Catalog Neckline
2. Collar-Based Neckline
3. Shoulder-Exposure Neckline
4. High Neckline
5. Designer Neckline
6. Basic Neckline
7. Composite Neckline (where applicable)

Higher-priority classifications shall always override lower-priority classifications unless a recognised composite neckline exists.

---

# Composite Neckline Rules

Composite Necklines shall only be generated when:

✓ Both constructions are clearly visible.

✓ Both constructions are commercially recognised.

✓ The resulting terminology remains concise and natural.

Examples

Sweetheart Illusion Neck

Mandarin Keyhole Neck

Collared V Neck

Incorrect Examples

Round Sweetheart V Neck

Boat Square Round Neck

High Collar Mandarin Boat Neck

Only commercially recognised combinations shall be emitted.

---

# Dominant Construction Rule

When multiple neckline characteristics are visible but no recognised composite exists:

FCOS shall classify the garment using the dominant neckline construction.

Secondary neckline characteristics shall be described in the Individual Description when appropriate.

Example

Visual Evidence

Round neckline with decorative lace edging

Output

Neck Style

Round Neck

Description

"...finished with delicate lace detailing along the neckline."

---

# Universal Recognition Rules

FCOS shall:

✓ Preserve explicit neckline terminology from Excel or Catalog Description.

✓ Recognise partially obscured necklines using validated visual evidence.

✓ Never invent unsupported neckline constructions.

✓ Preserve collar terminology.

✓ Keep Neck Style independent from Neck Depth.

✓ Maintain consistent terminology throughout the catalog.

---

# Validation

Before output generation FCOS shall verify:

✓ Neckline supported by Evidence Hierarchy.

✓ Correct neckline family identified.

✓ Composite neckline commercially recognised.

✓ Collar terminology preserved.

✓ Neck Style remains concise and human-readable.

✓ Decorative trims are not treated as Neck Styles.

✓ Neck Style remains independent of Neck Depth.

---

# Future Extensibility

The Neckline Intelligence Engine shall support future neckline innovations without modifying the core architecture.

Examples include:

- Sculptural Necklines
- Draped Couture Necklines
- Architectural Necklines
- Avant-Garde Necklines
- Designer Signature Necklines

All future neckline styles shall inherit the same recognition framework.

---
---

# Context-Aware Neckline Intelligence Engine

## Purpose

The Context-Aware Neckline Intelligence Engine enables FCOS to interpret neckline constructions according to the detected product category while preserving standardized Neck Style terminology.

The engine shall use garment context to improve recognition accuracy without altering the commercial neckline classification.

This ensures consistency across Women's Wear, Men's Wear, Kids' Wear, Jewellery, Ethnic Wear, Indo-Western, Fusion Wear, Western Wear, and future product categories.

---

# Context Recognition Workflow

FCOS shall determine Neck Style using the following sequence:

Evidence Hierarchy

↓

Product Category

↓

Garment Component

↓

Neckline Family

↓

Specific Neck Style

↓

Validation

---

# Context Rules

The same neckline construction may appear on different garment categories.

FCOS shall preserve the standardized Neck Style while adapting its interpretation to the garment context.

Example

Product Category

Saree Blouse

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

---

Product Category

Bridal Choli

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

---

Product Category

Designer Kurti

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

The Neck Style remains identical because the construction has not changed.

---

# Garment Context

Context influences recognition, not terminology.

Examples

Women's Wear

- Saree Blouse
- Choli
- Kurti
- Dress
- Gown
- Tunic

Men's Wear

- Kurta
- Sherwani
- Shirt
- Jacket

Kids' Wear

- Girls Dress
- Boys Kurta
- Girls Lehenga Choli

Indo-Western

- Cape Gown
- Fusion Dress
- Jacket Dress

Each category may present the same neckline differently due to garment construction.

---

# Category-Aware Recognition

Examples

Saree Blouse

Sweetheart Neck

↓

Recognize deeper curved shaping typical of blouse construction.

---

Sherwani

Mandarin Collar

↓

Recognize structured standing collar.

---

Men's Shirt

Shirt Collar

↓

Recognize folded collar construction.

---

Indo-Western Gown

Halter Neck

↓

Recognize shoulder-supported neckline.

---

Girls' Dress

Round Neck

↓

Recognize simplified rounded neckline.

---

# Commercial Classification

Context shall never modify the Neck Style terminology.

Correct

Sweetheart Neck

Mandarin Collar

Round Neck

Halter Neck

Incorrect

Bridal Sweetheart Neck

Wedding Halter Neck

Designer Mandarin Collar

Royal Round Neck

Fashion identity belongs elsewhere within FCOS.

---

# Relationship with Other Specifications

Product Context influences:

✓ Fashion Intelligence

✓ Description Engine

✓ Style Identity

✓ Design Aesthetic

Product Context shall NOT alter:

✓ Neck Style

✓ Sleeve Style

✓ Construction

✓ Silhouette

unless the physical construction itself differs.

---

# Validation

FCOS shall verify:

✓ Product category correctly identified.

✓ Neckline interpreted using garment context.

✓ Neck Style terminology remains standardized.

✓ No marketing adjectives introduced into Neck Style.

✓ Consistency maintained across the catalog.

---

# Future Extensibility

The Context-Aware Neckline Intelligence Engine shall automatically support future garment categories and emerging fashion constructions while preserving standardized commercial terminology.

---
---

# Context-Aware Neckline Intelligence Engine

## Purpose

The Context-Aware Neckline Intelligence Engine enables FCOS to interpret neckline constructions according to the detected product category while preserving standardized Neck Style terminology.

The engine shall use garment context to improve recognition accuracy without altering the commercial neckline classification.

This ensures consistency across Women's Wear, Men's Wear, Kids' Wear, Jewellery, Ethnic Wear, Indo-Western, Fusion Wear, Western Wear, and future product categories.

---

# Context Recognition Workflow

FCOS shall determine Neck Style using the following sequence:

Evidence Hierarchy

↓

Product Category

↓

Garment Component

↓

Neckline Family

↓

Specific Neck Style

↓

Validation

---

# Context Rules

The same neckline construction may appear on different garment categories.

FCOS shall preserve the standardized Neck Style while adapting its interpretation to the garment context.

Example

Product Category

Saree Blouse

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

---

Product Category

Bridal Choli

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

---

Product Category

Designer Kurti

Detected Neckline

Sweetheart

Output

Neck Style: Sweetheart Neck

The Neck Style remains identical because the construction has not changed.

---

# Garment Context

Context influences recognition, not terminology.

Examples

Women's Wear

- Saree Blouse
- Choli
- Kurti
- Dress
- Gown
- Tunic

Men's Wear

- Kurta
- Sherwani
- Shirt
- Jacket

Kids' Wear

- Girls Dress
- Boys Kurta
- Girls Lehenga Choli

Indo-Western

- Cape Gown
- Fusion Dress
- Jacket Dress

Each category may present the same neckline differently due to garment construction.

---

# Category-Aware Recognition

Examples

Saree Blouse

Sweetheart Neck

↓

Recognize deeper curved shaping typical of blouse construction.

---

Sherwani

Mandarin Collar

↓

Recognize structured standing collar.

---

Men's Shirt

Shirt Collar

↓

Recognize folded collar construction.

---

Indo-Western Gown

Halter Neck

↓

Recognize shoulder-supported neckline.

---

Girls' Dress

Round Neck

↓

Recognize simplified rounded neckline.

---

# Commercial Classification

Context shall never modify the Neck Style terminology.

Correct

Sweetheart Neck

Mandarin Collar

Round Neck

Halter Neck

Incorrect

Bridal Sweetheart Neck

Wedding Halter Neck

Designer Mandarin Collar

Royal Round Neck

Fashion identity belongs elsewhere within FCOS.

---

# Relationship with Other Specifications

Product Context influences:

✓ Fashion Intelligence

✓ Description Engine

✓ Style Identity

✓ Design Aesthetic

Product Context shall NOT alter:

✓ Neck Style

✓ Sleeve Style

✓ Construction

✓ Silhouette

unless the physical construction itself differs.

---

# Validation

FCOS shall verify:

✓ Product category correctly identified.

✓ Neckline interpreted using garment context.

✓ Neck Style terminology remains standardized.

✓ No marketing adjectives introduced into Neck Style.

✓ Consistency maintained across the catalog.

---

# Future Extensibility

The Context-Aware Neckline Intelligence Engine shall automatically support future garment categories and emerging fashion constructions while preserving standardized commercial terminology.

---

# Fashion Attribute Responsibility Model

## Purpose

The Fashion Attribute Responsibility Model defines the responsibility of each Fashion Intelligence attribute within FCOS.

Each attribute shall represent one distinct fashion concept only.

No attribute shall duplicate, overlap, or replace the responsibility of another attribute.

This ensures consistent classification, prevents semantic overlap, and improves maintainability across all Fashion Intelligence modules.

---

# Attribute Responsibilities

## Neck Style

Purpose

Describes the physical neckline construction.

Examples

- Round Neck
- Sweetheart Neck
- Square Neck
- Boat Neck
- V Neck
- Mandarin Collar
- Shirt Collar

Neck Style shall never describe:

- Occasion
- Fashion identity
- Product category
- Design language

---

## Sleeve Style

Purpose

Describes the physical sleeve construction.

Examples

- Bell Sleeves
- Puff Sleeves
- Cape Sleeves
- Kimono Sleeves
- Balloon Sleeves

Sleeve Style shall never describe sleeve length.

Sleeve Length remains an independent attribute.

---

## Construction

Purpose

Describes how the garment is physically constructed.

Examples

- A-Line
- Tiered
- Panelled
- Angrakha
- Peplum
- Empire
- Jacket Layered
- Gathered

Construction is independent of Silhouette.

---

## Silhouette

Purpose

Describes how the garment falls on the body.

Examples

- Straight
- Flared
- Circular
- Mermaid
- Fit & Flare
- Relaxed

Silhouette shall never describe construction.

---

## Fit

Purpose

Describes how the garment fits the wearer.

Examples

- Regular Fit
- Relaxed Fit
- Slim Fit
- Tailored Fit
- Comfort Fit

Fit shall remain independent of Construction and Silhouette.

---

## Pattern Detail

Purpose

Describes the dominant surface pattern.

Examples

- Floral Printed
- Paisley Woven
- Bandhani Printed
- Geometric
- Heritage Motif Embroidered

Pattern shall never include decorative craftsmanship.

---

## Work Detail

Purpose

Describes decorative craftsmanship.

Examples

- Zari Embroidery
- Mirror Work
- Thread Embroidery
- Sequin Embroidery
- Gota Patti

Work Detail shall remain independent of Pattern Detail.

---

## Style Type

Purpose

Defines the fashion identity of the product.

Examples

- Heritage Elegance
- Contemporary Chic
- Minimal Luxe
- Festive Glamour
- Timeless Grace

Style Type describes the personality of the garment rather than its physical construction.

---

## Design Aesthetic

Purpose

Defines the overall visual design language.

Examples

- Regal Heritage
- Royal Opulence
- Floral Romance
- Contemporary Minimalism
- Artisan Craft

Design Aesthetic represents the artistic direction of the design.

---

## Category Type

Purpose

Defines the commercial product classification.

Examples

- Designer Lehenga
- Bridal Lehenga Choli
- Printed Saree
- Men's Kurta Pajama
- Jacket Kurta Set

Category Type identifies what the customer is purchasing.

---

# Separation of Responsibilities

| Attribute | Responsibility | Never Describes |
|------------|----------------|-----------------|
| Neck Style | Physical neckline construction | Style identity, occasion, product category |
| Sleeve Style | Physical sleeve construction | Sleeve length |
| Sleeve Length | Sleeve measurement | Sleeve construction |
| Construction | Garment build | Silhouette |
| Silhouette | Garment shape | Construction |
| Fit | Garment fit | Shape or construction |
| Pattern Detail | Surface design | Decorative work |
| Work Detail | Decorative craftsmanship | Surface pattern |
| Style Type | Fashion identity | Product classification |
| Design Aesthetic | Visual design language | Construction |
| Category Type | Commercial product classification | Fashion identity |

---

# Enterprise Principle

Every Fashion Intelligence attribute shall have one clearly defined responsibility.

No attribute shall duplicate the meaning of another.

All Fashion Intelligence modules shall reference this responsibility model to maintain consistency across FCOS.

This model serves as the foundation for Product Naming, Style Information, Description Generation, Validation, and Regression Intelligence.

---

# Related Specifications

- EvidenceHierarchy.md
- StyleInformation.md
- DescriptionEngine.md
- Validation.md
