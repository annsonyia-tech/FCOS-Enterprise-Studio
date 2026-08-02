# FCOS Enterprise
## Weaving Intelligence Engine
Version: 2.0
Status: Architecture Frozen

---

# Purpose

The Weaving Intelligence Engine enables FCOS Enterprise to identify, normalize, classify, and describe weaving techniques across all supported product categories.

Weaving defines how yarns are interlaced to create fabric.

Weaving is independent of:

• Fabric Type
• Pattern
• Work Detail
• Construction
• Silhouette
• Garment Components

Supported Categories

• Women's Wear
• Men's Wear
• Kids Wear
• Sarees
• Lehengas
• Salwar Suits
• Kurtas
• Dupattas
• Indo-Western
• Fusion Wear
• Western Wear

---

# Evidence Hierarchy

FCOS follows the standard Evidence Hierarchy.

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Weaving only when higher-priority evidence is unavailable.

Excel always overrides every other source.

---

# Definition

Weaving describes the fabric manufacturing technique.

It answers:

"How was the fabric woven?"

NOT

"What is the fabric?"

NOT

"What embroidery exists?"

---

# Fabric vs Weaving

Fabric

Silk Blend

Weaving

Banarasi

Correct

Fabric:
Silk Blend

Weaving:
Banarasi Weave

---

Fabric

Cotton

Weaving

Jamdani

Correct

Fabric:
Cotton

Weaving:
Jamdani Weave

---

# Primary Weaving Categories

## Plain Weave

Plain Weave

Balanced Plain Weave

Open Plain Weave

Compact Plain Weave

---

## Twill Weave

Twill Weave

Diagonal Twill

Broken Twill

Herringbone Twill

Diamond Twill

---

## Satin Weave

Satin Weave

Five Harness Satin

Eight Harness Satin

Matt Satin

---

## Jacquard Weave

Jacquard Weave

Floral Jacquard

Paisley Jacquard

Geometric Jacquard

Textured Jacquard

Self Jacquard

---

## Brocade

Brocade Weave

Floral Brocade

Zari Brocade

Silk Brocade

Banarasi Brocade

---

## Banarasi

Banarasi Weave

Katan Banarasi

Organza Banarasi

Tissue Banarasi

Jangla Banarasi

Tanchoi Banarasi

Butidar Banarasi

Cutwork Banarasi

Rangkaat Banarasi

---

## Kanchipuram

Kanchipuram Weave

Korvai Weave

Temple Border Weave

Traditional Kanchipuram

Contrast Border Weave

---

## Jamdani

Jamdani Weave

Fine Jamdani

Handwoven Jamdani

Extra Weft Jamdani

---

## Chanderi

Chanderi Weave

Silk Chanderi

Cotton Chanderi

Silk Cotton Chanderi

---

## Maheshwari

Maheshwari Weave

Traditional Maheshwari

Silk Maheshwari

Cotton Maheshwari

---

## Patola

Patola Weave

Double Ikat Patola

Single Ikat Patola

Rajkot Patola

Patan Patola

---

## Ikat

Ikat Weave

Single Ikat

Double Ikat

Warp Ikat

Weft Ikat

---

## Khadi

Khadi Weave

Handspun Khadi

Handwoven Khadi

Fine Khadi

---

## Linen

Linen Weave

Natural Linen

Textured Linen

---

## Kota

Kota Doria

Square Kota

Fine Kota

Cotton Kota

Silk Kota

---

## Tissue

Tissue Weave

Metallic Tissue

Silk Tissue

Zari Tissue

---

## Organza

Organza Weave

Silk Organza

Soft Organza

Textured Organza

---

## Net

Power Net

Soft Net

Mesh Weave

Fine Mesh

---

# Decorative Weaves

Temple Border Weave

Contrast Border Weave

Extra Weft Weave

Extra Warp Weave

Self Woven

Textured Weave

Basket Weave

Dobby Weave

Honeycomb Weave

Mock Leno

Leno Weave

---

# Regional Indian Weaves

Banarasi

Kanchipuram

Jamdani

Patola

Maheshwari

Chanderi

Baluchari

Paithani

Mangalagiri

Ilkal

Pochampally

Narayanpet

Venkatagiri

Gadwal

Sambalpuri

Bomkai

Kotpad

Bhagalpuri

Tussar Handloom

Khun

---

# International Weaves

Tweed

Houndstooth

Oxford Weave

Chambray

Denim Weave

Poplin

Canvas

Duck Weave

Corduroy

Seersucker

---

# Weaving Detection Rules

Use Excel first.

↓

Catalog Description.

↓

Visual AI.

↓

Fashion Reasoning.

Never overwrite Excel.

---

# Weaving Normalization

Supplier

Banarsi

↓

Banarasi Weave

Supplier

Jacquard Design

↓

Jacquard Weave

Supplier

Handloom

↓

Handwoven Weave

Supplier

Brocade

↓

Brocade Weave

Supplier

Kanchi Silk

↓

Kanchipuram Weave

Supplier

Patola Design

↓

Patola Weave

---

# Weaving vs Pattern

Pattern

Paisley Print

Weaving

Jacquard Weave

Correct

Pattern Detail

Paisley Print

Weaving

Jacquard Weave

---

# Weaving vs Work

Work

Zari Embroidery

Weaving

Banarasi Weave

Correct

Work Detail

Zari Embroidery

Weaving

Banarasi Weave

---

# Multiple Weaving Rule

If multiple weaving techniques exist,

output primary weave first.

Examples

Banarasi Weave with Zari Brocade

Jacquard Weave with Dobby Texture

Patola Weave with Double Ikat

---

# Style Information

Weaving should only appear when it adds commercial value or is explicitly supported by evidence.

Examples

Saree Fabric: Silk Blend

Weaving: Banarasi Weave

---

Kurta Fabric: Cotton

Weaving: Dobby Weave

---

# Description Generation

Editorial descriptions should naturally incorporate weaving.

Example

"The luxurious Banarasi weave enhances the silk blend with exceptional richness and timeless craftsmanship."

---

# Confidence Rule

If weaving cannot be confidently identified,

omit Weaving.

Never invent weaving techniques.

---

# Future-Proof Rule

FCOS Enterprise shall recognize any commercially accepted weaving technique supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown weaving techniques shall be normalized to the closest accepted commercial weaving terminology.

---

# Enterprise Examples

Example 1

Fabric:
Silk Blend

Weaving:
Banarasi Weave

Pattern:
Heritage Motif

Work:
Zari Embroidery

---

Example 2

Fabric:
Cotton

Weaving:
Jamdani Weave

Pattern:
Floral Woven

Work:
Thread Embroidery

---

Example 3

Fabric:
Organza

Weaving:
Plain Weave

Pattern:
Floral Print

Work:
Sequin Embroidery

---

Example 4

Fabric:
Silk Blend

Weaving:
Jacquard Weave

Pattern:
Paisley Woven

Work:
Resham Embroidery

---

End of Weaving Intelligence Engine
