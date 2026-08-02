FCOS Enterprise
Product Subtype Intelligence Engine

Version: 1.0
Status: Architecture Frozen

Purpose

This document defines the Product Subtype Intelligence Engine used by FCOS Enterprise.

Its purpose is to classify garments into commercially recognized subtypes after the Product Type has been identified.

Product Subtype provides a more specific merchandising classification based on construction, silhouette, components, styling, and intended commercial identity.

Evidence Hierarchy

Always determine Product Subtype using

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Excel always overrides every other source.

Classification Flow
Category

↓

Product Type

↓

Product Subtype

↓

Construction

↓

Silhouette

↓

Components

Product Type must always be determined before Product Subtype.

Women's Wear
Sarees

Product Type

Saree

Possible Product Subtypes

Designer Saree

Printed Saree

Embroidered Saree

Party Wear Saree

Wedding Saree

Ready To Wear Saree

Pre Draped Saree

Ruffle Saree

Lehenga Saree

Pant Saree

Concept Saree

Belt Saree

Saree Gown

Half Saree

Silk Saree

Cotton Saree

Banarasi Saree

Kanchipuram Saree

Organza Saree

Georgette Saree

Lehengas

Product Type

Lehenga

Possible Product Subtypes

Designer Lehenga

Bridal Lehenga

Panelled Lehenga

Tiered Lehenga

Circular Lehenga

Layered Lehenga

Fish Cut Lehenga

Mermaid Lehenga

A-Line Lehenga

Printed Lehenga

Embroidered Lehenga

Jacket Lehenga

Cape Lehenga

Peplum Lehenga

Salwar Suits

Designer Kurta Set

Straight Kurta Set

Anarkali Suit

Pakistani Suit

Sharara Suit

Gharara Suit

Palazzo Suit

Pant Suit

Cape Suit

Jacket Suit

Peplum Suit

Layered Suit

Kaftan Suit

Kurtis

Straight Kurti

A-Line Kurti

Peplum Kurti

Empire Kurti

High Low Kurti

Layered Kurti

Kaftan Kurti

Angrakha Kurti

Panelled Kurti

Shirt Kurti

Asymmetric Kurti

Printed Kurti

Embroidered Kurti

Dresses

Maxi Dress

Midi Dress

Mini Dress

Tiered Dress

Kaftan Dress

Shirt Dress

Wrap Dress

Empire Dress

Cape Dress

A-Line Dress

Bodycon Dress

Fit & Flare Dress

Co-Ord Sets

Printed Co-Ord Set

Embroidered Co-Ord Set

Shirt Co-Ord Set

Top Pant Co-Ord Set

Skirt Co-Ord Set

Jacket Co-Ord Set

Cape Co-Ord Set

Men's Wear

Designer Kurta

Kurta Pajama

Kurta Churidar

Kurta Pant Set

Jacket Kurta Set

Nehru Jacket Set

Sherwani Set

Indo-Western Sherwani

Bandhgala Suit

Achkan

Pathani Suit

Dhoti Kurta Set

Boys Wear

Kurta Pajama Set

Sherwani Set

Waistcoat Set

Nehru Jacket Set

Dhoti Kurta Set

Indo-Western Set

Girls Wear

Designer Lehenga Choli

Printed Lehenga Choli

Embroidered Lehenga Choli

Sharara Set

Anarkali Set

Kurti Set

Gown

Party Dress

Frock

Jewellery

Choker Necklace

Layered Necklace

Pendant Set

Temple Necklace

Jhumka Earrings

Stud Earrings

Drop Earrings

Bracelet

Bangle

Maang Tikka

Nose Ring

Anklet

Waist Belt

Brooch

Subtype Rules

Subtype shall represent the commercially sellable version of a product.

Example

Product Type

Lehenga

Subtype

Designer Lehenga

NOT

Tiered

Construction Rule

Construction is independent.

Correct

Product Type

Lehenga

Subtype

Designer Lehenga

Construction

Tiered

Silhouette

Flared

Silhouette Rule

Silhouette is independent.

Never use silhouette as Product Subtype unless it is commercially accepted.

Correct

Silhouette

Mermaid

Subtype

Mermaid Lehenga

Only if Mermaid is a recognized commercial subtype.

Component Rule

Components do not determine Product Subtype.

Example

Kurta + Pant + Dupatta

↓

Designer Kurta Set

NOT

Three Piece Set

Naming Rule

SEO Product Name shall use

Product Subtype

only when required by duplicate colour rules or when it improves commercial clarity.

Unknown Subtypes

If FCOS encounters an unknown subtype

↓

Determine using

Construction

Silhouette

Commercial Fashion Terminology

Never output

Other

Miscellaneous

General Apparel

Confidence Rules

High

↓

Output Product Subtype

Medium

↓

Output only if supported

Low

↓

Omit Product Subtype

Never invent subtypes.

Universal Recognition Rule

FCOS shall recognize any current or future product subtype supported by:

Excel
Catalog Description
Visual AI
Fashion Reasoning

Unknown products shall be mapped to the closest commercially accepted subtype using construction, silhouette, garment components, and merchandising conventions.

Enterprise Recommendations (FCOS v2.2)

To make ProductSubtypes.md truly enterprise-grade, I recommend these additions:

1. Parent–Child Hierarchy ⭐⭐⭐⭐⭐

Maintain an explicit hierarchy:

Product Type	Valid Product Subtypes
Saree	Designer Saree, Printed Saree, Ready-to-Wear Saree, Ruffle Saree
Lehenga	Designer Lehenga, Bridal Lehenga, Tiered Lehenga, Jacket Lehenga
Kurta Set	Designer Kurta Set, Jacket Kurta Set, Anarkali Kurta Set

This prevents assigning invalid subtypes to a product.

2. Mutual Exclusivity Rules ⭐⭐⭐⭐⭐

Some subtypes cannot coexist.

For example:

Ready-to-Wear Saree and Unstitched Saree should never both be assigned.
Mermaid Lehenga and Circular Lehenga are generally mutually exclusive.
3. Subtype Priority Rules ⭐⭐⭐⭐⭐

When multiple valid subtype candidates exist, prioritize by commercial significance.

Example:

Jacket Lehenga (construction-based) takes precedence over Printed Lehenga (surface decoration) because it better identifies what the customer is buying.
4. SEO Integration ⭐⭐⭐⭐⭐

Define exactly when Product Subtype should appear in the SEO name:

Use only if required by your duplicate-colour naming formula.
Or when the subtype is the primary differentiator (e.g., Jacket Kurta Set vs Kurta Set).
5. Regression Validation ⭐⭐⭐⭐⭐

Require validation that:

Every Product Subtype belongs to its parent Product Type.
No subtype exists without a valid Product Type.
Output terminology remains consistent across the catalog.
