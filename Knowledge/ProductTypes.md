FCOS Enterprise
Universal Product Classification Engine

Version: 2.2
Status: Architecture Frozen

Purpose

This document defines the Universal Product Classification Engine used by FCOS Enterprise.

Its purpose is to accurately classify every fashion product into the correct commercial category using standardized fashion terminology.

The engine supports:

Women's Wear
Men's Wear
Boys Wear
Girls Wear
Jewellery

Excluded:

Footwear
Bags
Watches
Belts
Scarves
Baby Wear
Evidence Hierarchy

Always classify using

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Excel always wins.

Visual AI never overrides Excel.

Universal Classification Flow

FCOS shall determine

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

↓

Style Identity

↓

Design Aesthetic

↓

Occasion

This sequence is mandatory.

Women's Wear
Sarees

Saree

Ready To Wear Saree

Pre Draped Saree

Ruffle Saree

Lehenga Saree

Half Saree

Concept Saree

Belt Saree

Saree Gown

Pant Saree

Dhoti Saree

Salwar Suits

Salwar Suit

Designer Suit

Straight Suit

Pakistani Suit

Palazzo Suit

Pant Suit

Sharara Suit

Gharara Suit

Anarkali Suit

A-Line Suit

Jacket Suit

Cape Suit

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

Dresses

Maxi Dress

Midi Dress

Mini Dress

Kaftan Dress

Shirt Dress

Tiered Dress

Wrap Dress

Empire Dress

A-Line Dress

Bodycon Dress

Cape Dress

Lehengas

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

Co-Ord Sets

Top Pant Co-Ord

Shirt Pant Co-Ord

Skirt Co-Ord

Jacket Co-Ord

Cape Co-Ord

Men's Wear

Kurta

Kurta Pajama

Kurta Churidar

Kurta Pant

Jacket Kurta

Nehru Jacket Set

Sherwani

Indo Western Sherwani

Bandhgala

Achkan

Pathani Suit

Dhoti Kurta

Boys Wear

Kurta Pajama

Sherwani

Nehru Jacket Set

Waistcoat Set

Dhoti Set

Indo Western

Girls Wear

Lehenga Choli

Gown

Frock

Sharara Set

Kurti Set

Anarkali

Dress

Jewellery

Necklace

Choker

Pendant Set

Earrings

Jhumka

Stud

Ring

Bracelet

Bangle

Maang Tikka

Nose Ring

Anklet

Waist Belt

Brooch

Construction Intelligence

Construction is independent.

Examples

Peplum

Cape

Empire

Angrakha

Panelled

Tiered

Circular

Gathered

Kaftan

Layered

High Low

Straight

Silhouette Intelligence

Independent of Product Type.

Examples

Straight

Flared

Fit & Flare

Mermaid

A-Line

Relaxed

Slim

Oversized

Circular

Regular

Component Detection

Automatically identify

Top

Bottom

Dupatta

Cape

Jacket

Belt

Stole

Pallu

Blouse

Choli

Kurta

Pant

Palazzo

Sharara

Gharara

Dhoti

Skirt

Hybrid Product Detection

Examples

Cape Lehenga

Jacket Lehenga

Peplum Lehenga

Pant Saree

Saree Gown

Jacket Kurta

Layered Kurti

Kaftan Dress

Shirt Kurti

Ready To Wear Classification

Determine

Ready To Wear

Customized

Semi Stitched

Unstitched

Made To Measure

Jewellery

Style Identity

Examples

Minimal Luxe

Heritage Elegance

Contemporary Chic

Modern Classic

Bohemian Charm

Festive Glamour

Royal Heritage

Artisan Luxury

Indo Western Fusion

Timeless Grace

Design Aesthetic

Examples

Regal Heritage

Minimal Elegance

Modern Glamour

Vintage Revival

Contemporary Minimalism

Artisan Craft

Royal Opulence

Nature Inspired

Abstract Modern

Architectural

Product Naming Intelligence

If construction exists

↓

Use Construction Product Type.

Example

Cape Lehenga

NOT

Lehenga

Example

Peplum Kurti

NOT

Kurti

Unknown Products

If FCOS encounters an unknown product

↓

Classify using

Construction

Silhouette

Commercial Fashion Terminology

Never use

Other

Miscellaneous

Unknown

General Apparel

Confidence Rules

High

↓

Output

Medium

↓

Output if not contradicted

Low

↓

Omit

Never invent product types.

Enterprise Recommendations (FCOS v2.2)

To make ProductTypes.md truly world-class, I recommend adding these advanced intelligence layers:

1. Universal Product Relationship Matrix ⭐⭐⭐⭐⭐

Examples:

Parent Product	Valid Subtypes
Saree	Ready-to-Wear, Ruffle, Concept, Pant, Lehenga
Kurti	A-Line, Peplum, Angrakha, Kaftan
Lehenga	Bridal, Circular, Panelled, Tiered, Mermaid
Dress	Maxi, Midi, Kaftan, Wrap, Tiered

This prevents invalid subtype assignments.

2. Construction × Product Compatibility ⭐⭐⭐⭐⭐

Examples:

Peplum → Kurti, Lehenga, Suit, Top
Cape → Lehenga, Gown, Dress, Suit
Angrakha → Kurta, Kurti, Dress
Kaftan → Dress, Kurti, Suit

This improves both classification and naming.

3. Component Requirement Matrix ⭐⭐⭐⭐⭐

Define expected components:

Product Type	Expected Components
Saree	Saree, Blouse
Lehenga	Choli, Lehenga, Dupatta
Kurta Set	Kurta, Bottom
Sharara Set	Kurta, Sharara, Dupatta

This helps validate missing or incorrect component detection.

4. Occasion Mapping ⭐⭐⭐⭐☆

Associate common occasions:

Bridal Lehenga → Wedding
Cotton Kurti → Casual, Office Wear
Sherwani → Wedding, Reception
Party Gown → Cocktail, Evening

This supports more consistent occasion inference.

5. Global & Future Product Support ⭐⭐⭐⭐⭐

Instead of maintaining a closed list, add this architectural rule:

FCOS shall recognize, normalize, and classify any current or future fashion product using the Evidence Hierarchy (Excel → Catalog Description → Visual AI → Fashion Reasoning). Unknown products shall be mapped to the closest commercially accepted fashion terminology based on construction, silhouette, components, and intended use, without falling back to generic labels.

This single rule future-proofs the engine as new fashion categories emerge.
