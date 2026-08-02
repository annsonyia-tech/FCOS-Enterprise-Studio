# FCOS AI Studio Enterprise
# Colour Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Colour Intelligence Engine

---

# 1. Purpose

This document defines all colour processing, normalization, validation, and output rules used by FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden by this document.

---

# 2. Evidence Hierarchy

Colour shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Colour Priority Rules

Rule 1

If Excel contains Colour,

Always use Excel Colour.

Never override it.

---

Rule 2

If Excel Colour is unavailable,

Use Catalog Description Colour.

---

Rule 3

If both Excel and Catalog Description are unavailable,

Visual AI may determine the commercial colour.

---

Rule 4

If Visual AI confidence is insufficient,

Omit Colour.

Never invent a colour.

---

# 4. Commercial Colour Rules

Always output the commercial colour.

Examples

Black

White

Red

Navy Blue

Wine

Mustard

Rani Pink

Bottle Green

Olive Green

Never output RGB values.

Never output hexadecimal colours.

Never output colour codes.

---

# 5. Colour Normalization

Normalize colour names.

Examples

Fuchsia

↓

Rani Pink

Maroon Red

↓

Maroon

Dark Navy

↓

Navy Blue

Off White

↓

Off White

Grey Melange

↓

Grey Melange

---

# 6. Multiple Colour Rules

Single Colour

Output one colour.

Examples

Black

Mustard

Wine

---

Dual Colour

Output primary commercial colour.

Do not invent secondary colours.

---

Multicolour Products

Use

Multicolour

only when supported by the catalog.

---

# 7. Product Naming Rules

Colour shall always be the first element.

Example

Wine Zari Silk Blend Saree

Never omit colour when available.

---

# 8. Style Information Rules

Colour shall always immediately follow Size.

Examples

Bust Size

↓

Colour

↓

Fabric

↓

Length

---

# 9. Description Rules

Colour may naturally appear in Paragraph 1.

Never repeat colour excessively.

Do not keyword stuff.

---

# 10. Duplicate Detection Rules

Colour shall participate in Product Name uniqueness.

Examples

Black

↓

Black Zari Silk Blend Saree

If duplicate

↓

Black Zari Silk Blend Designer Saree

If still duplicate

↓

Black Zari Silk Blend Designer Heritage Saree

---

# 11. Validation Rules

Validation Engine shall verify:

• Colour exists when supported

• Excel colour never overridden

• Normalized commercial colour used

• Product Name colour matches Style Information

• Colour matches workbook

• No colour hallucination

---

# 12. Future Compatibility

Future commercial colours shall automatically inherit these rules.
