| __Student__            | [Subhramit Basu](https://github.com/subhramit)                                                                 |
|------------------------|----------------------------------------------------------------------------------------------------------------|
| __Organization__       | [JabRef]                                                                                                       |
| __Primary repository__ | [JabRef/jabref]                                                                                                |
| __Project name__       | Improved CSL Support (and more LibreOffice-JabRef integration enhancements)                                    |
| __Project mentors__    | [Christoph](https://github.com/Siedlerchr), [@ThiloteE](https://github.com/ThiloteE), [@calixtus](https://github.com/calixtus), [@koppor](https://github.com/koppor),                                                                                                    |
| __Project page__       | [Google Summer of Code 2024 Project Page](https://summerofcode.withgoogle.com/programs/2024/projects/MfPL66UW) |
| __Status__             | Complete                                                                                                       |

## Project summary

**[Citation Style Language](https://citationstyles.org/) (CSL)** is a popular open-source XML-based language that describes schema for formatting of citations and bibliographies.
It supports thousands of citation styles popular in academia, such as _American Psychological Association_ (APA), _American Medical Association_ (AMA), _Institute of Electrical and Electronics Engineers_ (IEEE), _Modern Language Association_ (MLA), _Chicago Manual of Style_ (CMS), _Springer - Lecture Notes in Computer Science_, _American Institute of Physics_, _Harvard_, _Vancouver_, _Nature_ and so on.  
  
JabRef's integration with LibreOffice lacked support for citing references using the Citation Style Language, which was a highly requested feature among its user base [(#119)](https://github.com/JabRef/jabref/issues/119), [(#2146)](https://github.com/JabRef/jabref/issues/2146). 

Refined project issue - [(#8893)](https://github.com/JabRef/jabref/issues/8893).

This project implements this feature and also enhances the existing Jabref-OO/LO integration in four broad sub-parts: 

1. Implementing a user-friendly CSL style selection functionality for citations, in-text citations and reference lists
2. Ensuring seamless adaptation of the selected CSL style to a connected LibreOffice document instance
3. Improving the existing architecture of JabRef's LibreOffice/OpenOffice integration code
4. Writing unit tests for the aforementioned features

### Pull Requests to *main* branch:

###### Scope - GSoC

####  [#11477](https://github.com/JabRef/jabref/pull/11477) - CSL4LibreOffice - A [GSoC '24]

Highlights:

- Added functionality to select a CSL style from the "Select style" dialog
- Added functionality to preview the selected CSL style (in bibliography form on a test entry) in the dialog
- Added functionality to insert citations and bibliographic entries into a running LibreOffice document with the selected CSL style

#### [#11521](https://github.com/JabRef/jabref/pull/11521) - CSL4LibreOffice - B [GSoC '24]

Highlights:

- Refactored existing code, revamped and unified the backend architecture for style type selection 
- Implemented preference storage for selected style (JStyle/CSL style) to make it persist across JabRef sessions
- Implemented "auto-scroll to and highlight" feature for currently selected CSL style when opening/reopening the "Select style" dialog
- Implemented a label in the dialog to keep the user informed about the currently set JStyle/CSL style
- Miscellaneous bug fixes and added fail-safety for edge cases (such as missing styles, empty selections, etc.)

#### [#11577](https://github.com/JabRef/jabref/pull/11577) - CSL4LibreOffice - C [GSoC '24]

Highlights:

- Implemented "reference marks" to fix resetting index issue for numeric CSL styles
- Added feature to auto-generate and sync a bibliography section (list of references) in the LibreOffice document based on existing citations
- Added support for in-text citations and empty citations for CSL styles
- Added support for underlined CSL styles
- Added support for alphanumeric CSL styles
- Implemented "smart spaces" feature for CSL citation insertion
- Miscellaneous refinement and additions (e.g. new icon for "add bibliography", fixed extra newlines in case of numeric styles, disabled irrelevant buttons when CSL style is selected, upgraded to StAX parsing for information from .csl files etc.)

#### [#11636](https://github.com/JabRef/jabref/pull/11636) - CSL4LibreOffice - D [GSoC '24]

Highlights:

- Refactored existing code from PR A, B and C
- Added documentation for the added classes and methods
- Added comprehensive unit tests for the added utility methods

#### [#11535](https://github.com/JabRef/jabref/pull/11535) - Make CSL Citation Adapter non-static
#### [#11604](https://github.com/JabRef/jabref/pull/11604) - Upgrade to StAX parsing for CSL style titles
#### [#11536](https://github.com/JabRef/jabref/pull/11536) - Patch: NullPointerException when accessing (absent) default CSL style file
#### [#11622](https://github.com/JabRef/jabref/pull/11622) - Update JabRef material icons pack

###### Outside core scope

#### [#11635](https://github.com/JabRef/jabref/pull/11635) - Persist selection of databases in SLR
#### [#11665](https://github.com/JabRef/jabref/pull/11665) - Upgrade EndNote XML exporter to StAX
#### [#11614](https://github.com/JabRef/jabref/pull/11614) - Fix authorsAlpha
#### [#11667](https://github.com/JabRef/jabref/pull/11667) - Selected SLR catalogs: maintain preferences abstraction level
#### [#11456](https://github.com/JabRef/jabref/pull/11456) - Add FAQ to devdocs (Code Howtos)
#### [#11486](https://github.com/JabRef/jabref/pull/11486) - FAQ updates
#### [#11603](https://github.com/JabRef/jabref/pull/11603) - Integrate DOI special character parsing test in existing parameterized test
#### [#11541](https://github.com/JabRef/jabref/pull/11541) - Fix OpenRewrite recipe
#### [#11568](https://github.com/JabRef/jabref/pull/11568) - Disable GUI debug log
#### [#11587](https://github.com/JabRef/jabref/pull/11587) - Improve developer documentation

###### Before GSoC

#### [#11055](https://github.com/JabRef/jabref/pull/11055) - Add new parser for MathSciNet search
#### [#11157](https://github.com/JabRef/jabref/pull/11157) - Add Endnote XML Exporter + Rehaul Importer
#### [#11073](https://github.com/JabRef/jabref/pull/11073) - Fix (some) fetcher tests
#### [#11080](https://github.com/JabRef/jabref/pull/11080) - Change file directory error dialog
#### [#11084](https://github.com/JabRef/jabref/pull/11084) - Fix DOI URL parsing
#### [#11088](https://github.com/JabRef/jabref/pull/11088) - Add checks and warnings in SLR for non-empty directories
#### [#11104](https://github.com/JabRef/jabref/pull/11104) - Add right click->copy functionality to event logs
#### [#11111](https://github.com/JabRef/jabref/pull/11111) - Remove warnings when importing search entries in unsaved libraries
#### [#11152](https://github.com/JabRef/jabref/pull/11152) - Fix LICENSE link


## Statistics

|        Changes        | **During GSoC** |      **All**        |
|-----------------------|-----------------|---------------------|
| **(+) Lines added**   |      3646       |        6218         |
| **(-) Lines removed** |      1217       |        1647         |  
  
Here is a complete [list of my commits](https://github.com/JabRef/jabref/commits?author=subhramit) to JabRef (main).

## Blog posts
(Upcoming)

[JabRef]: https://www.jabref.org
[JabRef/jabref]: https://github.com/JabRef/jabref
