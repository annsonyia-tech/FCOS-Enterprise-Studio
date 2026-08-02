# FCOS Enterprise
## Construction Intelligence Engine
Version: 2.0
Status: Architecture Frozen

---

# Purpose

The Construction Intelligence Engine enables FCOS Enterprise to identify, normalize, classify, and describe garment construction across all supported fashion categories.

Construction describes **how a garment is structurally engineered**. It is independent of Product Type, Silhouette, Fit, Pattern, Fabric, and Work Detail.

Construction is one of the core Fashion Intelligence attributes used for:

• Product Classification
• SEO Product Naming
• Style Information
• Editorial Description Generation
• Visual Fashion Intelligence

---

# Evidence Hierarchy

FCOS always follows the Evidence Hierarchy.

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Excel always overrides every other source.

Visual AI may determine Construction only when higher-priority evidence is unavailable.

Construction must never contradict verified evidence.

---

# Construction Intelligence Model

FCOS recognizes Construction using two intelligence levels.

## Level 1 — Primary Construction

Primary Construction defines the fundamental structural engineering of the garment.

It answers:

"How is this garment built?"

Examples

Straight

A-Line

Panelled

Tiered

Empire

Gathered

Princess Line

Peplum

Angrakha

Kaftan

Circular

Anarkali

Wrap

Shirt Construction

Jacket Construction

Cape Construction

Two Piece Ensemble

Three Piece Ensemble

Layered Ensemble

Only Primary Construction defines the structural identity of the garment.

---

## Level 2 — Construction Features

Construction Features describe secondary structural elements that enhance the Primary Construction.

Construction Features never replace Primary Construction.

Examples

Front Slit

Center Slit

Side Slit

Double Side Slits

Back Slit

Princess Seam

Yoke

Empire Seam

Waist Seam

Panel Join

Godet Inserts

Cape Attached

Detachable Cape

Jacket Layered

Overlay

Attached Jacket

Transparent Overlay

Attached Dupatta

Detachable Jacket

High-Low Hem

Asymmetric Hem

Curved Hem

Shark Bite Hem

Scalloped Hem

Gathered Waist

Gathered Hem

Ruffled Layers

Box Pleats

Knife Pleats

Sunray Pleats

Raglan Shoulder

Dropped Shoulder

Dolman Sleeve Construction

Kimono Sleeve Construction

Construction Features should only be included when confidently supported by the Evidence Hierarchy.

---

# Primary Construction Library

## Straight Construction

Straight

Straight Cut

Straight Panel

Straight Kurta

Straight Tunic

Straight Dress

Straight Gown

---

## A-Line Construction

A-Line

Soft A-Line

Structured A-Line

Classic A-Line

---

## Panelled Construction

Panelled

Six Panel

Eight Panel

Multi Panel

Princess Panel

Godet Panel

---

## Tiered Construction

Tiered

Double Tier

Triple Tier

Multi Tier

Layered Tier

Graduated Tier

---

## Gathered Construction

Gathered

Waist Gathered

Empire Gathered

Yoke Gathered

Hem Gathered

---

## Empire Construction

Empire

Empire Waist

Raised Empire

Empire Seam

---

## Princess Construction

Princess Line

Princess Cut

Princess Seam Construction

---

## Circular Construction

Circular

Semi Circular

Full Circular

Double Circular

Umbrella Construction

---

## Peplum Construction

Peplum

Layered Peplum

Asymmetric Peplum

Structured Peplum

---

## Angrakha Construction

Angrakha

Wrap Angrakha

Tie Angrakha

Cross Angrakha

---

## Kaftan Construction

Kaftan

Panelled Kaftan

Gathered Kaftan

Relaxed Kaftan

---

## Anarkali Construction

Anarkali

Empire Anarkali

Circular Anarkali

Panelled Anarkali

---

## Shirt Construction

Shirt

Shirt Dress

Shirt Kurta

Shirt Tunic

---

## Wrap Construction

Wrap

Overlap

Cross Over

Tie Wrap

---

## Jacket Construction

Jacket Construction

Open Jacket

Structured Jacket

Layered Jacket

---

## Cape Construction

Cape Construction

Attached Cape

Flowing Cape

Structured Cape

---

## Ensemble Construction

Two Piece Ensemble

