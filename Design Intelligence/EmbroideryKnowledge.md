# FCOS Enterprise
## Embroidery Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

The Embroidery Intelligence Engine enables FCOS Enterprise to identify, normalize, classify, and describe embroidery techniques across all supported product categories.

Supported Categories

• Women's Wear
• Men's Wear
• Kids Wear
• Sarees
• Lehengas
• Salwar Suits
• Kurtas
• Indo-Western
• Jewellery (where embroidery exists on textile components)

Embroidery is a subtype of Work Detail.

It must never be confused with:

• Pattern
• Fabric
• Construction
• Silhouette

---

# Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may identify embroidery only when higher-priority evidence is unavailable.

Excel always overrides every other source.

---

# Definition

Embroidery is decorative stitching created using threads, metallic yarns, beads, sequins, mirrors, pearls, or other embellishments applied to fabric.

Embroidery may be:

• Hand Embroidered
• Machine Embroidered
• Mixed Technique

---

# Embroidery Categories

## Thread Embroidery

Thread Embroidery

Cotton Thread Embroidery

Silk Thread Embroidery

Rayon Thread Embroidery

Poly Thread Embroidery

Multi-Thread Embroidery

Contrast Thread Embroidery

Tone-on-Tone Thread Embroidery

---

## Zari Embroidery

Zari Embroidery

Gold Zari Embroidery

Silver Zari Embroidery

Copper Zari Embroidery

Antique Zari Embroidery

Metallic Zari Embroidery

---

## Resham Embroidery

Resham Embroidery

Fine Resham Embroidery

Multicolour Resham Embroidery

Hand Resham Embroidery

---

## Aari Embroidery

Aari Work

Aari Embroidery

Fine Aari Embroidery

Heavy Aari Embroidery

---

## Maggam Embroidery

Maggam Work

Traditional Maggam Work

Heavy Maggam Work

Bridal Maggam Work

---

## Chikankari

Chikankari Embroidery

Hand Chikankari

Shadow Chikankari

Lucknowi Chikankari

---

## Kantha

Kantha Embroidery

Running Stitch Kantha

Hand Kantha

---

## Kashida

Kashida Embroidery

Kashmiri Kashida

Hand Kashida

---

## Phulkari

Phulkari Embroidery

Traditional Phulkari

Heavy Phulkari

---

## Mirror Embroidery

Mirror Embroidery

Shisha Embroidery

Kutchi Mirror Embroidery

Mirror Thread Embroidery

---

## Sequin Embroidery

Sequin Embroidery

Heavy Sequin Embroidery

Tonal Sequin Embroidery

Laser Sequin Embroidery

Matte Sequin Embroidery

Gloss Sequin Embroidery

---

## Stone Embroidery

Stone Embroidery

Crystal Embroidery

Rhinestone Embroidery

Pearl Embroidery

Bead Embroidery

American Diamond Embroidery

---

## Applique Embroidery

Applique Embroidery

Patch Applique

Decorative Applique

Fabric Applique

---

## Ribbon Embroidery

Ribbon Embroidery

Silk Ribbon Embroidery

Decorative Ribbon Embroidery

---

## Cutwork

Cutwork Embroidery

Laser Cutwork

Decorative Cutwork

---

## Cord Embroidery

Cord Embroidery

Dori Embroidery

Twisted Cord Embroidery

---

## Crochet Embroidery

Crochet Lace Embroidery

Hand Crochet

Decorative Crochet

---

## Mixed Embroidery

Zari & Resham Embroidery

Thread & Mirror Embroidery

Zari, Resham & Sequin Embroidery

Mirror & Thread Embroidery

Pearl & Stone Embroidery

Aari & Zari Embroidery

Heavy Bridal Embroidery

---

# Embroidery Placement

FCOS should identify placement when supported.

Examples

All Over Embroidery

Yoke Embroidery

Neck Embroidery

Sleeve Embroidery

Border Embroidery

Hemline Embroidery

Panel Embroidery

Scattered Embroidery

Front Embroidery

Back Embroidery

Shoulder Embroidery

Cuff Embroidery

Pallu Embroidery

Pleat Embroidery

---

# Embroidery Density

Light Embroidery

Medium Embroidery

Heavy Embroidery

Rich Embroidery

Intricate Embroidery

Bridal Embroidery

Festival Embroidery

---

# Embroidery Style Identity

Traditional Embroidery

Heritage Embroidery

Contemporary Embroidery

Minimal Embroidery

Royal Embroidery

Luxury Embroidery

Artisan Embroidery

Handcrafted Embroidery

---

# Embroidery Normalization

Normalize supplier terminology.

Examples

Sequence Work
↓

Sequin Embroidery

Zari Work
↓

Zari Embroidery

Resham Work
↓

Resham Embroidery

Heavy Embroidery Work
↓

Heavy Embroidery

Mirror Embroidery Work
↓

Mirror Embroidery

Thread Work
↓

Thread Embroidery

---

# Multiple Embroidery Rule

When multiple embroidery techniques exist,
list them in craftsmanship order.

Examples

Zari, Resham & Sequin Embroidery

Mirror & Thread Embroidery

Pearl, Stone & Zari Embroidery

---

# Priority Order

Hand Embroidery

↓

Traditional Embroidery

↓

Machine Embroidery

↓

Decorative Finish

Example

Correct

Zari, Resham & Sequin Embroidery

Incorrect

Sequin, Zari & Resham

---

# Pattern vs Embroidery

Pattern

Bandhani Print

Embroidery

Mirror Embroidery

Correct

Pattern Detail:
Bandhani Print

Work Detail:
Mirror Embroidery

---

# Confidence Rule

If embroidery cannot be confidently identified from the Evidence Hierarchy,

omit Work Detail.

Never infer or invent embroidery.

---

# Future-Proof Rule

FCOS Enterprise shall recognize any commercially accepted embroidery technique supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown embroidery techniques shall be normalized to the closest commercially accepted embroidery terminology without introducing unsupported embellishment types.
