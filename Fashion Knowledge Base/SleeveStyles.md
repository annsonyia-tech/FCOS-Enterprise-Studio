# FCOS Enterprise Studio

# Sleeve Styles Library

Version: FCOS AI Studio Enterprise v2.1.1

Status: Architecture Frozen

---

# Purpose

The Sleeve Styles Library defines the universal taxonomy for identifying sleeve styles across all supported fashion categories.

It serves as the authoritative Fashion Knowledge Base for Sleeve Style Recognition and shall be used by the Fashion Intelligence Engine whenever Sleeve Style is required.

This specification governs only Sleeve Style recognition.

---

# Evidence Hierarchy

Sleeve Style shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Higher-priority evidence shall always override lower-priority evidence.

Visual AI shall be used only when Sleeve Style is unavailable in Excel and Catalog Description.

Fashion Intelligence may refine terminology but shall never contradict higher-priority evidence.

---

# Universal Recognition Principles

FCOS shall identify the actual sleeve construction rather than generic sleeve terminology.

Sleeve Style shall describe the visual design and construction of the sleeve.

Sleeve Length shall be treated as a separate attribute.

Examples

Correct

Sleeve Style: Puff Sleeves

Sleeve Length: 10–12 Inches

Incorrect

Sleeve Style: Long Sleeves

---

# Universal Rules

Sleeve Style shall always end with:

" Sleeves "

Examples

Bell Sleeves

Puff Sleeves

Cape Sleeves

Bishop Sleeves

Kimono Sleeves

Elbow Sleeves

Full Sleeves

Sleeveless

---

Never generate generic sleeve names such as:

Regular Sleeves

Traditional Sleeves

Classic Sleeves

Normal Sleeves

Standard Sleeves

Straight Sleeves

Simple Sleeves

Basic Sleeves

---

Sleeve Length shall never appear for:

Sleeveless

---

# Sleeve Recognition Rules

FCOS shall recognise sleeve construction even when partially hidden by:

- Dupatta
- Saree Pallu
- Hair
- Jewellery
- Layering
- Folds
- Pose

Only when supported by visible evidence.

If confidence is insufficient, omit Sleeve Style.

Never invent.

---

# Sleeve Style vs Sleeve Length

Sleeve Style

Describes construction.

Examples

Bell Sleeves

Cape Sleeves

Puff Sleeves

Sleeve Length

Describes physical length.

Examples

6–8 Inches

10–12 Inches

20–22 Inches

These attributes shall always remain independent.

---

# Validation Rules

Before output generation FCOS shall verify:

✓ Sleeve Style supported by Evidence Hierarchy

✓ Sleeve Style ends with "Sleeves"

✓ Sleeve Style not generic

✓ Sleeve Length omitted for Sleeveless

✓ Sleeve Style and Sleeve Length not duplicated

✓ Terminology standardized

✓ Consistent across catalog

---

# Future Extensibility

The Sleeve Styles Library shall support future sleeve constructions without modifying the core architecture.

Examples

- Convertible Sleeves
- Detachable Sleeves
- Couture Sleeves
- Avant-Garde Sleeves
- Designer Signature Sleeves

Future sleeve styles shall inherit the same recognition framework.

---

# Sleeve Style Taxonomy

Sleeve Styles shall be organized by construction family rather than alphabetically or by sleeve length.

The taxonomy shall remain extensible and support future sleeve innovations without modifying the core architecture.

---

# 1. Volume Sleeves

Description

Sleeves characterised by added fullness created through gathering, pleating, shaping, or structured volume.

Examples

- Puff Sleeves
- Balloon Sleeves
- Bishop Sleeves
- Lantern Sleeves
- Juliet Sleeves

Recognition Priority

Determine fullness, gathering, and volume before evaluating sleeve length.

---

# 2. Flared Sleeves

Description

Sleeves that widen progressively from the arm toward the opening.

Examples

- Bell Sleeves
- Angel Sleeves
- Trumpet Sleeves

Recognition Priority

Identify the flared opening rather than sleeve length.

---

# 3. Integrated Sleeves

Description

Sleeves constructed as an extension of the garment body rather than attached separately.

Examples

- Kimono Sleeves
- Dolman Sleeves
- Raglan Sleeves
- Batwing Sleeves

Recognition Priority

Recognize integrated cutting lines before evaluating silhouette.

---

# 4. Decorative Sleeves

Description

Sleeves incorporating decorative construction elements.

Examples

- Cape Sleeves
- Layered Sleeves
- Double Layer Sleeves
- Slit Sleeves
- Ruffle Sleeves
- Gathered Sleeves
- Cuffed Sleeves
- Roll-Up Sleeves

Recognition Priority

Construction details override sleeve length.

---

# 5. Exposure Sleeves

