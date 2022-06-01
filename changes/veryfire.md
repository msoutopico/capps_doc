# Veryfire -- Development history

## Changes in version 0.8.4 (2014-12-17)

+ New: accuracy ruleset for Spanish time names (months, weekdays, etc.)
+ New: language ruleset for Arabic grammar: some basic rules created (plural masculine verb followed by regular plural masculine subject is flagged as incorrect).
+ New: language ruleset for Arabic spelling: some basic rules created (writing hamza at the end of feminine nouns).
+ New: accuracy ruleset for Spanish tenses (if past tense is used in the source, then past is expected in the target, and if future tense is used in the source, then future is expected in the target). To be tested extensively.
+ New: accuracy ruleset for Spanish numbers (if a number is used in the source, either in written form or as digit, its counterpart is expected in the target). Easy to implement for all languages but glossaries needed.
+ New: number rules from target to source and from source to target: RuleSet_Generic_Placeables_xxx-XXX_20141227_includingFigures.csv: 2 and 3. Note: Further development necessary to catch complex figures (decimals, thousands, radio stations, alphanumerics, zip codes, dates, phone numbers, IP addresses, etc.)
+ New: language-independent exceptions set created for PIRLS and TIMMS

## Changes in version 0.8.3 (2014-11-30)

+ Added check: LanguageTool
+ New: Tooltips for UI options
+ Improved: Persistence of user preferences in the upload form.
+ Improved: Term consistency check ignores occurrences which are substrings of longer terms
+ New: Logfile for later retrieval of characteristics of execution (for debugging purposes)
+ New: Added selected check for Numbers
+ New: Country-independent, language-specific rule selection (EXPLAIN: one same rule that applies to a language regardless of where it is spoken, so as not to have as many rules as countries in which it is applied)
+ New: Country-specific, language-independent rule selection (EXPLAIN... national or cultural realities that change from country to country: eg. the name of the national assembly in different Spanish-speaking countries (parlamento, congreso, asamblea, etc.)
+ Fixed: Link to go to report not working when processing zipped batches (all links refered to the first report).
+ Improved documentation.
+ Improved: UnalteredWords function gets exceptions from target terms in glossary rules
+ New: Sets (placeholders that stand for a list of items in rules)

## Changes in version 0.8.2 (2014-09-04)

+ Fixed: Extraction of segments from text nodes in XML files from PISA2015 portal (only first node of a series of nodes with same name and same level was imported)
+ Improved: Splitting of text strings into independent words for Unaltered Words check.
+ Improved: Better handling exceptions in Unaltered Words check
+ Improved: Better handling errors (file rejection) and empty report.
+ New: Option to analyse FOOD-12 TMX files.
+ Improved: Leading and trailing spaces in terms are now trimmed.
+ New: French ruleset containing French-specific language checks: RuleSet_Generic_Punctuation_fra-FRA_20140919.csv (to be completed gradually)
+ Improved: Made Unaltered Word exceptions case-insensitive
+ New: Context filters added glossary rule to prevent matching a term within a longer term

## Changes in version 0.8.1 (2014.08.15)

+ New: Unaltered segment check
+ New: Unaltered words check
+ New: Added source word exceptions to be checked in Unaltered words check
+ New: Rule to flag double spacing
+ New: Function ForeReference (searches in the source a captured entity in the target, i.e. it flags entities found in the target that were not used in the source)
+ New: Blank check (Checks whether a translation is totally blank.)
+ New: Rule: PISA unit titles (untranslatable)
+ New: Input file: pairs of monolingual XML files from PISA portal

## Changes in version 0.8

+ New: Added target segment exceptions
+ New: Added GUI option to choose output format (HTML or Excel)
+ New: Added option to sort results by translation unit or rule used (to be included in GUI)
+ New: Added GUI option to select tab and columns to be processed in Excel input files
+ New: Added GUI option to select checks to be applied (Placeables, Glossary, etc.)
+ New: Created accuracy (basic punctuation, spacing, basic numbers) rules
+ Improved: Rules flagging lack of integrity in the translation of placeholders/codes
+ New: Created basic punctuation rules for Greek

## Changes in version 0.7

+ New: The report is generated in Excel 2007 format.
+ New: User can submit zip file and all contents are batch-processed. HTML report.
+ Improved: Segment-level consistency check - correct error numbering, correct segment/cell id displayed, both reports (generic checks and rule-based) merged, correct colouring of rows in report.
+ New: Created function to parse TMX input files

## Changes in version 0.6

+ Improved: Backreference function (use in the target expression something coming from the source expression)
+ New: expansion rate (basic functionality ready, pending finding language-specific data)
+ New: Empty target check
+ Improved: Output is now usable by Vegasuite
+ New: Spell checking functionality (hunspell). Not working for special characters.
+ New: Spacing checks
+ New: Punctuation check

## Changes in version 0.5

+ New: User can submit zip file and all contents are batch-processed.
+ New: Segment-level consistency check
+ New: memoQ-style wildcards and synonym detection in the glossary rule
+ Improved: Added exception for PISA filenames (lll-CCC)

## Changes in version 0.4

+ New: Translatability assessment function
+ New: Writing TA results to spreadsheet
+ Improved: Report includes one new column for ruleset's name and rule number
+ New: Comment and suggestion come from the rule, if set there (otherwise, default message)
+ New: Added color highlight for matches

## Changes in version 0.3

+ New: Term consistency check (glossary rule)
+ New: Blacklisted/disallowed term check
+ New: Project and locale parameters are read from the input files' name
+ New: Selection of rule sets based on language and project parameters

## Changes in version 0.2

+ New: Placholder integrity checks for ESENER-2 project

## Wishlist

+ Readability index

## Work in progress

+ Expansion rate limit check
+ Spelling check

## Issues

+ Formulas are not retained in the TA output written to the original Excel file
+ Rulesets (in UTF-8) cannot be edited in Excel (workaround: Google docs and Calc) => FIXED 
