# FCOS Enterprise
## Work Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Work Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe decorative workmanship applied to garments and jewellery.

Work Detail is independent of:

• Pattern
• Fabric
• Construction
• Silhouette
• Garment Components

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Work Detail only when higher-priority evidence is unavailable.

---

# Definition

Work Detail describes decorative techniques applied to the product.

It does NOT describe:

• Fabric
• Pattern
• Construction
• Silhouette
• Product Type

Examples

✔ Zari Embroidery
✔ Mirror Work
✔ Thread Embroidery

NOT

✘ Floral Print
✘ Silk Blend
✘ A-Line

---

# Work Categories

## Embroidery

Zari Embroidery

Resham Embroidery

Thread Embroidery

Silk Thread Embroidery

Cotton Thread Embroidery

Wool Embroidery

Aari Embroidery

Maggam Work

Chikankari Embroidery

Kantha Embroidery

Kashida Embroidery

Phulkari Embroidery

Applique Embroidery

Cutwork Embroidery

Shadow Work

Hand Embroidery

Machine Embroidery

Multi-thread Embroidery

Cord Embroidery

Ribbon Embroidery

---

## Metallic Work

Zari Work

Dabka Work

Nakshi Work

Kasab Work

Tilla Work

Badla Work

Metal Thread Work

---

## Stone & Crystal Work

Stone Work

Crystal Work

Diamond Work

Rhinestone Work

American Diamond Work

CZ Stone Work

Gemstone Work

Pearl Work

Bead Work

Sequinned Crystal Work

---

## Sequin Work

Sequin Embroidery

Multi Sequin Work

Laser Sequin Work

Matte Sequin Work

Gloss Sequin Work

Tonal Sequin Work

---

## Mirror Work

Mirror Work

Kutchi Mirror Work

Shisha Work

Mirror Embroidery

---

## Patch Work

Kutchi Patch Work

Patch Work

Fabric Patch Work

Applique Patch Work

Leather Patch Work

Decorative Patch Work

---

## Lace & Borders

Lace Work

Crochet Lace

Scalloped Lace

Border Lace

Decorative Border

Fringed Border

Tassel Border

Pom Pom Border

---

## Traditional Indian Craft

Gota Patti

Zardozi

Aari Work

Mukaish

Pitta Work

Dori Work

Kundan Work

Gota Lace

Tissue Work

Maggam Work

Bandhej Embellishment

---

## Printed Decorative Finish

Foil Print

Metallic Foil Print

Glitter Print

Pigment Print

Screen Print

Digital Print

Discharge Print

Burnout Print

---

## Weaving Decoration

Jacquard Weave

Brocade Weave

Banarasi Weave

Kanchipuram Weave

Patola Weave

Jamdani Weave

Chanderi Weave

Maheshwari Weave

Temple Border Weave

Zari Woven Border

---

## Surface Texture

Smocking

Pleating

Ruching

Gathering

Pin Tucks

Quilting

Textured Surface

Crushed Texture

---

## Handmade Craft

Hand Painted

Hand Block Printed

Hand Dyed

Hand Woven

Hand Crafted

Hand Finished

---

## Jewellery Work

Kundan Setting

Polki Setting

Temple Jewellery

Antique Finish

Oxidised Finish

Filigree Work

Meenakari

Pearl Setting

Stone Setting

Bead Setting

---

# Work Normalization

Normalize supplier wording.

Examples

Zari Embroidery Work

↓

Zari Embroidery

Heavy Sequence Work

↓

Heavy Sequin Work

Thread Embroidery Work

↓

Thread Embroidery

Mirror Embroidery Work

↓

Mirror Work

Kutchi Embroidery Patch

↓

Kutchi Patch Work

---

# Work Detection Rules

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

# Pattern vs Work

Pattern

↓

Bandhani Print

Work

↓

Mirror Work

Correct

Pattern Detail:
Bandhani Print

Work Detail:
Mirror Work

NOT

Pattern Detail:
Mirror Work

---

# Multiple Work Rule

If multiple decorative techniques exist:

List all major techniques.

Example

Work Detail:

Zari, Resham & Sequin Embroidery

Example

Mirror Work, Thread Embroidery & Gota Patti

---

# Work Priority

Always list work in this order:

Primary handcrafted work

↓

Secondary embellishment

↓

Decorative finish

Example

Zari, Resham & Sequin Embroidery

NOT

Sequin, Zari & Resham

---

# Confidence Rule

If confidence is insufficient

↓

Omit Work Detail.

Never invent decorative work.

---

# Future-Proof Rule

FCOS shall recognize any commercially accepted decorative workmanship supported by:

Excel

Catalog Description

Visual AI

Fashion Reasoning

Unknown decorative techniques shall be normalized using the closest accepted commercial terminology.
