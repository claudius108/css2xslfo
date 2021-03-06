# Changes

1. Changes Since Version 1.6.1

3051512: Recompile for FOP 1.0

Bug fixes

2. Changes Since Version 1.6

Bug fixes

2571787: Bug in ProjectorFilter
2588555: The value "transparent" is not recognized as a color
2758546: Relative URLs are always resolved to absolute URLs

3. Changes Since Version 1.5.2

Bug fixes

1722531: hard coded urls in css file are all set to lowercase
1911693: xml:lang or lang on document element is ignored
1984171: The XHTML catalog is no longer included
1997883: table element with a region property causes program to die

New features

- Add FOP command-line parsing for fopnew (feature request 1989920). With the
  new "-fop" option any FOP command-line option can be used. Note that the
  complete command-line syntax is not compatible with the previous version. The
  "-fc" has been removed, because there now is the FOP equivalent.
- Add the "-config" command-line option to the Xinc variant.
- Add the "-config" command-line option to the XSLFormatter variant.

4. Changes Since Version 1.5.1

Bug fixes

1807366: Floating point values are locale dependent
1811419: The text-align-last property is not treated as inherited
1824076: Splitting shorthand properties four ways uses a wrong order
1843554: Setting float to "none" still generates an fo:float

5. Changes Since Version 1.5

Bug fixes

1802080: A named page sequence with only tables is considered empty

6. Changes Since Version 1.4.2

Bug fixes

1716939: Regression because of invalid property bug (1691044)
1722531: hard coded urls in css file are all set to lowercase
1722541: underscores in class name
1723310: Relative URLs in a style sheet are not resolved
1731447: Inline properties are not applied to "graphic" and "leader"
1733555: The width and height properties are not applied to "graphic"
1737664: Floating point values shouldn't use exponential notation
1767912: Using as filter without calling parse or setParent fails
1768297: The text-align property is no longer applied to table cells
1770690: The page-break properties are no longer applied to table-row
1778499: The fopnew option -fc is broken

New features

- Support last pages, analogous to first pages (feature request 1720073).
- Implement the "list-style-image" property (feature request 1721782).
- Implement the background, border and padding page properties that are defined
  in CSS3 (feature request 1724392). This deviates from that specification in
  that the properties are applied to the region-body, because in XSL-FO they are
  not defined at the page master level.

7. Changes Since Version 1.4.1

Bug fixes

1701428: The border-width shorthand property is not split
1715203: Regression because of font-family bug (1679537)

8. Changes Since Version 1.4

Bug fixes

1679537: Font family names not quoted when they contain spaces
1681734: Only block-container should have absolute positioning
1684177: ID attribute on body is duplicated
1691044: Unexpected CSS attributes come out as bogus FO attributes
1691392: Named strings fail when contents is fragmented

9. Changes Since Version 1.3.3

Bug fixes

1594025: Css2FopNew user configuration file
1626094: Testing a style sheet URL is too slow

New features

- New Ant tasks (feature request 1554682).
- New options "-config" and "-q" for css2xep.jar.

10. Changes Since Version 1.3.2

Bug fixes

1496388: Rules with document element don't work when in open document
1496389: xml:base treatment is not scoped
1553292: BASE element and xml:base not taken into account for links

New features

Use version 0.92beta instead of 0.91beta for the package for the new FOP branch.

11. Changes Since Version 1.3.1

Bug fixes

1359835: When display is "none" on regions, they are no longer shown
1462265: Regions which are not specific are not inherited
1482296: Overriding anonymous page context properties doesn't work
1482644: Drop width conversion for % values when parent has no width

12. Changes Since Version 1.3

Bug fixes

1455266: Regression with XSLTC because of prefix mapping events

13. Changes Since Version 1.2

Bug fixes

1356430: list-style and its singles are not treated correctly
1359835: When display is "none" on regions, they are no longer shown
1361765: No default for page counter reset
1425336: Invalid flow-name references

New features

- CSS3 namespaces.
- Implement the "list-style-position" property.
- Implement the ":first-letter" pseudo element.
- Add the "wrapper" display type, which prevents an element from contributing
  formatting objects, but for which property inheritance works.
