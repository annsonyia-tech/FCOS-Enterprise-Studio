FCOS Enterprise
Occasion Library

Version: 1.0
Status: Architecture Frozen

Purpose

This document is the master commercial reference library for all fashion occasions recognized by FCOS Enterprise.

The library standardizes occasion terminology across all supported categories.

Occasion Intelligence supports:

Product Classification
Product Description
SEO
Recommendation Engine
Occasion Filtering
Catalog Search
Fashion Styling
AI Merchandising
Evidence Hierarchy

Always determine Occasion using

Excel
↓

Catalog Description
↓

Visual AI
↓

Fashion Reasoning

Excel always overrides every other source.

Primary Occasion Categories
Everyday Wear

Casual

Daily Wear

Home Wear

Lounge Wear

Travel Wear

Resort Wear

Weekend Wear

Comfort Wear

Office

Office Wear

Business Casual

Corporate Wear

Professional Wear

Formal Office Wear

Festive

Festive Wear

Traditional Wear

Religious Ceremony

Temple Wear

Cultural Event

Festival Celebration

Wedding

Wedding

Wedding Ceremony

Bridal

Bridesmaid

Wedding Guest

Wedding Reception

Engagement Ceremony

Ring Ceremony

Indian Wedding Functions

Haldi

Mehendi

Sangeet

Cocktail

Reception

Roka

Tilak Ceremony

Baraat

Vidai

Pooja Ceremony

Party

Party Wear

Evening Party

Cocktail Party

Birthday Party

Anniversary Celebration

House Party

Family Gathering

Luxury

Luxury Occasion

Designer Event

Fashion Show

Red Carpet

Celebrity Event

High Tea

Premium Gathering

Traditional

Ethnic Celebration

Navratri

Diwali

Durga Puja

Ganesh Chaturthi

Onam

Pongal

Ugadi

Karva Chauth

Raksha Bandhan

Eid

Christmas Celebration

Baisakhi

Janmashtami

Formal

Formal Event

Black Tie

Reception

Award Ceremony

Convocation

Business Event

Conference

Vacation

Holiday

Cruise

Beach Vacation

Summer Holiday

Destination Wedding

Resort Stay

Seasonal

Spring

Summer

Monsoon

Autumn

Winter

Kids

Birthday

School Event

Festival

Family Function

Wedding

Party

Occasion Normalization

Normalize supplier wording.

Examples

Wedding Function

↓

Wedding

Marriage

↓

Wedding

Festival Wear

↓

Festive Wear

Party

↓

Party Wear

Office

↓

Office Wear

Multiple Occasion Rule

A product may have multiple occasions.

Maximum Output

Two occasions.

Example

Wedding

Reception

Example

Festive Wear

Party Wear

Never output more than two occasions.

Occasion Priority

When multiple occasions are possible

Use the strongest commercial selling occasion first.

Priority

Bridal
Wedding
Reception
Cocktail
Festive Wear
Party Wear
Office Wear
Casual
Occasion Selection Rules

Determine occasions using

Product Type

Construction

Fabric

Work Detail

Design Aesthetic

Style Identity

Visual Styling

Never use colour alone.

Occasion Compatibility

Examples

Bridal Lehenga

↓

Wedding

Reception

Cotton Kurti

↓

Casual

Office Wear

Heavy Embroidered Saree

↓

Wedding

Festive Wear

Printed Cotton Saree

↓

Office Wear

Casual

Style Information Rule

Output

Occasion:
Wedding

or

Occasion:
Wedding, Reception

Maximum two occasions.

Description Rule

Editorial descriptions should naturally reference the selected occasions.

Example

Perfect for weddings and engagement ceremonies.

Never introduce unsupported occasions.

Confidence Rule

High

↓

Output

Medium

↓

Output if not contradicted

Low

↓

Omit

Never invent occasions.

Universal Recognition Rule

FCOS shall recognize any current or future commercial fashion occasion using:

Excel
Catalog Description
Visual AI
Fashion Reasoning

Unknown occasion terminology shall be normalized to the closest accepted commercial occasion.

Enterprise Recommendations (FCOS v2.2)

To make OccasionLibrary.md enterprise-grade, I recommend adding these intelligence layers:

1. Occasion × Product Matrix ⭐⭐⭐⭐⭐
Product Type	Common Occasions
Bridal Lehenga	Wedding, Reception
Designer Saree	Wedding, Festive Wear
Cotton Kurti	Casual, Office Wear
Sherwani	Wedding, Reception
Co-Ord Set	Casual, Party Wear

This improves consistency and avoids unrealistic occasion assignments.

2. Occasion × Work Matrix ⭐⭐⭐⭐⭐

Examples:

Zardozi → Wedding, Reception
Gota Patti → Haldi, Mehendi
Mirror Work → Navratri, Mehendi
Chikankari → Casual, Festive Wear
Sequin Embroidery → Cocktail, Party Wear
3. Occasion × Fabric Matrix ⭐⭐⭐⭐⭐

Examples:

Organza → Party Wear, Festive Wear
Cotton → Casual, Office Wear
Velvet → Wedding, Winter Events
Georgette → Party Wear, Reception
Silk → Wedding, Festive Wear
4. Occasion Priority Engine ⭐⭐⭐⭐⭐

Define conflict resolution rules.

Example:

A heavily embroidered silk bridal lehenga may qualify for:

Wedding
Reception
Cocktail
Festive Wear

FCOS should output only the top two based on commercial priority.

5. Global Occasion Support ⭐⭐⭐⭐⭐

Future-proof FCOS by including internationally recognized occasions:

Prom
Graduation
Gala
Charity Ball
Bridal Shower
Baby Shower
Engagement Party
Destination Wedding
Garden Party
Evening Gala

This allows FCOS to support global catalogs without changing the core architecture.
