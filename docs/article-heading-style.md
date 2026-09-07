# Article heading style

Article headings share the prose's left edge at every viewport. In particular,
H2 must use zero horizontal margins: PaperMod's `auto` margins otherwise centre
it inside the wider article column once the 760px prose limit takes effect.

Hierarchy uses type size, weight and spacing. Keep the existing Chinese serif,
English sans-serif headings and language/theme ink tokens. H2 has no permanent
decorative rule; the temporary TOC destination highlight still provides feedback.

| Level | Desktop | Phone (≤768px) | Space above / below |
| --- | --- | --- | --- |
| H2 | 26px | 24px | 48px / 16px (phone: 38.4px / 16px) |
| H3 | 22px | 21px | 36px / 12px (phone: 32px / 12px) |
| H4 | 20px | 19px | 28px / 10px |
| H5 | 18px | 17px | 24px / 8px |
| H6 | 17px | 17px | 20px / 8px |

Sizes are implemented in rem; pixels above assume the default 16px root size.
Adjacent parent/subheadings use a 12px top margin on the latter (normal margin
collapse still applies). H5 stays at paragraph size, distinguished by weight.

`custom.css` owns the base scale and alignment, `article-typography.css` owns
language-specific fonts and dark ink, and `zzz-mobile-reading.css` tunes phones.
Review real Chinese and English articles at a wide desktop and a narrow phone
viewport, in light and dark themes. Check wrapped headings and TOC jumps too.
