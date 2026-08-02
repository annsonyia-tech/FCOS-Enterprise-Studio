# FCOS Enterprise Studio

# Construction Library

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Construction Library defines the universal taxonomy for identifying garment construction across all supported product categories.

Construction describes **how a garment is physically engineered and assembled**, independent of its silhouette, fit, pattern, work detail, or style identity.

It serves as the authoritative Fashion Knowledge Base for Construction Recognition and shall be used by the Fashion Intelligence Engine whenever Construction is required.

---

# Evidence Hierarchy

Construction shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Visual AI shall classify Construction only when unavailable in Excel and Catalog Description.

Fashion Intelligence may refine terminology but shall never contradict higher-priority evidence.

---

# Universal Recognition Principles

Construction shall describe **how the garment is physically built**.

Construction shall never describe:

- Silhouette
- Fit
- Pattern
- Work Detail
- Style Identity
- Design Aesthetic
- Occasion

Construction shall remain independent of all other Fashion Intelligence attributes.

---

# Construction Intelligence Workflow

Every garment shall be classified using the following sequence:

Evidence Hierarchy

↓

Garment Category

↓

Primary Construction

↓

Secondary Construction (if applicable)

↓

Hybrid Construction (if applicable)

↓

Validation

---

# Construction Categories

## Straight

Description

Garment panels fall vertically with minimal shaping.

Examples

- Straight Kurta
- Straight Dress
- Straight Tunic

---

## A-Line

Description

Garment gradually widens from the upper body toward the hem.

Examples

- A-Line Kurti
- A-Line Dress
- A-Line Gown

---

## Empire

Description

Waist seam positioned directly below the bust.

Examples

- Empire Dress
- Empire Kurti
- Empire Gown

---

## Peplum

Description

Short flared extension attached at the waist.

Examples

- Peplum Top
- Peplum Kurti
- Peplum Choli

---

## Panelled

Description

Constructed using multiple joined fabric panels.

Examples

- Panelled Lehenga
- Panelled Dress
- Panelled Gown

---

## Tiered

Description

Multiple horizontal fabric tiers creating layered volume.

Examples

- Tiered Lehenga
- Tiered Dress
- Tiered Kurti

---

## Gathered

Description

Volume created through gathering fabric into seams.

Examples

- Gathered Dress
- Gathered Kurti
- Gathered Skirt

---

## Circular

Description

Constructed using circular fabric cutting to maximize flare.

Examples

- Circular Lehenga
- Circular Skirt
- Circular Dress

---

## Angrakha

Description

Traditional overlapping wrap-front construction.

Examples

- Angrakha Kurta
- Angrakha Dress
- Angrakha Kurti

---

## Kaftan

Description

Loose integrated body construction with minimal seam shaping.

Examples

- Kaftan Dress
- Kaftan Kurti
- Kaftan Top

---

## Jacket Layered

Description

Garment incorporates an integrated or separate jacket layer.

Examples

- Jacket Kurta Set
- Jacket Dress
- Jacket Lehenga

---

## Cape Attached

Description

Integrated cape forms part of the garment construction.

Examples

- Cape Gown
- Cape Dress
- Cape Kurti

---

## High-Low

Description

Hemline intentionally varies between front and back.

Examples

- High-Low Dress
- High-Low Kurti

---

## Wrap

Description

Garment wraps around the body for closure.

Examples

- Wrap Dress
- Wrap Top

---

## Draped

Description

Construction relies on intentional fabric draping.

Examples

- Saree Gown
- Draped Dress
- Draped Top

---

## Layered

Description

Two or more visible garment layers integrated into the design.

Examples

- Layered Dress
- Layered Kurti
- Layered Gown

---

## Co-Ord

Description

Matching coordinated garment set designed as one ensemble.

Examples

- Co-Ord Set
- Printed Co-Ord Set

---

# Hybrid Construction

FCOS shall recognise garments combining multiple constructions.

Examples

- Panelled Tiered
- Empire Gathered
- Cape Attached A-Line
- Jacket Layered Straight
- Angrakha Panelled

Hybrid constructions shall only be generated when both constructions are clearly supported by the Evidence Hierarchy.

---

# Dominant Construction Rule

When multiple construction elements are visible:

Priority

1. Explicit Catalog Construction

↓

2. Commercially Recognised Hybrid Construction

↓

3. Dominant Primary Construction

↓

4. Secondary Construction

If no recognised hybrid exists, classify using the dominant construction.

Secondary construction may be described in the Individual Description.

---

# Construction vs Silhouette

Construction describes **how the garment is built**.

Silhouette describes **how the garment falls on the body**.

Example

Construction

Tiered

Silhouette

Flared

Correct

Construction: Tiered

Silhouette: Flared

Incorrect

Construction: Flared

---

# Construction vs Product Type

Construction influences Product Type but does not replace it.

Examples

Construction

Cape Attached

↓

Product Type

Cape Gown

Construction

Angrakha

↓

Product Type

Angrakha Kurta

Construction

Tiered

↓

Product Type

Tiered Lehenga

---

# Validation Rules

Before output generation FCOS shall verify:

✓ Construction supported by Evidence Hierarchy.

✓ Construction terminology standardized.

✓ Construction independent of Silhouette.

✓ Hybrid Construction commercially recognised.

✓ No duplicate Construction terminology.

✓ Construction consistent throughout the catalog.

---

# Future Extensibility

The Construction Library shall support future garment engineering techniques without modifying the core architecture.

Examples

- Sculptural Construction
- Modular Construction
- Convertible Construction
- Detachable Construction
- Transformable Construction
- Architectural Construction
- Couture Construction

All future constructions shall inherit the same classification framework.

---

---

