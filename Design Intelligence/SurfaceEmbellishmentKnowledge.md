# FCOS Enterprise
## Surface Embellishment Intelligence Engine
Version: 1.0
Status: Architecture Frozen

---

# Purpose

The Surface Embellishment Intelligence Engine enables FCOS Enterprise to identify, normalize, classify, and describe decorative surface embellishments applied to garments and textile products.

Surface embellishments are decorative elements attached or applied to the fabric surface and are distinct from:

• Fabric
• Pattern
• Embroidery
• Construction
• Silhouette

This knowledge engine supports all current and future product categories.

Supported Categories

• Women's Wear
• Men's Wear
• Kids Wear
• Sarees
• Lehengas
• Salwar Suits
• Kurtas
• Indo-Western
• Fusion Wear
• Western Wear
• Dupattas
• Blouses
• Jackets
• Capes

---

# Evidence Hierarchy

1. Excel
2. Catalog Description
3. Visual AI
4. Fashion Reasoning

Visual AI may identify embellishments only when higher-priority evidence is unavailable.

Excel always overrides Catalog Description and Visual AI.

---

# Definition

Surface Embellishment refers to decorative elements attached to or applied on the fabric surface.

Examples include:

• Mirrors
• Stones
• Pearls
• Beads
• Crystals
• Tassels
• Fringes
• Sequins
• Shells
• Coins
• Studs

Surface Embellishment does NOT describe:

• Print
• Weaving
• Embroidery
• Fabric
• Garment Construction

---

# Mirror Embellishment

Mirror Work

Kutchi Mirror Work

Shisha Work

Round Mirror Work

Square Mirror Work

Decorative Mirror Work

Hand-Applied Mirror Work

Mirror Border

Mirror Yoke

Mirror Panel

Mirror Scattered Work

---

# Stone Embellishment

Stone Work

Crystal Work

Glass Stone Work

American Diamond Work

CZ Stone Work

Semi-Precious Stone Work

Gemstone Work

Decorative Stone Work

Hotfix Stone Work

Flat Stone Work

---

# Pearl Embellishment

Pearl Work

Pearl Embellishment

Pearl Border

Pearl Scattered Work

Pearl Cluster Work

Freshwater Pearl Work

Artificial Pearl Work

---

# Bead Embellishment

Bead Work

Seed Bead Work

Glass Bead Work

Wooden Bead Work

Metal Bead Work

Crystal Bead Work

Decorative Bead Work

---

# Sequin Surface Work

Sequin Work

Heavy Sequin Work

Tonal Sequin Work

Laser Sequin Work

Matte Sequin Work

Gloss Sequin Work

Reversible Sequin Work

Scattered Sequin Work

---

# Shell Embellishment

Shell Work

Cowrie Shell Work

Natural Shell Work

Decorative Shell Work

---

# Coin Embellishment

Coin Work

Metal Coin Work

Decorative Coin Work

Oxidised Coin Work

---

# Stud Embellishment

Metal Stud Work

Decorative Stud Work

Pyramid Stud Work

Round Stud Work

Crystal Stud Work

---

# Lace Embellishment

Decorative Lace

Scalloped Lace

Crochet Lace

Border Lace

Neck Lace

Sleeve Lace

Panel Lace

Hem Lace

---

# Fringe & Tassels

Fringe Detail

Thread Fringe

Beaded Fringe

Tassel Detail

Decorative Tassels

Layered Tassels

Pom Pom Detail

---

# Decorative Borders

Decorative Border

Embellished Border

Stone Border

Mirror Border

Pearl Border

Beaded Border

Fringed Border

Lace Border

---

# Decorative Surface Finish

Foil Finish

Metallic Finish

Glitter Finish

Shimmer Finish

Gloss Finish

Matte Finish

Textured Finish

Burnout Finish

Crushed Finish

Pleated Surface

Quilted Surface

Smocked Surface

Ruffled Surface

Ruched Surface

---

# Placement Detection

When supported by evidence, FCOS should identify embellishment placement.

Examples

All Over

Scattered

Yoke

Front Panel

Back Panel

Neckline

Sleeves

Cuffs

Hemline

Border

Shoulder

Waist

Pocket

Pallu

Pleats

---

# Density Classification

Light Surface Work

Medium Surface Work

Heavy Surface Work

Rich Surface Embellishment

Bridal Surface Work

Luxury Surface Work

---

# Normalization Rules

Normalize supplier wording.

Examples

Sequence Work
↓

Sequin Work

Stone Decoration
↓

Stone Work

Mirror Decoration
↓

Mirror Work

Pearl Decoration
↓

Pearl Work

Stud Decoration
↓

Stud Work

---

# Multiple Surface Embellishments

If multiple embellishments exist, list them in order of visual prominence.

Examples

Mirror Work, Pearl Work & Stone Work

Stone Work, Crystal Work & Bead Work

Mirror Work & Tassel Detail

---

# Surface Embellishment vs Embroidery

Surface Embellishment

Mirror Work

Embroidery

Zari Embroidery

Correct

Work Detail:

Zari Embroidery, Mirror Work

NOT

Pattern Detail:

Mirror Work

---

# Confidence Rule

If embellishment cannot be confidently verified using the Evidence Hierarchy,

omit the embellishment.

Never invent decorative details.

---

# Future-Proof Rule

FCOS Enterprise shall recognize any commercially accepted textile surface embellishment supported by:

• Excel
• Catalog Description
• Visual AI
• Fashion Reasoning

Unknown embellishments shall be normalized to the closest accepted commercial terminology without introducing unsupported decorative elements.
