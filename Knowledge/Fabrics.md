FCOS Enterprise
Fabric Intelligence Engine (Fabrics.md)

Version: 1.0
Status: Architecture Frozen

1. Purpose

The Fabric Intelligence Engine enables FCOS to identify, normalize, classify, validate, and describe all apparel and jewellery component materials using a universal evidence hierarchy.

Fabric intelligence supports:

Product Naming
Style Information
Product Description
Fabric Feel
Fabric Movement
Care Instructions
Occasion Classification
Product Classification
SEO Optimization
2. Evidence Hierarchy

Always follow:

Excel
↓
Catalog Description
↓
Visual AI
↓
Fashion Reasoning

Excel always overrides every other source.

Visual AI must never overwrite Excel.

3. Fabric Component Rules

Always identify fabrics by garment component.

Examples

Saree Fabric

Blouse Fabric

Lehenga Fabric

Choli Fabric

Kurta Fabric

Bottom Fabric

Pant Fabric

Dupatta Fabric

Jacket Fabric

Cape Fabric

Lining Fabric

Inner Fabric

Never output

Fabric: Silk Blend

Instead

Kurta Fabric: Silk Blend

Bottom Fabric: Silk Blend

Dupatta Fabric: Organza
4. Fabric Categories
Silk

Silk

Pure Silk

Soft Silk

Raw Silk

Banarasi Silk

Kanchipuram Silk

Tussar Silk

Matka Silk

Dupion Silk

Chanderi Silk

Bhagalpuri Silk

Art Silk

Silk Blend

Cotton

Cotton

Pure Cotton

Organic Cotton

Slub Cotton

Cambric Cotton

Mul Cotton

Muslin Cotton

Linen Cotton

Cotton Blend

Khadi Cotton

Linen

Linen

Pure Linen

Linen Blend

Cotton Linen

Wool

Wool

Merino Wool

Cashmere

Pashmina

Wool Blend

Rayon Family

Rayon

Viscose Rayon

Modal

Modal Silk

Bamboo Rayon

Rayon Blend

Synthetic

Polyester

Polyester Blend

Crepe

Georgette

Faux Georgette

Chiffon

Organza

Net

Mesh

Tulle

Satin

Velvet

Taffeta

Shimmer

Lycra

Spandex

Designer Fabrics

Jacquard

Brocade

Tissue

Crushed Tissue

Chinon

Roman Silk

Dola Silk

Mashru Silk

Uppada Silk

Kota

Kota Doria

Kora Cotton

Kora Silk

Denim

Denim

Stretch Denim

Cotton Denim

Knit Fabrics

Jersey

Interlock

Rib Knit

Ponte

French Terry

Leather

Leather

Faux Leather

Suede

PU Leather

5. Fabric Normalization

Normalize supplier terminology.

Example

GGT

↓

Georgette

Art Silk

↓

Art Silk

Cot Silk

↓

Cotton Silk

PV

↓

Poly Viscose
6. Fabric Characteristics

Store internally.

Examples

Texture

Soft

Smooth

Crisp

Slub

Grainy

Sheer

Opaque

Lightweight

Medium Weight

Heavy Weight

Stretch

Non-Stretch

Breathable

Structured

Fluid

7. Fabric Movement

Used for descriptions.

Examples

Fluid Drape

Soft Fall

Structured Fall

Flowing Movement

Voluminous

Crisp Structure

8. Fabric Finish

Store internally.

Examples

Matte

Glossy

Shimmer

Metallic

Textured

Washed

Wrinkled

Crushed

Mercerized

Brushed

9. Transparency

Examples

Opaque

Semi Sheer

Sheer

Transparent

10. Seasonal Suitability

Examples

Summer

Winter

All Season

Festive

Layering

11. Premium Positioning

Examples

Luxury

Premium

Designer

Artisan

Heritage

Contemporary

Commercial

12. Fabric Detection Rules

Use Excel.

↓

If unavailable

Catalog Description.

↓

If unavailable

Visual AI.

↓

If unavailable

Fashion Reasoning.

Never overwrite Excel.

13. Multiple Fabric Rule

Always output in garment component order.

Example

Choli Fabric

↓

Silk Blend

Lehenga Fabric

↓

Silk Blend

Dupatta Fabric

↓

Net
14. Style Information Rule

Always use component-based labels.

Example

Kurta Fabric:
Silk Blend

Bottom Fabric:
Silk Blend

Dupatta Fabric:
Organza
15. Description Rule

Descriptions should naturally mention

Fabric feel
Texture
Movement
Breathability
Weight
Comfort
Luxury appeal

Never invent unsupported characteristics.

16. Care Rule

Care Instructions must be selected using

Fabric
Work
Dyeing
Finish
17. Confidence Rule

High

↓

Output

Medium

↓

Output if not contradicted

Low

↓

Omit

Never invent fabrics.

18. Universal Recognition Rule

FCOS shall recognize any commercially accepted textile supported by

Excel
Catalog Description
Visual AI
Fashion Reasoning

Unknown supplier names shall be normalized to accepted commercial terminology.

Enterprise Recommendations (FCOS v2.2)

To make Fabrics.md truly enterprise-grade, I recommend adding these advanced sections:

1. Fabric by Product Type ⭐⭐⭐⭐⭐

Define commonly used fabrics for each category.

Examples:

Product Type	Common Fabrics
Saree	Silk, Cotton, Georgette, Chiffon, Organza, Tissue
Lehenga	Silk Blend, Velvet, Georgette, Net, Brocade
Kurta	Cotton, Rayon, Linen, Silk Blend
Sherwani	Jacquard, Brocade, Silk
Co-Ord Set	Cotton, Rayon, Linen, Crepe
2. Fabric Composition Intelligence ⭐⭐⭐⭐⭐

Support blends and percentages when available.

Examples:

80% Cotton, 20% Linen
70% Viscose, 30% Polyester
Cotton Silk Blend
Linen Viscose Blend
3. Fabric Compatibility Matrix ⭐⭐⭐⭐⭐

Relate fabrics to construction and occasion.

Examples:

Organza → Festive, Lightweight, Structured
Georgette → Fluid Drape, Party Wear
Cotton → Casual, Office Wear
Velvet → Bridal, Winter
4. Fabric Performance Attributes ⭐⭐⭐⭐☆

Store internally:

Breathable
Moisture Wicking
Stretch
Wrinkle Resistant
Lightweight
Heavyweight
Soft Touch
Structured

These enrich descriptions and future filtering.

5. Regional & Heritage Textile Library ⭐⭐⭐⭐⭐

Include heritage textiles such as:

Banarasi Silk
Kanchipuram Silk
Patola
Ikat
Chanderi
Maheshwari
Kota Doria
Jamdani
Muga Silk
Eri Silk
Pochampally
Sambalpuri
Paithani
Bhagalpuri Silk

This is especially valuable for premium Indian ethnic wear and aligns with FCOS's luxury positioning.
