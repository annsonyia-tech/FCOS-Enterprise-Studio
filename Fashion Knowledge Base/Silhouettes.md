# FCOS Enterprise Studio

# Silhouettes Library

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Silhouettes Library defines the universal taxonomy for identifying garment silhouettes across all supported fashion categories.

Silhouette describes **how the garment visually falls on the body after construction**, independent of garment construction, fit, pattern, work detail, style identity, or design aesthetic.

It serves as the authoritative Fashion Knowledge Base for Silhouette Recognition and shall be used by the Fashion Intelligence Engine whenever Silhouette is required.

---

# Evidence Hierarchy

Silhouette shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Visual AI shall classify Silhouette only when unavailable in Excel and Catalog Description.

Fashion Intelligence may refine terminology but shall never contradict higher-priority evidence.

---

# Universal Recognition Principles

Silhouette shall describe **the visual outline created when the garment is worn.**

Silhouette shall never describe:

- Construction
- Fit
- Pattern
- Work Detail
- Style Identity
- Design Aesthetic
- Occasion

Silhouette remains independent of all other Fashion Intelligence attributes.

---

# Silhouette Intelligence Workflow

Every garment shall be classified using the following sequence:

Evidence Hierarchy

↓

Garment Category

↓

Silhouette Family

↓

Primary Silhouette

↓

Secondary Silhouette (if applicable)

↓

Validation

---

# Silhouette Families

## 1. Straight Silhouettes

Description

Garments falling vertically with minimal flare.

Examples

- Straight
- Column
- Shift

Examples of Products

- Straight Kurta
- Straight Dress
- Straight Tunic

---

## 2. Flared Silhouettes

Description

Garments widening gradually or dramatically toward the hem.

Examples

- Flared
- A-Line
- Fit & Flare
- Circular

Examples of Products

- Flared Kurti
- Circular Lehenga
- A-Line Dress

---

## 3. Fitted Silhouettes

Description

Garments closely following body contours.

Examples

- Slim
- Bodycon
- Sheath
- Mermaid

Examples of Products

- Mermaid Gown
- Sheath Dress

---

## 4. Relaxed Silhouettes

Description

Garments designed with generous ease.

Examples

- Relaxed
- Oversized
- Loose
- Boxy

Examples of Products

- Kaftan
- Oversized Shirt
- Relaxed Kurta

---

## 5. Draped Silhouettes

Description

Silhouettes created primarily through natural fabric drape.

Examples

- Draped
- Waterfall
- Cascade

Examples of Products

- Saree Gown
- Draped Dress

---

## 6. Layered Silhouettes

Description

Silhouettes created using multiple visible garment layers.

Examples

- Layered
- Tiered Flared
- Cape Flowing

Examples of Products

- Cape Gown
- Layered Dress

---

# Hybrid Silhouettes

FCOS may generate hybrid silhouettes only when commercially recognised.

Examples

- Tiered Flared
- Relaxed Straight
- Fit & Flare
- Draped Circular

Hybrid silhouettes shall remain concise and commercially meaningful.

---

---

# Silhouette Confidence Rule

## Purpose

The Silhouette Confidence Rule ensures that FCOS produces concise, commercially recognised, and human-readable silhouette classifications while avoiding unnecessary complexity.

Silhouette classification shall prioritise clarity, consistency, and commercial fashion terminology over exhaustive visual enumeration.

---

# Decision Hierarchy

When determining the final silhouette, FCOS shall apply the following priority:

1. Explicit Catalog Silhouette

↓

2. Commercially Recognised Hybrid Silhouette

↓

3. Dominant Primary Silhouette

↓

4. Secondary Visual Characteristics (Description Only)

Higher-priority classifications shall always override lower-priority classifications.

---

# Recognition Rules

## Rule 1 — Preserve Explicit Catalog Silhouette

If the Excel workbook or Catalog Description explicitly specifies a silhouette, FCOS shall preserve that terminology without modification unless it contradicts higher-priority evidence.

Examples

Catalog

Fit & Flare

Output

Fit & Flare

---

