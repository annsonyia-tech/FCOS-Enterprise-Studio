# FCOS AI Studio Enterprise
# Jewellery Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Fashion Intelligence Engine

---

# 1. Purpose

This document defines all processing, classification, styling, measurement, validation, and output rules specific to Jewellery within FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden by this document.

---

# 2. Scope

FCOS shall support and classify all current and future jewellery categories using the Enterprise Evidence Hierarchy.

Supported categories include but are not limited to:

Necklace

Choker

Pendant

Pendant Set

Earrings

Stud Earrings

Drop Earrings

Hoop Earrings

Jhumka

Chandbali

Maang Tikka

Passa

Nose Ring

Bangles

Bracelets

Kada

Finger Ring

Toe Ring

Waist Belt (Kamarbandh)

Anklet (Payal)

Temple Jewellery

Bridal Jewellery

Jewellery Set

Future jewellery product types shall automatically inherit FCOS universal architecture.

---

# 3. Evidence Hierarchy

All jewellery attributes shall be resolved using:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 4. Product Classification

FCOS shall independently identify:

- Product Type
- Product Subtype
- Jewellery Components
- Jewellery Style
- Jewellery Construction
- Ornament Category
- Set Composition

Visual construction shall always take precedence over generic naming.

---

# 5. Colour Rules

Colour shall follow:

Excel

↓

Catalog Description

↓

Visual AI

Never override Excel colour.

---

# 6. Material Rules

Maintain component-specific material information.

Examples

Base Metal

Brass

Copper

Silver Alloy

German Silver

Alloy

Sterling Silver

Gold Plated

Rose Gold Plated

Oxidized Silver

Enamel

Pearls

Beads

Stones

Kundan

Polki

American Diamond

Cubic Zirconia

Crystal

Resin

---

# 7. Jewellery Component Detection

FCOS shall independently detect:

Pendant

Chain

Necklace

Earrings

Bangles

Bracelets

Ring

Maang Tikka

Passa

Nose Ring

Waist Belt

Anklet

Hair Accessory

Each component shall retain its own material and decorative attributes.

---

# 8. Construction Detection

Examples include:

Layered

Multi-Strand

Single Strand

Statement

Adjustable

Openable

Flexible

Rigid

Linked

Handcrafted

Temple Style

Contemporary

Construction describes how the jewellery is built.

---

# 9. Finish Detection

Examples

Gold Finish

Silver Finish

Rose Gold Finish

Oxidized Finish

Matte Finish

Gloss Finish

Antique Finish

Dual Tone Finish

---

# 10. Stone Detection

Examples

Kundan

Polki

American Diamond

Cubic Zirconia

Crystal

Pearl

Semi Precious Stone

Natural Stone

Synthetic Stone

Glass Stone

---

# 11. Decorative Work Detection

Examples

Temple Work

Meenakari

Filigree

Nakshi

Kundan Setting

Polki Setting

Pearl Work

Bead Work

Stone Work

Hand Carving

Laser Cut

Enamel Work

---

# 12. Size & Dimension Rules

Follow:

Excel

↓

Catalog Description

↓

Visual AI

Examples

Necklace Length

Pendant Size

Earring Length

Bangle Diameter

Ring Size

Bracelet Length

Waist Belt Length

Anklet Length

Never estimate dimensions when confidence is insufficient.

If unavailable, omit the field.

---

# 13. Jewellery Style Detection

Examples

Minimal

Classic

Statement

Traditional

Contemporary

Bridal

Temple

Bohemian

Fusion

Vintage

Royal

---

# 14. Occasion Detection

Examples

Daily Wear

Office Wear

Festive Wear

Wedding

Reception

Cocktail

Haldi

Mehendi

Sangeet

Bridal

Party

---

# 15. Style Type

Examples

Royal Heritage

Minimal Luxe

Modern Glamour

Classic Elegance

Festive Splendour

Timeless Luxury

Temple Grandeur

Contemporary Chic

---

# 16. Design Aesthetic

Examples

Regal Heritage

Royal Opulence

Artisan Craft

Vintage Revival

Minimal Elegance

Modern Glamour

Contemporary Luxury

Temple Heritage

---

# 17. Category Type Examples

Examples

Designer Necklace

Bridal Necklace Set

Temple Jewellery Set

Designer Jhumka

Designer Chandbali

Designer Bangles

Designer Bracelet

Designer Ring

Designer Anklet

Designer Maang Tikka

---

# 18. Ready-to-Wear Classification

Jewellery shall always be classified as:

Jewellery

No Ready-to-Wear or Customized apparel logic shall be applied.

---

# 19. Jewellery Style Information Rules

Jewellery Style Information shall follow the Universal FCOS Jewellery format.

Material →
Finish →
Stone →
Decorative Work →
Occasion →
Style Type →
Design Aesthetic →
Category Type

Only include attributes supported by available evidence.

---

# 20. Care Instruction

Always use:

Avoid water, perfumes, and harsh chemicals. Store in a soft pouch and wipe with a dry cloth after use. Remove before bathing, swimming, exercising, or sleeping.

---

# 21. Delivery Information

Always use:

Expertly packed for secure delivery and shipped worldwide within 7–10 days.

---

# 22. Jewellery Output Rules

The Universal FCOS Output Specification shall apply.

Jewellery outputs shall generate:

- SEO Product Name
- Jewellery Style Information
- Individual Description
- Care Instruction
- Delivery Information
- Validation Report
- Excel Output

---

# 23. Jewellery Validation Rules

The Validation Engine shall verify:

- 5–8 word SEO Product Name
- Unique Product Name
- Correct Product Classification
- Correct Component Detection
- Correct Material Classification
- Correct Finish Classification
- Correct Stone Classification
- Correct Style Information Order
- 150–180 word Individual Description
- Valid HTML Structure
- No Hallucinated Attributes
- 1:1 Image-to-Row Mapping
- Zero Validation Errors
