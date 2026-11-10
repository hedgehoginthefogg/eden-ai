# Help Claude make more accessible PDFs

By default, Claude will often create PDFs that are not accessible, for example they don't work well with screen reading software. This prompt can help Claude turn Artifacts such as html web pages into a PDF with tagged headings, alt text for images and good colour context. The resulting PDF should pass automated accessibility tests, such as those available via [axesCheck](https://check.axes4.com/en). However, automated tests can't capture all issues – you should still review the PDF yourself, and ideally get input from someone who uses screen reading software. For an exploration of what can and can't be tested automatically, see for example [How should accessibility testing change in the age of AI?](https://abilitynet.org.uk/news-blogs/how-should-accessibility-testing-change-age-ai).

This prompt is the result of ongoing experimentation and testing – please let Steven Williams (s.williams10@lse.ac.uk) know if you have any suggestions for improvements.

## Overview

Don't make the accessible PDF by printing a web page from a browser such as Chromium. Browser PDFs leave backgrounds, borders and boxes untagged, don't add the PDF/UA metadata, and usually fail accessibility checkers such as axesCheck and PAC. Use this method instead.

### 1. Write a clean, semantic version first

- Write the content as a simple HTML file: no buttons, text boxes, copy controls, scripts or decorative wrappers.
- Use one Heading 1 for the title, then headings in order without skipping levels. Keep labels such as timings or "Optional" after the heading they belong to, not before it.
- Give every image alt text. For an animation, use a still frame and say in the alt text that it's a still from an animation.
- Leave out decorative images, such as photos of people, and give every other image a set width as a percentage of the text width (for example width="100%" for wide screenshots and diagrams, and 40–75% for small screenshots and buttons), so pandoc doesn't size images at their full pixel dimensions.
- Turn any diagram that shows which item goes with which into a table with header cells.
- Use real lists, and give every table a header row.
- If the document is longer than a few pages, add a "Contents" list after the introduction, with each entry linking to its heading and giving its page number. Build the PDF once, read each heading's page number from the PDF bookmarks, fill the numbers in, then build again and confirm they haven't changed.

### 2. Convert to Word with pandoc

- Convert the HTML to a Word file with pandoc, setting the language to en-GB, and run pandoc with a UTF-8 locale (for example LANG=C.UTF-8) so characters such as en dashes aren't garbled.
- Don't let a title paragraph appear above the Heading 1: remove the HTML `<title>` before converting, and set the document title in the Word file's properties (docProps/core.xml) instead.
- Then edit the Word file before exporting:
  - Rename the paragraph style called "Figure" (for example to "Image block"). LibreOffice turns style names into PDF tags, and a style called Figure clashes with the real image tags.
  - Replace the default light-blue colour (#4F81BD) on headings and links with dark colours, removing the theme colour attributes so the theme can't override them. For example, use #1C1F3A for headings and #1F3A93 for links. The default blue fails WCAG contrast.
  - Pandoc wraps each section in a bookmark that spans the whole section, placed between paragraphs, so LibreOffice can send contents links to the wrong place or drop them. Move each heading's bookmark inside its heading paragraph, straight after the paragraph properties, as a point bookmark (start and end together), and delete the original end marker.
  - Set the page size to A4 with 2.54 cm margins in the Word file's section properties (w:sectPr, with w:pgSz of 11906 × 16838 and w:pgMar of 1440 on each side). Pandoc leaves these empty, so LibreOffice would otherwise use US Letter.
  - Pandoc sizes percentage image widths against its own assumed text width, not the page's, so scale every image (wp:extent and a:ext) to the real text width: 9026 twips on A4 with these margins.
  - If the contents list should have a page to itself, add a page break before the first main heading.

### 3. Export with LibreOffice

- Export the Word file to PDF with LibreOffice in headless mode, with PDF/UA compliance, tagged PDF and bookmarks turned on (filter options PDFUACompliance, UseTaggedPDF and ExportBookmarks set to true).
- If LibreOffice or pandoc isn't available, tell me before using another method.

### 4. Check the PDF in code before giving it to me

- Every painting operator on every page is either inside tagged content or marked as an Artifact.
- The document language is en-GB, the title is set and DisplayDocTitle is true, MarkInfo Marked is true, and the XMP metadata includes pdfuaid:part 1 and dc:title.
- Headings run in order without skipping levels, and there is only one H1.
- Every Figure has alt text, and no standard tag names (such as Figure, P or Table) appear as keys in the role map.
- Tables have TH cells.
- Every link annotation has a description in its Contents entry, and every internal link goes to the top of the right page. List each contents link with its target page.
- All fonts are embedded.
- Every image has the width it was given. List each image with its width on the page.
- Every page is A4 (595 × 842 points).
- Every text colour in the finished PDF meets WCAG 2.2 AA contrast against its background. List each colour with its contrast ratio.
- Bookmarks exist for every main heading.

Tell me anything you couldn't check, so I can test the PDF with [axesCheck](https://check.axes4.com/en) or PAC. If it fails, I'll give you the report so you can fix it.