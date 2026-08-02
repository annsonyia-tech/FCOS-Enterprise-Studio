# FCOS AI Studio Enterprise
# Size Rules Specification

Version: 1.0
Status: Architecture Freeze
Module: Size Intelligence Engine

---

# 1. Purpose

Defines all size processing, normalization, validation, conversion, and output rules used by FCOS AI Studio Enterprise.

Universal FCOS specifications remain applicable unless explicitly overridden.

---

# 2. Evidence Hierarchy

Size shall always follow:

Excel

↓

Catalog Description

↓

Visual AI

↓

Fashion Reasoning

Higher-priority evidence shall never be overridden.

---

# 3. Universal Size Rules

FCOS shall always use the manufacturer-provided size whenever available.

Visual AI shall only infer size when:

• Excel does not provide size.

• Catalog Description does not provide size.

• Visual confidence is sufficient.

If confidence is insufficient,

omit the size.

Never invent or hallucinate size values.

---

# 4. Body Size Labels

FCOS shall use category-specific body size labels.

Women's Apparel

→ Bust Size

Men's Apparel

→ Chest Size

Boys' Apparel

→ Chest Size

Girls' Apparel

→ Chest Size

Non-fitted Products

→ Free Size

Examples:

Bust Size: 40–44 Inches

Chest Size: 38–42 Inches

Free Size: 38–42 Inches

---

# 5. Size Conversion Rules

Letter sizes shall be normalized whenever reliable measurements exist.

Examples

XS

↓

Bust Size: 32–34 Inches

S

↓

Bust Size: 34–36 Inches

M

↓

Bust Size: 36–38 Inches

L

↓

Bust Size: 38–40 Inches

XL

↓

Bust Size: 40–42 Inches

XXL

↓

Bust Size: 42–44 Inches

XXXL

↓

Bust Size: 44–46 Inches

If exact manufacturer measurements are available,

manufacturer measurements shall always take precedence.

---

# 6. Multiple Size Rules

If multiple consecutive sizes are available,

convert into one continuous range.

Examples

36,38,40,42

↓

Bust Size: 36–42 Inches

38,40,42,44

↓

Bust Size: 38–44 Inches

---

# 7. Stitched Garment Rules

Manufacturer stitched size shall include available margin.

Example

Blouse Size Stitched 40" (Margin 4")

↓

Bust Size: 40–44 Inches

Kurta Size 42" (Margin 2")

↓

Bust Size: 42–44 Inches

Always use the manufacturer-provided margin.

---

# 8. Free Size Rules

Free Size products shall use manufacturer-supported ranges.

Examples

Free Size

↓

38–42 Inches

Free Size up to 44

↓

38–44 Inches

Free Size up to 46

↓

38–46 Inches

Never invent Free Size ranges.

---

# 9. Jewellery Size Rules

Jewellery dimensions shall follow manufacturer specifications.

Do not convert jewellery dimensions into Bust Size or Chest Size.

---

# 10. Style Information Rules

Size shall always be the first attribute.

Examples

Bust Size

↓

Colour

↓

Fabric

↓

Length

↓

Construction

↓

Silhouette

↓

Fit

...

---

# 11. Product Category Rules

Women's Wear

Always output Bust Size.

Men's Wear

Always output Chest Size.

Kids' Wear

Always output Chest Size.

Sarees, Dupattas, Shawls, Stoles

Output Free Size only when applicable.

Jewellery

Omit size unless manufacturer specifies dimensions.

---

# 12. Validation Rules

Validation Engine shall verify:

• Correct evidence hierarchy

• Correct body size label

• Correct size normalization

• Correct stitched margin conversion

• Correct Free Size conversion

• No hallucinated sizes

• Style Information begins with Size

---

# 13. Output Rules

Output Examples

Bust Size: 40–44 Inches

Chest Size: 38–42 Inches

Free Size: 38–46 Inches

Maintain consistent formatting across the catalog.

---

# 14. Future Compatibility

FCOS shall automatically support future size systems, international sizing standards, and product categories without requiring architectural changes.