- Add DeltaXML (http://www.deltaxml.com) to the User Agent style sheet. It
  takes care of the difference mark-up in the DeltaXML namespace. Note that the
  style sheet uses change bars, which work only for XEP4
  (http://www.renderx.com) at the moment.
- Add XLink to the User Agent style sheet. This merely consists of supporting
  the global XLink "href" attribute.
- Relax the constraint that there should be no whitespace between a footnote
  reference and a footnote body. Whitespace between them is now gobbled.
- Add the possibility for a footnote body to have a ":before" pseudo element
  with the display type "footnote-reference" instead of an explicit footnote
  reference element. The generated contents will go in the flow as well as in
  the footnote body.
- Add support for xml:id.
- Add the "foreign" display type. Elements having it end up in an
  fo:instream-foreign-object element.

14. Changes Since Version 1.1

Bug fixes

1348367: Fix table normalisation when display type is "none".
1348374: Fix link processing.
1348383: A CSS style sheet is not treated as case-insensitive.
1349014: Correct manual section about running with FOP.

New features

- The special Unicode spaces U+2000 through U+200A are post-processed using
  fo:leader elements (reminiscent of Jirka Kosek's DocBook style sheet).

15. Changes Since Version 1.0

Bug fixes

1281230: The presence of the anonymous @page rule is assumed.
1285991: Move fo:marker to the next allowed place in the XSL-FO tree.
1286078: Turn off hyphenation by default for User Agent page set-up.
1291094: A marker pseudo element shouldn't imply the other is one too.
1315758: Don't generate empty page sequences.

New features

- Add the "colspan" and "rowspan" properties for table cells.
- Add the unit "pcw" (proportional column width) for table column widths.
- Add the "table-omit-footer-at-break" and "table-omit-header-at-break"
  properties for tables.

16. Changes Since Version 1.0rc2

Incompatible changes

- The "footnote" property no longer exists. It is replaced by the new display
  types "footnote-reference" and "footnote-body". This provides control over
  contents and style of both the footnote reference and body. The list style
  type "footnote" has also been added. It generates symbols such as the
  asterix, dagger, etc.
- Regions have an incompatible restriction. They must now be the first children
  of the body region element. For XHTML the latter is the body element.
- Move "counter-reset" for the "page" counter from the static regions to the
  @page rule.
- Hyphenation is turned off by default instead of on. This puts it in line
  with XSL-FO.

Enhancements

- Add the "precedence" property for the top and bottom regions.
- Implement the change bar extension. This works only with XEP at the moment.
- Add the link extension, which covers internal and external links.
- Make it work with Saxon 8.3 and later.
- Make it work with JDK 1.5 without having to prepend an XSLT processor in the
  boot class path.
- Remove the CSS rules for the XHTML elements "sup" and "sub" from the User
  Agent style sheet. Set the "line-height-shift-adjustment" property to
  "disregard-shifts" to compensate this.
- Show a stack trace only in the main functions when -Dbe.re.stack is on.
- Generalize the named pages feature. It is no longer bound to a sibling list
  below the XHTML "body" element or the document element for another XML
  vocabulary.
- Enhance performance and reduce memory usage.
- Add a Xinc package.
- Add the XSL-FO "force-page-count" property.
- Implement markers with the limitation that the value "auto" is not supported
  for the the "width" property. Check out section 12.6 of the CSS2
  specification to learn how you can have much more control over lists through
  markers.
- Implement the "column-span" property for multicolumn pages.
- Introduce the display type "graphic".
- Add the pseudo page "blank".

Bug fixes

- Fix the "string-set" property bug. It didn't cascade properly and it didn't
  work when placed in the XHTML "style" attribute.
- Fix the CSSToXSLFOFilter constructor. It didn't check the absence of the
  user agent parameters.
- Fix the absence of the "any" simple-page-master when there were @page rules
  without an anonymous @page rule.
- Fix a page rule cascade bug. The page rules weren't split before sorting them.
- Do the inheritance of text-align and vertical-align in tables only for XHTML
  tables and take into account the specificity of UA rules and universal
  selectors.
- Fix the bug where properties on pseudo elements were also applied to the
  elements themselves.
- Change the processing instruction xml:stylesheet into xml-stylesheet. The
  XML namespaces specification doesn't allow colons in PI targets. The new
  target follows the CSS2.1 convention.
- Fix the combination of pseudo classes and pseudo elements. The specification
  ":first-child:before" didn't work.
- Fix the application of the "content" property. It didn't cascade, but
  combined all matched property values.
- Fix the specificity calculation in the case where several conditions are
  combined.
- Set the "font-selection-strategy" property to "character-by-character", which
  corresponds to CSS.
- Implement centering of blocks and tables when "margin-left" and
  "margin-right" are set to "auto".
- Report missing command-line options in css2fop.jar.
- Produce a descent error message when an URL is invalid when trying to parse
  a CSS style sheet.
- The value "contents" for the "string-set" property also included the
  generated content for the element it was set on.
- Fix the bug where the "userAgentParameters" argument to the constructor can't
  be "null".
- Fix the treatment of the "clear" property.

17. Changes Since Version 1.0rc1

- Install an error handler on the filter chain for the validating mode,
  otherwise there are no error messages when Xalan 2.6.0 or higher are used.
  This is because Xalan's TraXFilter now correctly propagates error handler
  events instead of throwing an exception.
- Also add the default unit "px" to the "width" and "height" of the XHTML "img"
  element if there is no specified unit.
- Honor the "media" attribute of the XHTML "style" and "link" elements.
- Fix a selector bug in the case unnamed element selectors are used elsewhere
  than at the final position.
- Fix a named pages regression when using a more recent Xalan version.
- Implement the multicolumn extension.

18. Changes Since Version 1.0b3

- Implement positioned elements (position, top, bottom, left and right
  properties).
- Implement layered presentation (z-index property).
- Use a block-container instead of a plain block when one of the following
  properties is specified on a block-level element: clip, height, min-height,
  min-width, overflow, width. This bug disabled those properties.
- Add a FOP package variant with a FOP filter that removes some of the
  non-supported XSL-FO properties.
- Implement the additional CSS3 List Module glyphs for the list-style-type
  property.

19. Changes Since Version 1.0b2

- Change the common -p option to accept a comma-separated list of URLs or
  filenames instead of just one.
- The anonymous page block elements following a named page block element are
  now part of the same name page type of the latter.
- Give lower precedence to the UA style sheet.
- Fix a bug in the translation of XHTML attributes into CSS properties.
- Fix a bug in the static region mapping onto pages.
- Fix a bug in the load of the embedded XHTML catalog.
- Document the footnote extension.
- Document the orientation extension.
- Complete the "Compliance With CSS2" section of the manual.

20. Changes Since Version 1.0b1

- Drop XSLTC because it produces wrong results.
- Add the option "-v" to turn on XML validation explicitly. By default no
  validation is done.
- Replace the deprecated XEP interface with the new interface.
