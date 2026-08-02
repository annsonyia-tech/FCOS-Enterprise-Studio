FCOS Enterprise
Style Identity Library

Version: 1.0
Status: Architecture Frozen

Purpose

This document defines the Style Identity Library used by FCOS Enterprise.

Style Identity represents the fashion personality or styling character of a product.

It is independent of:

Product Type
Product Subtype
Construction
Silhouette
Pattern
Work Detail
Design Aesthetic

Style Identity answers the question:

"How would a fashion stylist describe the overall styling personality of this garment?"

Evidence Hierarchy

Always determine Style Identity using:

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Excel always overrides every other source.

Style Identity Categories
Heritage

Heritage Elegance

Royal Heritage

Timeless Heritage

Classic Heritage

Traditional Grace

Cultural Legacy

Artisan Heritage

Vintage Heritage

Luxury

Luxury Couture

Luxury Glamour

Luxury Minimalism

Luxury Elegance

Designer Luxury

Premium Craftsmanship

Modern Luxury

Contemporary

Contemporary Chic

Modern Chic

Urban Elegance

Modern Classic

Contemporary Grace

Minimal Chic

Festive

Festive Glamour

Festive Elegance

Celebration Ready

Occasion Luxe

Radiant Festive

Bridal

Bridal Grandeur

Regal Bridal

Royal Bride

Wedding Elegance

Couture Bride

Bridal Luxury

Minimal

Minimal Luxe

Modern Minimal

Contemporary Minimal

Elegant Simplicity

Quiet Luxury

Refined Minimalism

Indo-Western

Indo-Western Fusion

Fusion Chic

Modern Ethnic

Ethnic Contemporary

East Meets West

Bohemian

Bohemian Charm

Boho Luxe

Free Spirit

Artisan Bohemian

Contemporary Boho

Romantic

Romantic Elegance

Floral Romance

Soft Femininity

Graceful Romance

Elegant Bloom

Artisan

Artisan Luxury

Handcrafted Heritage

Craft Revival

Handloom Elegance

Traditional Artisan

Professional

Corporate Chic

Office Elegance

Smart Casual

Business Contemporary

Refined Professional

Casual

Everyday Comfort

Relaxed Chic

Weekend Style

Effortless Elegance

Contemporary Casual

Resort

Resort Luxe

Vacation Chic

Coastal Elegance

Holiday Glamour

Destination Style

Style Identity Rules

Style Identity describes the styling personality.

It is not:

Product Type
Occasion
Design Aesthetic
Pattern
Work
Determination Rules

Determine Style Identity using:

Construction
Silhouette
Fabric
Work
Styling
Fashion Positioning

Never determine Style Identity using colour alone.

Normalization Rules

Supplier

Designer Wear

↓

Designer Luxury

Supplier

Premium Collection

↓

Luxury Couture

Supplier

Traditional

↓

Heritage Elegance

Multiple Style Identity Rule

Output only one primary Style Identity.

Never output multiple values.

Style Information Rule

Example

Style Identity:
Artisan Luxury
Description Rule

Editorial descriptions should naturally reinforce the selected Style Identity without repeating the exact wording excessively.

Example

Style Identity:

Heritage Elegance

Description:

Inspired by timeless Indian craftsmanship with refined artisanal detailing...

Confidence Rule

High

↓

Output

Medium

↓

Output if supported

Low

↓

Omit

Never invent unsupported identities.

Universal Recognition Rule

FCOS shall recognize any current or future styling personality using:

Excel
Catalog Description
Visual AI
Fashion Reasoning

Unknown styling descriptions shall be normalized to the closest commercial Style Identity.

Enterprise Recommendations (FCOS v2.2)

To make StyleIdentity.md enterprise-grade, I recommend adding these intelligence layers:

1. Style Identity × Product Matrix ⭐⭐⭐⭐⭐
Product Type	Typical Style Identities
Bridal Lehenga	Bridal Grandeur, Royal Heritage
Cotton Kurti	Everyday Comfort, Contemporary Casual
Designer Saree	Heritage Elegance, Luxury Glamour
Sherwani	Royal Heritage, Luxury Couture
Co-Ord Set	Contemporary Chic, Urban Elegance
2. Style Identity × Construction Matrix ⭐⭐⭐⭐⭐

Examples:

Peplum → Contemporary Chic
Cape → Luxury Couture
Angrakha → Heritage Elegance
Kaftan → Resort Luxe
Jacket Layered → Indo-Western Fusion
3. Style Identity × Fabric Matrix ⭐⭐⭐⭐⭐

Examples:

Organza → Luxury Glamour
Linen → Quiet Luxury
Cotton → Everyday Comfort
Velvet → Royal Heritage
Silk → Heritage Elegance
4. Style Identity × Occasion Matrix ⭐⭐⭐⭐⭐

Examples:

Wedding → Bridal Grandeur
Office Wear → Corporate Chic
Casual → Relaxed Chic
Cocktail → Luxury Glamour
Resort → Vacation Chic
5. Controlled Vocabulary Rule ⭐⭐⭐⭐⭐

Maintain a fixed enterprise vocabulary of approximately 80–120 approved Style Identity values.

Do not generate new Style Identity names dynamically.
Always normalize supplier wording to the closest approved identity.
This ensures consistency across catalogs, SEO, filtering, and analytics.
My One Architectural Recommendation

I would make one small change to your terminology.

Instead of naming the file:

StyleIdentity.md

I recommend:

StyleIdentityLibrary.md

because it is a controlled vocabulary library, similar to:

Fabrics.md
WorkLibrary.md
OccasionLibrary.md
ProductSubtypes.md

This keeps your FCOS architecture consistent:

Knowledge files → Recognition, inference, normalization, and rules.
Library files → Approved enterprise vocabulary and classifications.