Three Piece Ensemble

Layered Ensemble

Co-Ord Construction

---

# Bottom Construction Library

Straight Pant

Cigarette Pant

Palazzo

Sharara

Gharara

Dhoti Pant

Tulip Pant

Flared Pant

Skirt

Gathered Skirt

Panelled Skirt

Circular Skirt

Mermaid Skirt

Tiered Lehenga

Panelled Lehenga

Circular Lehenga

Gathered Lehenga

---

# Construction Feature Library

## Slits

Front Slit

Center Slit

Side Slit

Double Side Slits

Back Slit

---

## Layering

Cape Attached

Detachable Cape

Jacket Layered

Overlay

Transparent Overlay

Attached Jacket

Attached Dupatta

Detachable Jacket

---

## Structural Elements

Princess Seam

Yoke

Empire Seam

Waist Seam

Panel Join

Godet Inserts

Decorative Panels

---

## Hemlines

High-Low Hem

Asymmetric Hem

Curved Hem

Straight Hem

Scalloped Hem

Shark Bite Hem

Rounded Hem

---

## Volume Features

Gathered Waist

Gathered Hem

Box Pleats

Knife Pleats

Sunray Pleats

Accordion Pleats

Ruffled Layers

---

## Sleeve Construction

Raglan Shoulder

Dropped Shoulder

Dolman Sleeve Construction

Kimono Sleeve Construction

Cape Sleeve Construction

---

# Construction Detection Rules

Determine Primary Construction first.

↓

Identify Construction Features.

↓

Determine Silhouette.

↓

Determine Fit.

Construction must never be confused with Silhouette.

---

# Construction vs Silhouette

Construction

Panelled

Silhouette

Flared

Correct

Construction:
Panelled

Silhouette:
Flared

---

Construction

Empire

Silhouette

Fit & Flare

Correct

Construction:
Empire

Silhouette:
Fit & Flare

---

Construction

Gathered

Silhouette

A-Line

Correct

Construction:
Gathered

Silhouette:
A-Line

---

Construction

Tiered

Silhouette

Flared

Correct

Construction:
Tiered

Silhouette:
Flared

---

# Construction vs Product Type

Product Type

Lehenga Kurti

Construction

Gathered

Construction Features

Front Slit

Silhouette

A-Line

All four attributes are independent.

---

# Construction Normalization

Supplier

Umbrella Cut

↓

Circular

Supplier

Umbrella Lehenga

↓

Circular Lehenga

Supplier

Princess Cut

↓

Princess Line

Supplier

Three Layer

↓

Tiered

Supplier

Jacket Style

↓

Jacket Construction

Supplier

Cape Style

↓

Cape Construction

Supplier

Frock Style

↓

A-Line

---

# Style Information Output

Construction shall always output the Primary Construction.

If verified Construction Features exist,

append them naturally.

Examples

Construction: Panelled

Construction: Panelled with Front Slit

Construction: Empire with Cape Attached

Construction: Gathered with Tiered Hem

Construction: Straight with Side Slits

Construction: A-Line with Overlay Jacket

---

# Description Generation

Construction intelligence should enrich editorial descriptions.

Example

Instead of

"A beautiful kurti."

Generate

"The gathered construction complemented by a graceful front slit creates fluid movement while maintaining an elegant A-Line profile."

---

# Confidence Rule

If Construction cannot be confidently verified,

omit Construction.

Never invent structural engineering.

---

# Future-Proof Rule

FCOS Enterprise shall recognize any commercially accepted garment construction supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown constructions shall be normalized to the closest commercially accepted construction terminology.

---

# Enterprise Examples

Example 1

Product Type:
Lehenga Kurti

Construction:
Gathered with Front Slit

Silhouette:
A-Line

---

Example 2

Product Type:
Cape Gown

Construction:
Empire with Cape Attached

Silhouette:
Fit & Flare

---

Example 3

Product Type:
Peplum Top

Construction:
Peplum

Silhouette:
Regular

---

Example 4

Product Type:
Tiered Lehenga

Construction:
Panelled with Tiered Hem

Silhouette:
Flared

---

Example 5

Product Type:
Anarkali Suit

Construction:
Empire, Panelled

Silhouette:
Circular

---

End of Construction Intelligence Engine
