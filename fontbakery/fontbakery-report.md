## Fontbakery report

Fontbakery version: 0.8.5

<details>
<summary><b>[1] Family checks</b></summary>
<details>
<summary>💔 <b>ERROR:</b> Check README.md has a sample image.</summary>

* [com.google.fonts/check/repo/sample_image](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/repo/sample_image)
<pre>--- Rationale ---
In order to showcase what a font family looks like, the project&#x27;s README.md file
should ideally include a sample image and highlight it in the upper portion of
the document, no more than 10 lines away from the top of the file.</pre>

* 💔 **ERROR** Failed with AttributeError: 'NoneType' object has no attribute 'split'

</details>
<br>
</details>
<details>
<summary><b>[24] occasional29-Regular.ttf</b></summary>
<details>
<summary>💔 <b>ERROR:</b> Check `Google Fonts Latin Core` glyph coverage.</summary>

* [com.google.fonts/check/glyph_coverage](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/glyph_coverage)
<pre>--- Rationale ---
Google Fonts expects that fonts in its collection support at least the minimal
set of characters defined in the `GF-latin-core` glyph-set.</pre>

* 💔 **ERROR** Failed with TypeError: name() argument 1 must be a unicode character, not int

</details>
<details>
<summary>💔 <b>ERROR:</b> Check for METADATA subsets with zero support.</summary>

* [com.google.fonts/check/metadata/unsupported_subsets](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/metadata/unsupported_subsets)
<pre>--- Rationale ---
This check ensures that the subsets specified on a METADATA.pb file are actually
supported (even if only partially) by the font files.
Subsets for which none of the codepoints are supported will cause the check to
FAIL.</pre>

* 💔 **ERROR** Failed with AttributeError: 'NoneType' object has no attribute 'subsets'

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 fsType does not impose restrictions.</summary>

* [com.google.fonts/check/fstype](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/fstype)
<pre>--- Rationale ---
The fsType in the OS/2 table is a legacy DRM-related field. Fonts in the Google
Fonts collection must have it set to zero (also known as &quot;Installable
Embedding&quot;). This setting indicates that the fonts can be embedded in documents
and permanently installed by applications on remote systems.
More detailed info is available at:
https://docs.microsoft.com/en-us/typography/opentype/spec/os2#fstype</pre>

* 🔥 **FAIL** In this font fsType is set to 8 meaning that:
The font may be embedded but must only be installed temporarily on other systems.

No such DRM restrictions can be enabled on the Google Fonts collection, so the fsType field must be set to zero (Installable Embedding) instead. [code: drm]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check license file has good copyright string.</summary>