# Construction Intelligence Engine

## Purpose

The Construction Intelligence Engine enables FCOS to recognize, classify, and standardize garment construction using a hierarchical engineering taxonomy rather than a flat list of construction names.

Instead of treating every construction equally, FCOS shall first identify the Construction Family before determining the specific garment construction.

This mirrors professional garment engineering, fashion design, and apparel product development practices while improving Fashion Intelligence accuracy and scalability.

---

# Construction Recognition Workflow

Every garment shall be classified using the following sequence:

Evidence Hierarchy

↓

Garment Category

↓

Construction Family

↓

Primary Construction

↓

Secondary Construction (if applicable)

↓

Hybrid Construction (if applicable)

↓

Validation

---

# Construction Families

## 1. Shape-Based Construction

### Description

Garments whose primary identity is determined by structural shaping.

Examples

- Straight
- A-Line
- Empire
- Peplum
- High-Low

Recognition Rule

Shape-Based Construction shall be selected when shaping defines the primary garment architecture.

Examples

A-Line Kurti

Empire Dress

Peplum Top

---

## 2. Volume-Based Construction

### Description

Garments whose primary identity is created through engineered fullness or volume.

Examples

- Gathered
- Tiered
- Circular
- Panelled

Recognition Rule

Volume-Based Construction shall take precedence when fullness is created through garment engineering rather than silhouette alone.

Examples

Tiered Lehenga

Circular Skirt

Panelled Gown

Gathered Dress

---

## 3. Traditional Construction

### Description

Garments defined by established traditional construction techniques.

Examples

- Angrakha
- Kaftan
- Wrap
- Draped

Recognition Rule

Traditional Construction shall preserve established fashion terminology.

Examples

Angrakha Kurta

Kaftan Dress

Wrap Dress

Draped Saree Gown

---

## 4. Layered Construction

### Description

Garments incorporating multiple structural layers.

Examples

- Jacket Layered
- Cape Attached
- Layered

Recognition Rule

Layered Construction shall be selected when additional garment layers form an integral part of the design.

Examples

Cape Gown

Jacket Kurta Set

Layered Dress

---

## 5. Ensemble Construction

### Description

Garments engineered as coordinated multi-piece ensembles.

Examples

- Co-Ord
- Two-Piece Ensemble
- Three-Piece Ensemble
- Jacket Set

Recognition Rule

Ensemble Construction shall describe how multiple coordinated garments function as a single commercial product.

Examples

Designer Co-Ord Set

Three-Piece Salwar Suit

Jacket Kurta Set

---

## 6. Hybrid Construction

### Description

Garments combining multiple commercially recognised construction techniques.

Examples

- Panelled Tiered
- Empire Gathered
- Cape Attached A-Line
- Jacket Layered Straight
- Angrakha Panelled

Hybrid Construction shall only be generated when all recognised constructions are clearly supported by the Evidence Hierarchy.

---

# Construction Recognition Priority

When multiple construction characteristics are detected, FCOS shall classify them using the following hierarchy:

1. Explicit Catalog Construction

↓

2. Traditional Construction

↓

3. Layered Construction

↓

4. Ensemble Construction

↓

5. Shape-Based Construction

↓

6. Volume-Based Construction

↓

7. Commercially Recognised Hybrid Construction

Higher-priority classifications shall override lower-priority classifications unless a recognised Hybrid Construction exists.

---

# Hybrid Construction Rules

Hybrid Construction shall only be generated when:

✓ All construction elements are independently identifiable.

✓ The combined construction is commercially recognised.

✓ The resulting terminology remains concise and human-readable.

Examples

Cape Attached A-Line

Empire Gathered

Panelled Tiered

Jacket Layered Straight

Incorrect Examples

Tiered Circular Gathered Empire

Cape Jacket Panelled Gathered Straight

Only commercially recognised combinations shall be emitted.

---

# Dominant Construction Rule

When multiple construction characteristics are visible but no recognised Hybrid Construction exists:

FCOS shall classify the garment using the dominant construction.

Secondary construction characteristics may be incorporated into the Individual Description where appropriate.

Example

Visual Evidence

Panelled construction with minor gathered detailing.

Output

Construction

Panelled

Description

"...finished with subtle gathered detailing that enhances movement."

---

# Construction vs Silhouette

Construction describes:

How the garment is engineered.

Silhouette describes:

How the garment visually falls on the body.

Example

Construction

Tiered

Silhouette

Flared

Correct

Construction: Tiered

Silhouette: Flared

Incorrect

Construction: Flared

---

# Universal Recognition Rules

FCOS shall:

✓ Preserve explicit construction terminology from Excel or Catalog Description.

✓ Recognise partially obscured construction using validated visual evidence.

✓ Never invent unsupported construction.

✓ Preserve commercially recognised terminology.

✓ Keep Construction independent from Silhouette.

✓ Maintain consistent terminology throughout the catalog.

---

# Validation

Before output generation FCOS shall verify:

✓ Construction supported by Evidence Hierarchy.

✓ Correct Construction Family identified.

✓ Hybrid Construction commercially recognised.

✓ Construction independent of Silhouette.

✓ Construction terminology standardised.

✓ Construction remains concise and human-readable.

---

# Future Extensibility

The Construction Intelligence Engine shall support future garment engineering techniques without modifying the core architecture.

Examples include:

- Convertible Construction
- Modular Construction
- Detachable Construction
- Sculptural Construction
- Transformable Construction
- Architectural Construction
- Couture Construction

Future construction techniques shall inherit the same classification framework.

---

# Related Specifications

- EvidenceHierarchy.md
- ProductNaming.md
- StyleInformation.md
- Silhouettes.md
- Validation.md
