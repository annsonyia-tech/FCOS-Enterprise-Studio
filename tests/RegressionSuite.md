# FCOS Enterprise Studio

# Regression Intelligence Engine

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Regression Intelligence Engine protects FCOS Enterprise Studio against unintended behavioral changes.

Unlike the Validation Engine, which validates only the current output, the Regression Intelligence Engine compares the current release with previously approved FCOS releases to ensure that improvements never introduce regressions.

Regression testing shall execute automatically before every production release.

---

# Objectives

The Regression Intelligence Engine shall:

✓ Preserve previously approved behaviour

✓ Detect unexpected output changes

✓ Detect specification violations

✓ Detect formatting regressions

✓ Detect Fashion Intelligence regressions

✓ Detect SEO regressions

✓ Detect measurement regressions

✓ Ensure enterprise stability

---

# Regression Pipeline

Baseline Release

↓

Generate Current Output

↓

Compare Outputs

↓

Detect Differences

↓

Classify Differences

↓

Approve or Reject

↓

Release

---

# Regression Categories

## 1. Product Naming Regression

Verify:

✓ Naming Formula unchanged

✓ Product Name remains 5–8 words

✓ Product Name includes Fabric

✓ Special Construction still overrides generic Product Type

✓ Pattern removal rule still applied

✓ No Product Name ends with:

- Set
- with Dupatta
- with Blouse

✓ Product Name uniqueness maintained

---

## 2. Fashion Intelligence Regression

Verify:

✓ Product Type unchanged

✓ Product Subtype unchanged

✓ Construction unchanged

✓ Silhouette unchanged

✓ Garment Components unchanged

✓ Style Type unchanged

✓ Design Aesthetic unchanged

✓ Category Type unchanged

---

## 3. Evidence Hierarchy Regression

Verify:

Excel

↓

Catalog

↓

Visual AI

↓

Fashion Intelligence

has not changed.

Higher-priority evidence shall never be replaced by lower-priority evidence.

---

## 4. Measurement Regression

Verify:

✓ Bust Size unchanged

✓ Chest Size unchanged

✓ Free Size unchanged

✓ 2-inch normalization unchanged

✓ Saree Length preserved

✓ Dupatta Length preserved

✓ Sleeve Length normalization preserved

✓ Measurement units unchanged

---

## 5. Style Information Regression

Verify:

Field order remains:

Size

↓

Colour

↓

Fabric Details

↓

Length Details

↓

Construction

↓

Silhouette

↓

Fit

↓

Sleeve Style

↓

Sleeve Length

↓

Neck Style

↓

Pattern Detail

↓

Work Detail

↓

Occasion

↓

Stitching Status

↓

Style Type

↓

Design Aesthetic

↓

Category Type

↓

Product Subtype

Verify:

✓ No fields missing

✓ No duplicated fields

✓ No reordered fields

✓ Single-line formatting preserved

---

## 6. Description Regression

Verify:

✓ Four paragraphs maintained

✓ HTML structure unchanged

✓ Word count maintained

✓ Product Name appears once

✓ Two occasions maintained

✓ One styling suggestion maintained

✓ Care Instruction unchanged

✓ Delivery Information unchanged

✓ Editorial tone preserved

---

## 7. Narrative Intelligence Regression

Verify:

✓ Narrative category appropriate

✓ Narrative variation preserved

✓ Vocabulary diversity maintained

✓ Sentence diversity maintained

✓ No repetitive storytelling

---

## 8. HTML Regression

Verify:

✓ Only <p>

✓ Only <strong>

✓ Valid HTML

✓ No unsupported tags

---

## 9. Output Regression

Verify:

Output columns remain:

S.No

Product Name

Colour

Style Information

Individual Description

Output behaviour:

Rows ≤ 3

↓

Table

Rows > 3

↓

Excel

---

## 10. Image Mapping Regression

Verify:

✓ Image count unchanged

✓ Row count unchanged

✓ No duplicate rows

✓ No missing rows

✓ 1:1 mapping preserved

---

# Approved Changes

The following changes are permitted:

✓ Better Product Names

✓ Better Fashion Intelligence

✓ Better Narrative Diversity

✓ Improved SEO

✓ Better HTML

✓ Better Measurement Accuracy

✓ Expanded Fashion Knowledge

All approved changes shall be documented before release.

---

# Regression Severity

## Critical

Examples

Wrong Product Type

Wrong Colour

Wrong Size

Wrong Fabric

Broken HTML

Duplicate Product

Missing Product

Release Blocked

---

## Major

Examples

Wrong Construction

Wrong Silhouette

Wrong Style Information order

Description below minimum quality

Release requires review

---

## Minor

Examples

Improved vocabulary

Better editorial wording

Better SEO wording

Release permitted

---

# Golden Catalog

FCOS shall maintain a permanent regression dataset.

Recommended minimum:

- Sarees
- Lehengas
- Salwar Suits
- Kurtis
- Kurta Sets
- Co-Ord Sets
- Gowns
- Dresses
- Men's Kurta
- Sherwani
- Kids Wear
- Jewellery

Every future release shall reproduce compliant outputs for this benchmark set.

---

# Regression Report

Every release shall generate:

Release Version

Regression Pass Rate

Critical Issues

Major Issues

Minor Improvements

New Features

Performance Metrics

Overall Status

---

# Release Gate

FCOS shall only approve a release when:

✓ Validation Engine passes

✓ Regression Engine passes

✓ No Critical regressions

✓ No unresolved Major regressions

✓ Enterprise Quality Score ≥ 98

Only then may the release be marked as Production Ready.

---

# Scope

This specification governs regression testing only.

Related Specifications

- Validation.md
- EvidenceHierarchy.md
- ProductNaming.md
- StyleInformation.md
- MeasurementRules.md
- DescriptionEngine.md