## Rule 2 — Generate Hybrid Silhouette Only When Commercially Recognised

When multiple silhouette characteristics are visible, FCOS shall generate a Hybrid Silhouette only if the combination is widely recognised within commercial fashion terminology.

Examples

✓ Fit & Flare

✓ Tiered Flared

✓ Relaxed Straight

✓ Draped Circular

---

## Rule 3 — Prefer the Dominant Silhouette

When no recognised Hybrid Silhouette exists, FCOS shall output only the dominant silhouette.

Secondary silhouette characteristics may be incorporated into the Individual Description where appropriate.

Example

Visual Evidence

Relaxed body with slight flare.

Output

Silhouette

Relaxed

Description

"...finished with a softly flared hem that enhances graceful movement."

---

## Rule 4 — Avoid Overly Complex Combinations

FCOS shall never generate silhouette combinations that reduce readability or commercial usability.

Examples

Correct

- Fit & Flare
- Tiered Flared
- Relaxed Straight

Avoid

- Relaxed Flared Circular Layered
- Draped Relaxed Circular Flared
- Oversized Tiered Circular

---

## Rule 5 — Confidence-Based Omission

If no silhouette can be confidently determined from the Evidence Hierarchy, FCOS shall omit the Silhouette field rather than generating an uncertain classification.

Silhouette shall never be inferred solely to complete the Style Information.

---

# Enterprise Principles

FCOS shall prioritise:

✓ Commercially recognised silhouette terminology.

✓ Human-readable output.

✓ Consistency across the catalog.

✓ Compliance with the Evidence Hierarchy.

✓ Independence from Construction and Fit.

✓ Concise classifications suitable for SEO, merchandising, and luxury retail presentation.

---

# Silhouette Recognition Priority

When multiple silhouette characteristics are detected:

1. Explicit Catalog Silhouette

↓

2. Commercially Recognised Hybrid Silhouette

↓

3. Primary Silhouette

↓

4. Secondary Silhouette

---

# Dominant Silhouette Rule

When multiple silhouettes are visible but no recognised hybrid exists:

FCOS shall emit the dominant silhouette.

Secondary visual characteristics may be incorporated into the Individual Description.

Example

Visual Evidence

Relaxed body with slight flare

Output

Silhouette

Relaxed

Description

"...finished with a softly flared hem for graceful movement."

---

# Silhouette vs Construction

Construction

Describes how the garment is engineered.

Examples

Tiered

Panelled

Peplum

Empire

Silhouette

Describes how the garment falls.

Examples

Flared

Straight

Relaxed

Mermaid

Correct

Construction: Tiered

Silhouette: Flared

Incorrect

Construction: Flared

---

# Silhouette vs Fit

Silhouette

Overall visual shape.

Fit

How closely the garment follows the body.

Example

Silhouette

Flared

Fit

Regular Fit

Both attributes are independent.

---

# Validation Rules

Before output generation FCOS shall verify:

✓ Silhouette supported by Evidence Hierarchy.

✓ Correct Silhouette Family identified.

✓ Construction and Silhouette are not duplicated.

✓ Hybrid Silhouette commercially recognised.

✓ Terminology standardised.

✓ Human-readable output.

✓ Consistent terminology throughout the catalog.

---

# Future Extensibility

The Silhouettes Library shall support future fashion silhouettes without modifying the core architecture.

Examples

- Sculptural
- Architectural
- Cocoon
- Tulip
- Balloon
- Avant-Garde
- Convertible

Future silhouettes shall inherit the same recognition framework.

---

---

# Silhouette Intelligence Engine

## Purpose

The Silhouette Intelligence Engine enables FCOS to recognise, classify, and standardise garment silhouettes using a hierarchical silhouette taxonomy rather than a flat list of silhouette names.

Instead of treating every silhouette equally, FCOS shall first determine the Silhouette Family before identifying the Primary Silhouette and evaluating whether a commercially recognised Hybrid Silhouette exists.

This approach mirrors professional fashion merchandising and apparel classification while improving recognition accuracy, consistency, and scalability.

---