* [com.google.fonts/check/license/OFL_copyright](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/license/OFL_copyright)
<pre>--- Rationale ---
An OFL.txt file&#x27;s first line should be the font copyright e.g:
&quot;Copyright 2019 The Montserrat Project Authors
(https://github.com/julietaula/montserrat)&quot;</pre>

* 🔥 **FAIL** First line in license file does not match expected format: "copyright 20** the my font project authors (https://github.com/googlefonts/my-font-repository)"

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check copyright namerecords match license file.</summary>

* [com.google.fonts/check/name/license](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/name/license)
<pre>--- Rationale ---
A known licensing description must be provided in the NameID 14 (LICENSE
DESCRIPTION) entries of the name table.
The source of truth for this check (to determine which license is in use) is a
file placed side-by-side to your font project including the licensing terms.
Depending on the chosen license, one of the following string snippets is
expected to be found on the NameID 13 (LICENSE DESCRIPTION) entries of the name
table:
- &quot;This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is available with a FAQ at: https://scripts.sil.org/OFL&quot;
- &quot;Licensed under the Apache License, Version 2.0&quot;
- &quot;Licensed under the Ubuntu Font Licence 1.0.&quot;
Currently accepted licenses are Apache or Open Font License.
For a small set of legacy families the Ubuntu Font License may be acceptable as
well.
When in doubt, please choose OFL for new font projects.</pre>

* 🔥 **FAIL** Font lacks NameID 13 (LICENSE DESCRIPTION). A proper licensing entry must be set. [code: missing]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check name table: FONT_FAMILY_NAME entries.</summary>

* [com.google.fonts/check/name/familyname](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/name/familyname)
<pre>--- Rationale ---
Checks that the family name infered from the font filename matches the string at
nameID 1 (NAMEID_FONT_FAMILY_NAME) if it conforms to RIBBI and otherwise checks
that nameID 1 is the family name + the style name.</pre>

* 🔥 **FAIL** Entry [FONT_FAMILY_NAME(1):WINDOWS(3)] on the "name" table: Expected "occasional 29" but got "occasional29". [code: mismatch]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check name table: FULL_FONT_NAME entries.</summary>

* [com.google.fonts/check/name/fullfontname](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/name/fullfontname)
<pre>--- Rationale ---
Requirements for the FULL_FONT_NAME entries in the &#x27;name&#x27; table.</pre>

* 🔥 **FAIL** [FULL_FONT_NAME(4):WINDOWS(3)]
Expected: "occasional 29 Regular"
But got:  "occasional29 Regular" [code: bad-entry]

</details>
<details>
<summary>🔥 <b>FAIL:</b> OS/2.fsSelection bit 7 (USE_TYPO_METRICS) is set in all fonts.</summary>

* [com.google.fonts/check/os2/use_typo_metrics](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/os2/use_typo_metrics)
<pre>--- Rationale ---
All fonts on the Google Fonts collection should have OS/2.fsSelection bit 7
(USE_TYPO_METRICS) set. This requirement is part of the vertical metrics scheme
established as a Google Fonts policy aiming at a common ground supported by all
major font rendering environments.
For more details, read:
https://github.com/googlefonts/gf-docs/blob/main/VerticalMetrics/README.md
Below is the portion of that document that is most relevant to this check:
Use_Typo_Metrics must be enabled. This will force MS Applications to use the
OS/2 Typo values instead of the Win values. By doing this, we can freely set the
Win values to avoid clipping and control the line height with the typo values.
It has the added benefit of future line height compatibility. When a new script
is added, we simply change the Win values to the new yMin and yMax, without
needing to worry if the line height have changed.</pre>

* 🔥 **FAIL** OS/2.fsSelection bit 7 (USE_TYPO_METRICS) wasNOT set in the following fonts: ['fonts/ttf/occasional29-Regular.ttf']. [code: missing-os2-fsselection-bit7]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 usWinAscent & usWinDescent.</summary>

* [com.google.fonts/check/family/win_ascent_and_descent](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/family/win_ascent_and_descent)
<pre>--- Rationale ---
A font&#x27;s winAscent and winDescent values should be greater than the head table&#x27;s
yMax, abs(yMin) values. If they are less than these values, clipping can occur
on Windows platforms (https://github.com/RedHatBrand/Overpass/issues/33).
If the font includes tall/deep writing systems such as Arabic or Devanagari, the
winAscent and winDescent can be greater than the yMax and abs(yMin) to
accommodate vowel marks.
When the win Metrics are significantly greater than the upm, the linespacing can
appear too loose. To counteract this, enabling the OS/2 fsSelection bit 7
(Use_Typo_Metrics), will force Windows to use the OS/2 typo values instead. This
means the font developer can control the linespacing with the typo values,
whilst avoiding clipping by setting the win values to values greater than the
yMax and abs(yMin).</pre>

* 🔥 **FAIL** OS/2.usWinDescent value should be equal or greater than 374, but got 265 instead. [code: descent]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 Metrics match hhea Metrics.</summary>

* [com.google.fonts/check/os2_metrics_match_hhea](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/os2_metrics_match_hhea)
<pre>--- Rationale ---
OS/2 and hhea vertical metric values should match. This will produce the same
linespacing on Mac, GNU+Linux and Windows.
- Mac OS X uses the hhea values.
- Windows uses OS/2 or Win, depending on the OS or fsSelection bit value.
When OS/2 and hhea vertical metrics match, the same linespacing results on
macOS, GNU+Linux and Windows. Unfortunately as of 2018, Google Fonts has
released many fonts with vertical metrics that don&#x27;t match in this way. When we
fix this issue in these existing families, we will create a visible change in
line/paragraph layout for either Windows or macOS users, which will upset some
of them.
But we have a duty to fix broken stuff, and inconsistent paragraph layout is
unacceptably broken when it is possible to avoid it.
If users complain and prefer the old broken version, they have the freedom to
take care of their own situation.</pre>

* 🔥 **FAIL** OS/2 sTypoAscender (800) and hhea ascent (935) must be equal. [code: ascender]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Font contains glyphs for whitespace characters?</summary>

* [com.google.fonts/check/whitespace_glyphs](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/whitespace_glyphs)

* 🔥 **FAIL** Whitespace glyph missing for codepoint 0x00A0. [code: missing-whitespace-glyph-0x00A0]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check glyphs do not have duplicate components which have the same x,y coordinates.</summary>

* [com.google.fonts/check/glyf_non_transformed_duplicate_components](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/glyf.html#com.google.fonts/check/glyf_non_transformed_duplicate_components)
<pre>--- Rationale ---
There have been cases in which fonts had faulty double quote marks, with each of
them containing two single quote marks as components with the same x, y
coordinates which makes them visually look like single quote marks.
This check ensures that glyphs do not contain duplicate components which have
the same x,y coordinates.</pre>

* 🔥 **FAIL** The following glyphs have duplicate components which have the same x,y coordinates:
	* {'glyph': 'quotedblbase', 'component': 'comma', 'x': 0, 'y': 0} [code: found-duplicates]

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking OS/2 achVendID.</summary>

* [com.google.fonts/check/vendor_id](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/vendor_id)
<pre>--- Rationale ---
Microsoft keeps a list of font vendors and their respective contact info. This
list is updated regularly and is indexed by a 4-char &quot;Vendor ID&quot; which is stored
in the achVendID field of the OS/2 table.
Registering your ID is not mandatory, but it is a good practice since some
applications may display the type designer / type foundry contact info on some
dialog and also because that info will be visible on Microsoft&#x27;s website:
https://docs.microsoft.com/en-us/typography/vendors/
This check verifies whether or not a given font&#x27;s vendor ID is registered in
that list or if it has some of the default values used by the most common font
editors.
Each new FontBakery release includes a cached copy of that list of vendor IDs.
If you registered recently, you&#x27;re safe to ignore warnings emitted by this
check, since your ID will soon be included in one of our upcoming releases.</pre>

* ⚠ **WARN** OS/2 VendorID value 'NONE' is not yet recognized. If you registered it recently, then it's safe to ignore this warning message. Otherwise, you should set it to your own unique 4 character code, and register it with Microsoft at https://www.microsoft.com/typography/links/vendorlist.aspx
 [code: unknown]

</details>
<details>
<summary>⚠ <b>WARN:</b> Font has old ttfautohint applied?</summary>

* [com.google.fonts/check/old_ttfautohint](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/old_ttfautohint)
<pre>--- Rationale ---
Check if font has been hinted with an outdated version of ttfautohint.</pre>

* ⚠ **WARN** ttfautohint used in font = 1.8.3; latest = 1.8.4; Need to re-run with the newer version! [code: old-ttfa]

</details>
<details>
<summary>⚠ <b>WARN:</b> Ensure fonts have ScriptLangTags declared on the 'meta' table.</summary>

* [com.google.fonts/check/meta/script_lang_tags](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/meta/script_lang_tags)
<pre>--- Rationale ---
The OpenType &#x27;meta&#x27; table originated at Apple. Microsoft added it to OT with
just two DataMap records:
- dlng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font is designed for
- slng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font supports
The slng structure is intended to describe which languages and scripts the font
overall supports. For example, a Traditional Chinese font that also contains
Latin characters, can indicate Hant,Latn, showing that it supports Hant, the
Traditional Chinese variant of the Hani script, and it also supports the Latn
script
The dlng structure is far more interesting. A font may contain various glyphs,
but only a particular subset of the glyphs may be truly &quot;leading&quot; in the design,
while other glyphs may have been included for technical reasons. Such a
Traditional Chinese font could only list Hant there, showing that it’s designed
for Traditional Chinese, but the font would omit Latn, because the developers
don’t think the font is really recommended for purely Latin-script use.
The tags used in the structures can comprise just script, or also language and
script. For example, if a font has Bulgarian Cyrillic alternates in the locl
feature for the cyrl BGR OT languagesystem, it could also indicate in dlng
explicitly that it supports bul-Cyrl. (Note that the scripts and languages in
meta use the ISO language and script codes, not the OpenType ones).
This check ensures that the font has the meta table containing the slng and dlng
structures.
All families in the Google Fonts collection should contain the &#x27;meta&#x27; table.
Windows 10 already uses it when deciding on which fonts to fall back to. The
Google Fonts API and also other environments could use the data for smarter
filtering. Most importantly, those entries should be added to the Noto fonts.
In the font making process, some environments store this data in external files
already. But the meta table provides a convenient way to store this inside the
font file, so some tools may add the data, and unrelated tools may read this
data. This makes the solution much more portable and universal.</pre>

* ⚠ **WARN** This font file does not have a 'meta' table. [code: lacks-meta-table]

</details>
<details>
<summary>⚠ <b>WARN:</b> Check font contains no unreachable glyphs</summary>

* [com.google.fonts/check/unreachable_glyphs](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/unreachable_glyphs)
<pre>--- Rationale ---
Glyphs are either accessible directly through Unicode codepoints or through
substitution rules. Any glyphs not accessible by either of these means are
redundant and serve only to increase the font&#x27;s file size.</pre>

* ⚠ **WARN** The following glyphs could not be reached by codepoint or substitution rules:
 - pique
 - stroke.t
 - bole
 - sortie_courte
 - _attaque_bdhklpd
 - stem_upp
 - _serif_cap_long
 - ud
 - t_barre
 - nouveauGlyphe 
 - And 3 more.

Use -F or --full-lists to disable shortening of long lists.
 [code: unreachable-glyphs]

</details>
<details>
<summary>⚠ <b>WARN:</b> Check if each glyph has the recommended amount of contours.</summary>

* [com.google.fonts/check/contour_count](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/contour_count)
<pre>--- Rationale ---
Visually QAing thousands of glyphs by hand is tiring. Most glyphs can only be
constructured in a handful of ways. This means a glyph&#x27;s contour count will only
differ slightly amongst different fonts, e.g a &#x27;g&#x27; could either be 2 or 3
contours, depending on whether its double story or single story.
However, a quotedbl should have 2 contours, unless the font belongs to a display
family.
This check currently does not cover variable fonts because there&#x27;s plenty of
alternative ways of constructing glyphs with multiple outlines for each feature
in a VarFont. The expected contour count data for this check is currently
optimized for the typical construction of glyphs in static fonts.</pre>

* ⚠ **WARN** This check inspects the glyph outlines and detects the total number of contours in each of them. The expected values are infered from the typical ammounts of contours observed in a large collection of reference font families. The divergences listed below may simply indicate a significantly different design on some of your glyphs. On the other hand, some of these may flag actual bugs in the font such as glyphs mapped to an incorrect codepoint. Please consider reviewing the design and codepoint assignment of these to make sure they are correct.

The following glyphs do not have the recommended number of contours:

 - Glyph name: exclam	Contours detected: 1	Expected: 2
 - Glyph name: quotedbl	Contours detected: 0	Expected: 2
 - Glyph name: numbersign	Contours detected: 0	Expected: 2
 - Glyph name: asterisk	Contours detected: 0	Expected: 1 or 4
 - Glyph name: slash	Contours detected: 0	Expected: 1
 - Glyph name: one	Contours detected: 0	Expected: 1
 - Glyph name: three	Contours detected: 2	Expected: 1
 - Glyph name: five	Contours detected: 2	Expected: 1
 - Glyph name: seven	Contours detected: 2	Expected: 1
 - Glyph name: eight	Contours detected: 2	Expected: 3 
 - And 64 more.

Use -F or --full-lists to disable shortening of long lists.
 [code: contour-count]

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking Vertical Metric Linegaps.</summary>

* [com.google.fonts/check/linegaps](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/hhea.html#com.google.fonts/check/linegaps)

* ⚠ **WARN** OS/2 sTypoLineGap is not equal to 0. [code: OS/2]

</details>
<details>
<summary>⚠ <b>WARN:</b> Does GPOS table have kerning information? This check skips monospaced fonts as defined by post.isFixedPitch value</summary>

* [com.google.fonts/check/gpos_kerning_info](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/gpos.html#com.google.fonts/check/gpos_kerning_info)

* ⚠ **WARN** GPOS table lacks kerning information. [code: lacks-kern-info]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are there any misaligned on-curve points?</summary>

* [com.google.fonts/check/outline_alignment_miss](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_alignment_miss)
<pre>--- Rationale ---
This check heuristically looks for on-curve points which are close to, but do
not sit on, significant boundary coordinates. For example, a point which has a
Y-coordinate of 1 or -1 might be a misplaced baseline point. As well as the
baseline, here we also check for points near the x-height (but only for lower
case Latin letters), cap-height, ascender and descender Y coordinates.
Not all such misaligned curve points are a mistake, and sometimes the design may
call for points in locations near the boundaries. As this check is liable to
generate significant numbers of false positives, it will pass if there are more
than 100 reported misalignments.</pre>

* ⚠ **WARN** The following glyphs have on-curve points which have potentially incorrect y coordinates:
	* four (U+0034): X=70.0,Y=1.0 (should be at baseline 0?)
	* four (U+0034): X=99.0,Y=-1.5 (should be at baseline 0?)
	* four (U+0034): X=70.0,Y=1.0 (should be at baseline 0?)
	* G (U+0047): X=525.0,Y=-1.0 (should be at baseline 0?)
	* Q (U+0051): X=492.0,Y=762.0 (should be at cap-height 764?)
	* T (U+0054): X=277.0,Y=2.0 (should be at baseline 0?)
	* T (U+0054): X=188.0,Y=2.0 (should be at baseline 0?)
	* T (U+0054): X=476.0,Y=2.0 (should be at baseline 0?)
	* T (U+0054): X=387.0,Y=2.0 (should be at baseline 0?)
	* underscore (U+005F): X=50.0,Y=-2.0 (should be at baseline 0?) and 7 more.

Use -F or --full-lists to disable shortening of long lists. [code: found-misalignments]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are any segments inordinately short?</summary>

* [com.google.fonts/check/outline_short_segments](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_short_segments)
<pre>--- Rationale ---
This check looks for outline segments which seem particularly short (less than
0.6% of the overall path length).
This check is not run for variable fonts, as they may legitimately have short
segments. As this check is liable to generate significant numbers of false
positives, it will pass if there are more than 100 reported short segments.</pre>

* ⚠ **WARN** The following glyphs have segments which seem very short:
	* four (U+0034) contains a short segment B<<337.5,373.0>-<334.0,367.0>-<327.0,367.0>>
	* nine (U+0039) contains a short segment L<<482.0,773.0>--<493.0,773.0>>
	* nine (U+0039) contains a short segment L<<432.0,-15.0>--<423.0,-15.0>>
	* question (U+003F) contains a short segment L<<102.0,343.0>--<105.0,343.0>>
	* question (U+003F) contains a short segment L<<396.0,343.0>--<398.0,343.0>>
	* question (U+003F) contains a short segment L<<201.0,343.0>--<202.0,343.0>>
	* H (U+0048) contains a short segment L<<348.0,33.0>--<348.0,0.0>>
	* H (U+0048) contains a short segment L<<60.0,0.0>--<60.0,33.0>>
	* H (U+0048) contains a short segment L<<60.0,731.0>--<60.0,764.0>>
	* H (U+0048) contains a short segment L<<348.0,764.0>--<348.0,731.0>> and 42 more.

Use -F or --full-lists to disable shortening of long lists. [code: found-short-segments]

</details>
<details>
<summary>⚠ <b>WARN:</b> Do any segments have colinear vectors?</summary>

* [com.google.fonts/check/outline_colinear_vectors](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_colinear_vectors)
<pre>--- Rationale ---
This check looks for consecutive line segments which have the same angle. This
normally happens if an outline point has been added by accident.
This check is not run for variable fonts, as they may legitimately have colinear
vectors.</pre>

* ⚠ **WARN** The following glyphs have colinear vectors:
	* W (U+0057): L<<59.0,726.0>--<59.0,726.0>> -> L<<59.0,726.0>--<59.0,726.0>> and Z (U+005A): L<<158.0,53.0>--<346.0,53.0>> -> L<<346.0,53.0>--<417.0,54.0>> [code: found-colinear-vectors]

</details>
<details>
<summary>⚠ <b>WARN:</b> Do outlines contain any jaggy segments?</summary>

* [com.google.fonts/check/outline_jaggy_segments](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_jaggy_segments)
<pre>--- Rationale ---
This check heuristically detects outline segments which form a particularly
small angle, indicative of an outline error. This may cause false positives in
cases such as extreme ink traps, so should be regarded as advisory and backed up
by manual inspection.</pre>

* ⚠ **WARN** The following glyphs have jaggy segments:
	* B (U+0042): B<<469.5,434.0>-<430.0,419.0>-<390.0,415.0>>/L<<390.0,415.0>--<404.0,415.0>> = 5.710593137499633 [code: found-jaggy-segments]

</details>
<details>
<summary>⚠ <b>WARN:</b> Do outlines contain any semi-vertical or semi-horizontal lines?</summary>

* [com.google.fonts/check/outline_semi_vertical](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_semi_vertical)
<pre>--- Rationale ---
This check detects line segments which are nearly, but not quite, exactly
horizontal or vertical. Sometimes such lines are created by design, but often
they are indicative of a design error.
This check is disabled for italic styles, which often contain nearly-upright
lines.</pre>

* ⚠ **WARN** The following glyphs have semi-vertical/semi-horizontal lines:
 * N (U+004E): L<<730.0,215.0>--<727.0,726.0>>
 * c (U+0063): L<<428.0,496.0>--<429.0,368.0>>
 * e (U+0065): L<<131.0,335.0>--<372.0,336.0>>
 * eacute (U+00E9): L<<131.0,335.0>--<372.0,336.0>>
 * edieresis (U+00EB): L<<131.0,335.0>--<372.0,336.0>>
 * egrave (U+00E8): L<<131.0,335.0>--<372.0,336.0>>
 * two (U+0032): L<<151.0,83.0>--<357.0,84.0>> and zero (U+0030): L<<377.0,164.0>--<136.0,165.0>> [code: found-semi-vertical]

</details>
<br>
</details>

### Summary

| 💔 ERROR | 🔥 FAIL | ⚠ WARN | 💤 SKIP | ℹ INFO | 🍞 PASS | 🔎 DEBUG |
|:-----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 3 | 10 | 12 | 109 | 7 | 81 | 0 |
| 1% | 5% | 5% | 49% | 3% | 36% | 0% |

**Note:** The following loglevels were omitted in this report:
* **SKIP**
* **INFO**
* **PASS**
* **DEBUG**