Description

Sleeves intentionally exposing part or all of the shoulder.

Examples

- Cold Shoulder Sleeves
- Off-Shoulder Sleeves
- One-Shoulder Sleeves

Recognition Priority

Shoulder exposure takes precedence over sleeve length.

---

# 6. Length-Based Sleeves

Description

Sleeves primarily distinguished by finished length rather than structural styling.

Examples

- Cap Sleeves
- Short Sleeves
- Elbow Sleeves
- Three-Quarter Sleeves
- Bracelet Sleeves
- Full Sleeves
- Sleeveless

Recognition Priority

Use this category only when no distinctive construction or styling feature is present.

---

# Sleeve Recognition Priority

When multiple sleeve characteristics exist, FCOS shall classify them in the following order:

1. Exposure Construction
2. Integrated Construction
3. Decorative Construction
4. Volume Construction
5. Flared Construction
6. Length-Based Classification

Examples

Cape Sleeve extending to the wrist

Output

Sleeve Style: Cape Sleeves

Not

Full Sleeves

---

Puff sleeve ending at the elbow

Output

Sleeve Style: Puff Sleeves

Sleeve Length: 10–12 Inches

Not

Elbow Sleeves

---

Cold shoulder bell sleeve

Output

Sleeve Style: Cold Shoulder Bell Sleeves

Never reduce to

Bell Sleeves

or

Cold Shoulder Sleeves

when both constructions are clearly identifiable.

---

# Universal Recognition Rules

• Sleeve Style shall always describe the most distinctive construction.

• Sleeve Length shall remain a separate measurement attribute.

• Never replace a distinctive construction with a generic length-based sleeve style.

• When multiple sleeve constructions coexist, combine them only when both are clearly supported by the available evidence.

• If confidence is insufficient, omit the Sleeve Style rather than inventing one.

---

---

# Composite Sleeve Recognition

## Purpose

The Composite Sleeve Recognition Engine enables FCOS to identify and classify garments that combine multiple sleeve constructions.

Rather than forcing a single Sleeve Style classification, FCOS shall generate a composite Sleeve Style when multiple distinctive sleeve characteristics are simultaneously supported by the Evidence Hierarchy.

Composite Sleeve Recognition improves Fashion Intelligence accuracy for premium designer garments, couture collections, Indo-Western fashion, and contemporary silhouettes.

---

# Evidence Hierarchy

Composite Sleeve recognition shall follow:

Excel Workbook

↓

Catalog Description

↓

Visual AI

↓

Fashion Intelligence

Composite Sleeve Styles shall only be generated when supported by the available evidence.

---

# Composite Recognition Principles

A composite Sleeve Style shall be generated only when:

• Multiple sleeve constructions are simultaneously visible.

• The combined construction is commercially meaningful.

• The combined construction does not contradict higher-priority evidence.

If confidence is insufficient, classify only the most confidently identified Sleeve Style.

---

# Composite Sleeve Examples

Examples include:

- Cold Shoulder Bell Sleeves
- Cape Puff Sleeves
- Layered Bell Sleeves
- Bishop Slit Sleeves
- Balloon Cuffed Sleeves
- Raglan Full Sleeves
- Kimono Three-Quarter Sleeves
- Puff Elbow Sleeves
- Bell Three-Quarter Sleeves
- Cape Full Sleeves

Future composite styles shall follow the same recognition framework.

---

# Composite Construction Priority

When multiple sleeve characteristics are detected, FCOS shall evaluate them in the following order:

1. Exposure Construction
2. Integrated Construction
3. Decorative Construction
4. Volume Construction
5. Flared Construction
6. Length Classification

Each higher-priority construction shall take precedence over lower-priority construction.

---

# Composite Classification Rules

## Exposure + Flared

Example

Cold Shoulder

+

Bell Sleeves

↓

Cold Shoulder Bell Sleeves

---

## Decorative + Volume

Example

Cape

+

Puff Sleeves

↓

Cape Puff Sleeves

---

## Decorative + Flared

Example

Layered

+

Bell Sleeves

↓

Layered Bell Sleeves

---

## Volume + Decorative

Example

Balloon

+

Cuffed

↓

Balloon Cuffed Sleeves

---

## Integrated + Length

Example

Kimono

+

Three-Quarter

↓

Kimono Three-Quarter Sleeves

---

## Integrated + Length

Example

Raglan

+

Full

↓

Raglan Full Sleeves

---

# Composite Generation Rules

FCOS shall combine sleeve attributes only when:

✓ Both constructions are clearly visible.

✓ Both constructions are commercially recognised.

✓ Combined terminology remains natural and human-readable.

FCOS shall never generate artificial combinations.

---

# Invalid Examples

Incorrect

Bell Puff Raglan Cape Sleeves

