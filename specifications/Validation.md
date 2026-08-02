# FCOS Enterprise Studio

# Validation Specification

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Validation Engine is the final quality assurance layer of FCOS Enterprise Studio.

Its purpose is to ensure that every generated product satisfies all Enterprise specifications before output generation.

Validation shall be automatic.

Recoverable errors shall be corrected automatically.

Only unrecoverable errors shall be reported.

---

# Validation Pipeline

Every product shall pass the following validation stages.

Input Validation

↓

Evidence Validation

↓

Fashion Intelligence Validation

↓

Measurement Validation

↓

Product Naming Validation

↓

Style Information Validation

↓

Description Validation

↓

Output Validation

↓

Catalog Validation

↓

Final Release

No product shall bypass any validation stage.

---

# Input Validation

Verify:

✓ Workbook readable

✓ Catalog Description readable

✓ Images accessible

✓ Image count matches expected input

✓ Workbook mapping available

If any mandatory input is unavailable, stop processing and report the blocking error.

---

# Evidence Validation

Validate Evidence Hierarchy.

Priority

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Checks

✓ Excel overrides Catalog

✓ Catalog overrides Visual AI

✓ Visual AI used only when permitted

✓ Fashion Intelligence used only when higher evidence is unavailable

Never overwrite higher-priority evidence.

---

# Fashion Intelligence Validation

Verify:

✓ Product Type identified

✓ Product Subtype identified where applicable

✓ Construction identified when supported

✓ Silhouette identified when supported

✓ Garment components identified

✓ Category classification correct

✓ Style Type appropriate

✓ Design Aesthetic appropriate

Never invent unsupported fashion attributes.

---

# Measurement Validation

Verify:

✓ Correct measurement strategy selected

✓ Size normalized

✓ Bust Size / Chest Size label correct

✓ Two-inch normalization applied

✓ Saree Length preserved

✓ Dupatta Length preserved

✓ Blouse Piece Length preserved

✓ Sleeve Length omitted for Sleeveless garments

✓ Units correctly formatted

---

# Product Naming Validation

Verify:

✓ 5–8 words

✓ SEO optimized

✓ Human readable

✓ Luxury editorial tone

✓ Unique within catalog

✓ Correct naming formula applied

✓ Fabric included

✓ Correct Product Type used

✓ Special Construction overrides generic Product Type

✓ Product Name never ends with:

- Set
- with Dupatta
- with Blouse

If Pattern =

Solid

Plain

Self

Missing

remove Pattern from Product Name.

---

# Style Information Validation

Verify:

Field order exactly matches:

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

Checks

✓ Colour from Excel whenever available

✓ Missing fields omitted

✓ No blank labels

✓ No duplicated fields

✓ No line breaks

✓ Single uninterrupted line

✓ Component fabrics correctly labelled

✓ Component lengths correctly labelled

---

# Description Validation

Verify

✓ Four HTML paragraphs

✓ Only <p> and <strong> tags

✓ Product Name appears once

✓ Paragraph 1 = 50–70 words

✓ Paragraph 2 = 60–80 words

✓ Paragraph 3 = 30–50 words

✓ Total = 150–180 words excluding Paragraph 4

✓ Exactly two occasions

✓ Exactly one styling suggestion

✓ Correct Care Instruction

✓ Correct Delivery Information

✓ Editorial tone maintained

✓ No unsupported claims

✓ Description unique

---

# Narrative Validation

Verify

✓ Appropriate narrative selected

✓ Narrative matches:

Style Type

Design Aesthetic

Construction

Occasion

✓ Sentence variation maintained

✓ Vocabulary variation maintained

✓ Editorial flow unique

✓ No repetitive openings

✓ No repetitive storytelling

---

# Colour Validation

Verify

✓ Colour comes from Excel

If unavailable

↓

Catalog

If unavailable

↓

Visual AI

Never overwrite workbook colour.

---

# Stitching Validation

Verify

Correct stitching classification.

Ready To Wear

Customized

Semi-Stitched

Unstitched

Jewellery

Ensure Care and Delivery Information match stitching status.

---

# Category Validation

Verify

✓ Category Type correct

✓ Product Subtype correct

✓ Product Type correct

✓ Construction consistent

✓ Silhouette consistent

---

# Image Mapping Validation

Verify

Strict 1:1 Image-to-Row Mapping.

Checks

✓ No missing rows

✓ No duplicate rows

✓ No skipped images

✓ No extra products

Image count must equal output row count.

---

# Catalog Validation

Verify

✓ Product Names unique

✓ Descriptions unique

✓ Consistent terminology

✓ Consistent formatting

✓ Consistent measurements

✓ Consistent Style Information

✓ No duplicate products

✓ SEO uniqueness maintained

---

# HTML Validation

Verify

✓ Valid HTML

✓ Proper tag nesting

✓ No unsupported tags

✓ No broken HTML

Allowed Tags

<p>

<strong>

No other HTML tags permitted.

---

# Output Validation

Verify

Output structure:

S.No

↓

Product Name

↓

Colour

↓

Style Information

↓

Individual Description

If

Rows ≤ 3

↓

Display table.

If

Rows > 3

↓

Generate downloadable Excel.

---

# Performance Validation

Verify

✓ No repeated confirmations

✓ Single validation pass

✓ Automatic recovery

✓ Low context usage

✓ Enterprise formatting maintained

---

# Auto-Correction Rules

Automatically correct:

✓ Duplicate spaces

✓ Capitalization

✓ Measurement formatting

✓ HTML formatting

✓ Field ordering

✓ Missing commas

✓ Product Name uniqueness

✓ Word count deviations

✓ Style Information ordering

---

# Blocking Errors

Stop processing only when:

Workbook unreadable

Image mapping impossible

Corrupted workbook

Unsupported file format

Missing mandatory inputs

Everything else shall be automatically corrected.

---

# Enterprise Quality Score

Each product shall be evaluated.

| Category | Weight |
|----------|--------:|
| Evidence Accuracy | 25 |
| Fashion Intelligence | 20 |
| Product Naming | 15 |
| Style Information | 15 |
| Description Quality | 15 |
| Measurement Accuracy | 5 |
| HTML & Formatting | 5 |

Maximum Score

100

Release Threshold

98+

Products below 98 shall be automatically revalidated before release.

---

# Final Release Checklist

Before release, FCOS shall verify:

✓ Evidence Hierarchy followed

✓ Fashion Intelligence complete

✓ Measurements validated

✓ Product Name unique

✓ Style Information correct

✓ Description validated

✓ Narrative validated

✓ HTML valid

✓ Image mapping correct

✓ Catalog consistency maintained

✓ Output format correct

✓ Enterprise Quality Score ≥ 98

Only after all checks pass shall the catalog be released.

---

# Scope

This specification governs validation only.

Related Specifications

- EvidenceHierarchy.md
- ProductNaming.md
- StyleInformation.md
- MeasurementRules.md
- DescriptionEngine.md
- MasterPrompt.md
