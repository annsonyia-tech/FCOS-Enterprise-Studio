# FCOS Enterprise
## Fit Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

This document defines the Fit Intelligence Engine used by FCOS Enterprise.

Its purpose is to identify, normalize, classify, and describe garment fit across Women's Wear, Men's Wear, Kids' Wear, Jewellery (where applicable), Ethnic Wear, Indo-Western Wear, and Western Wear.

Fit describes how the garment is intended to sit on the wearer's body.

Fit is independent of:

• Product Type
• Product Subtype
• Construction
• Silhouette
• Fabric
• Pattern
• Work Detail

Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may determine Fit only when higher-priority evidence is unavailable.

---

# Definition

Fit defines the relationship between the garment and the human body.

It describes ease, shaping, body proximity, and intended wearing comfort.

Examples

✔ Regular Fit

✔ Relaxed Fit

✔ Slim Fit

✔ Tailored Fit

NOT

✘ Straight

✘ A-Line

✘ Flared

✘ Tiered

Those describe Construction or Silhouette.

---

# Fit Categories

## Standard Fit

Regular Fit

Classic Fit

Standard Fit

Traditional Fit

Comfort Fit

---

## Relaxed Fit

Relaxed Fit

Loose Fit

Easy Fit

Comfort Relaxed Fit

Relaxed Straight Fit

---

## Body Fitted

Slim Fit

Tailored Fit

Body Fit

Shaped Fit

Close Fit

Figure-Hugging Fit

Contoured Fit

---

## Oversized

Oversized Fit

Boxy Fit

Boyfriend Fit

Dropped Shoulder Fit

Wide Fit

---

## Structured

Structured Fit

Architectural Fit

Precision Tailored Fit

Sharp Tailored Fit

---

## Contemporary

Modern Fit

Contemporary Fit

Smart Fit

Urban Fit

Minimal Fit

---

## Traditional Ethnic

Classic Ethnic Fit

Heritage Fit

Traditional Fit

Comfort Ethnic Fit

---

## Kids

Comfort Fit

Relaxed Fit

Play Fit

Regular Fit

---

# Fit Detection Rules

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

# Fit Inference Rules

Fit may be inferred only when supported by Construction, Silhouette, and visible ease.

Examples

Construction

Straight Cut

Silhouette

Straight

↓

Regular Fit

--------------------------------

Construction

A-Line

Silhouette

Flared

↓

Comfort Fit

--------------------------------

Construction

Body Contour

↓

Slim Fit

--------------------------------

Construction

Oversized Shirt

↓

Oversized Fit

--------------------------------

Construction

Tailored Blazer

↓

Tailored Fit

--------------------------------

Construction

Kaftan

↓

Relaxed Fit

---

# Fit vs Construction

Construction

↓

A-Line

Fit

↓

Regular Fit

Correct

Construction:
A-Line

Fit:
Regular Fit

NOT

Fit:
A-Line

---

# Fit vs Silhouette

Silhouette

↓

Flared

Fit

↓

Comfort Fit

Correct

Silhouette:
Flared

Fit:
Comfort Fit

NOT

Fit:
Flared

---

# Fit Normalization

Normalize supplier wording.

Examples

Regular

↓

Regular Fit

Comfort

↓

Comfort Fit

Slim

↓

Slim Fit

Tailored

↓

Tailored Fit

Loose

↓

Relaxed Fit

Oversize

↓

Oversized Fit

---

# Category Guidelines

Women's Wear

Regular Fit

Comfort Fit

Relaxed Fit

Slim Fit

Tailored Fit

Oversized Fit

--------------------------------

Men's Wear

Classic Fit

Regular Fit

Modern Fit

Slim Fit

Tailored Fit

Relaxed Fit

--------------------------------

Kids Wear

Comfort Fit

Relaxed Fit

Regular Fit

Play Fit

---

# Style Information Rule

Include Fit only when:

• Excel provides it

OR

• Catalog Description provides it

OR

• It can be confidently inferred without contradicting visible evidence.

Otherwise

↓

Omit the field completely.

---

# Confidence Rule

If confidence is insufficient

↓

Omit Fit.

Never invent garment fit.

---

# Future-Proof Rule

FCOS shall recognize any commercially accepted garment fit supported by:

Excel

Catalog Description

Visual AI

Fashion Reasoning

Unknown fit terminology shall be normalized using the closest accepted commercial fashion terminology.

---

# Examples

Example 1

Construction:
Straight

Silhouette:
Straight

Fit:
Regular Fit

--------------------------------

Example 2

Construction:
Peplum

Silhouette:
Fit & Flare

Fit:
Comfort Fit

--------------------------------

Example 3

Construction:
Tailored

Silhouette:
Slim

Fit:
Tailored Fit

--------------------------------

Example 4

Construction:
Kaftan

Silhouette:
Relaxed

Fit:
Relaxed Fit

--------------------------------

Example 5

Construction:
Oversized Shirt

Silhouette:
Boxy

Fit:
Oversized Fit