Incorrect

Bell Puff Balloon Sleeves

Incorrect

Cape Bell Puff Raglan Sleeves

Only commercially meaningful combinations are permitted.

---

# Sleeve Length Independence

Composite Sleeve Style shall remain independent of Sleeve Length.

Example

Sleeve Style

Cape Puff Sleeves

Sleeve Length

10–12 Inches

Never merge Sleeve Length into Sleeve Style.

---

# Validation Rules

Before output generation, FCOS shall verify:

✓ Composite Sleeve supported by Evidence Hierarchy.

✓ Combination commercially valid.

✓ Terminology standardized.

✓ Sleeve Length reported separately.

✓ No contradictory constructions.

✓ No unsupported combinations.

✓ Composite Sleeve remains concise and human-readable.

---

# Future Extensibility

The Composite Sleeve Recognition Engine shall automatically support future designer sleeve innovations while preserving the existing classification framework.

New sleeve constructions may be added without modifying the core recognition logic.

---

---

# Dominant Construction Rule

## Purpose

The Dominant Construction Rule ensures that Sleeve Style remains commercially meaningful, human-readable, and aligned with established fashion terminology.

When multiple sleeve characteristics are detected, FCOS shall prioritize the most distinctive and commercially recognized sleeve construction rather than generating unnecessarily complex composite names.

This rule improves consistency with premium fashion retailers and designer catalogs while preserving Fashion Intelligence accuracy.

---

# Recognition Priority

Sleeve Style shall be determined using the following hierarchy:

1. Explicit Designer or Catalog Sleeve Name
2. Commercially Recognized Composite Sleeve Style
3. Dominant Sleeve Construction
4. Sleeve Length Classification

The highest applicable level shall always take precedence.

---

# Rule 1 – Preserve Explicit Sleeve Names

When Excel or the Catalog Description explicitly specifies a sleeve style, FCOS shall preserve that terminology.

Examples

Catalog

Cape Sleeves

↓

Output

Cape Sleeves

Catalog

Kimono Sleeves

↓

Output

Kimono Sleeves

Visual AI shall not override documented sleeve names.

---

# Rule 2 – Generate Composite Sleeve Styles

Composite Sleeve Styles shall only be generated when:

✓ Multiple sleeve characteristics are clearly visible.

✓ The combination is commercially recognized.

✓ The resulting name remains concise and natural.

Examples

Cold Shoulder Bell Sleeves

Cape Puff Sleeves

Layered Bell Sleeves

Balloon Cuffed Sleeves

Kimono Three-Quarter Sleeves

Raglan Full Sleeves

---

# Rule 3 – Apply Dominant Construction

When no recognised composite exists, FCOS shall classify the garment using the dominant sleeve construction.

Secondary sleeve characteristics may be incorporated into the Individual Description when relevant.

Example

Visual Features

Puff construction with minor cuff detailing

↓

Sleeve Style

Puff Sleeves

Description

"...finished with neatly tailored cuffs for a refined look."

---

# Rule 4 – Avoid Overly Complex Composites

FCOS shall never generate excessively long sleeve names.

Incorrect

Cape Puff Balloon Slit Bell Sleeves

Layered Cape Bell Balloon Sleeves

Correct

Cape Puff Sleeves

Bell Sleeves

Balloon Cuffed Sleeves

Only commercially meaningful combinations shall be produced.

---

# Rule 5 – Preserve Readability

Sleeve Style shall remain:

✓ Human-readable

✓ Commercially recognised

✓ SEO-friendly

✓ Consistent with luxury fashion terminology

Complex visual details that do not contribute to the commercial sleeve classification shall instead be described within the Individual Description.

---

# Examples

| Visual Features | Sleeve Style | Description |
|-----------------|--------------|-------------|
| Cape + Puff | Cape Puff Sleeves | May mention soft gathered volume |
| Bell + Slit | Bell Sleeves | Slit detail described in editorial copy |
| Balloon + Cuff | Balloon Cuffed Sleeves | Cuff refinement may be highlighted |
| Raglan + Full Length | Raglan Full Sleeves | Length remains supported separately |
| Puff + Decorative Buttons | Puff Sleeves | Buttons described in narrative |

---

# Validation

Before output generation, FCOS shall verify:

✓ Explicit catalog sleeve names preserved.

✓ Composite Sleeve Style used only when commercially recognised.

✓ Dominant Construction applied where appropriate.

✓ Sleeve Style remains concise and readable.

✓ Secondary decorative sleeve details captured in the Individual Description rather than forcing additional sleeve classifications.

---

# Scope

This rule governs Sleeve Style classification only.

Related Specifications

- SleeveStyles.md
- EvidenceHierarchy.md
- StyleInformation.md
- DescriptionEngine.md
- Validation.md