# Silhouette Recognition Workflow

Every garment shall be classified using the following sequence:

Evidence Hierarchy

↓

Garment Category

↓

Silhouette Family

↓

Primary Silhouette

↓

Secondary Silhouette (if applicable)

↓

Hybrid Silhouette (if applicable)

↓

Validation

---

# Silhouette Families

## 1. Linear Silhouettes

### Description

Garments characterised by clean, vertical lines with minimal flare.

Examples

- Straight
- Column
- Shift

Recognition Rule

Linear Silhouettes shall be selected when the garment maintains a predominantly vertical profile.

---

## 2. Flared Silhouettes

### Description

Garments widening progressively toward the hem.

Examples

- Flared
- A-Line
- Circular
- Fit & Flare

Recognition Rule

Flared Silhouettes shall be selected when widening is the dominant visual characteristic.

---

## 3. Contoured Silhouettes

### Description

Garments designed to closely follow the body's contours.

Examples

- Slim
- Sheath
- Mermaid
- Bodycon

Recognition Rule

Contoured Silhouettes shall be selected when body shaping defines the overall appearance.

---

## 4. Relaxed Silhouettes

### Description

Garments designed with generous ease and a loose profile.

Examples

- Relaxed
- Oversized
- Loose
- Boxy

Recognition Rule

Relaxed Silhouettes shall be selected when ease and volume dominate the visual appearance.

---

## 5. Draped Silhouettes

### Description

Silhouettes primarily defined by flowing fabric movement and draping.

Examples

- Draped
- Waterfall
- Cascade

Recognition Rule

Draped Silhouettes shall be selected when fabric drape is the defining visual characteristic.

---

## 6. Layered Silhouettes

### Description

Silhouettes created through multiple visible garment layers.

Examples

- Layered
- Tiered Flared
- Cape Flowing

Recognition Rule

Layered Silhouettes shall be selected when layering significantly influences the overall visual profile.

---

## 7. Hybrid Silhouettes

### Description

Silhouettes combining two commercially recognised silhouette characteristics.

Examples

- Relaxed Straight
- Fit & Flare
- Draped Circular
- Tiered Flared

Hybrid Silhouettes shall only be generated when both characteristics are clearly supported by the Evidence Hierarchy and the resulting terminology is commercially recognised.

---

# Silhouette Recognition Priority

When multiple silhouette characteristics are detected:

1. Explicit Catalog Silhouette

↓

2. Commercially Recognised Hybrid Silhouette

↓

3. Primary Silhouette

↓

4. Secondary Silhouette

Higher-priority classifications shall override lower-priority classifications unless a recognised Hybrid Silhouette exists.

---

# Dominant Silhouette Rule

When multiple silhouette characteristics are visible but no recognised Hybrid Silhouette exists:

FCOS shall emit only the dominant silhouette.

Secondary silhouette characteristics may be incorporated into the Individual Description where appropriate.

---

# Universal Recognition Rules

FCOS shall:

✓ Preserve explicit silhouette terminology from Excel or Catalog Description.

✓ Recognise partially obscured silhouettes using validated visual evidence.

✓ Never invent unsupported silhouettes.

✓ Preserve commercially recognised terminology.

✓ Keep Silhouette independent from Construction.

✓ Maintain consistent terminology throughout the catalog.

---

# Validation

Before output generation FCOS shall verify:

✓ Silhouette supported by the Evidence Hierarchy.

✓ Correct Silhouette Family identified.

✓ Hybrid Silhouette commercially recognised.

✓ Silhouette independent of Construction.

✓ Terminology standardised.

✓ Output remains concise, human-readable, and commercially meaningful.

---

# Future Extensibility

The Silhouette Intelligence Engine shall support future silhouette concepts without modifying the core architecture.

Examples

- Cocoon
- Tulip
- Sculptural
- Architectural
- Balloon
- Avant-Garde
- Convertible

Future silhouettes shall inherit the same classification framework.

---

# Related Specifications

- Construction.md
- ProductNaming.md
- StyleInformation.md
- DescriptionEngine.md
- Validation.md
