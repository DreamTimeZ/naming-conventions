# File Naming Best Practices

## Best Practices for Cross-Platform Folder Names

Research on cross-platform naming conventions (Farmer, 2022; Spreckelsen et al., 2020) establishes these evidence-based guidelines:

1. **Use all lowercase letters** - Eliminates case sensitivity issues across systems
2. **Use hyphens (-) as separators** - More readable than underscores and compatible with URLs
3. **Avoid spaces and special characters** - Spaces create issues in command-line operations
4. **Keep folder names under 31 characters** - For maximum compatibility
5. **Use ISO 8601 date format (YYYY-MM-DD)** - Ensures chronological sorting
6. **Include README files** in each main folder explaining the organization system

Controlled studies on file organization and retrieval have shown that consistent folder naming:

- Improves retrieval speed by 27-35% (Journal of Information Science, 2019)
- Reduces organizational errors by up to 42% (International Journal of Human-Computer Interaction, 2020)
- Significantly enhances collaboration efficiency in research settings (Spreckelsen et al., 2020)

## Time Spans and Date Ranges in Folder Names

ISO 8601-2:2019 provides standardized extensions for representing time spans and date ranges in a cross-platform compatible way. For time spans and date ranges in folder names, follow these scientifically validated formats:

### Standard Formats for Year Spans and Time Periods

1. **Basic Closed Range Format:**
   - Use a hyphen between start and end dates: `[YYYY]-[YYYY]` (e.g., `2020-2022`)
   - For more detailed ranges: `[YYYY-MM]-[YYYY-MM]` (e.g., `2020-01-2022-06`)
   - This syntax follows the ISO 8601-2 preferred method for file/folder naming

2. **ISO 8601-2 Interval Notation:**
   - For machine processing and data interchange, the solidus format `[YYYY]/[YYYY]` is the ISO standard (e.g., `2020/2022`)
   - Note: For filenames and folders, hyphens are preferred over solidus due to operating system path limitations

3. **Open Date Ranges:**
   - For start date with no defined end: `[YYYY]-ongoing` (e.g., `2020-ongoing`)
   - For periods before a specific date: `until-[YYYY]` (e.g., `until-2020`)

4. **Academic Year Notation:**
   - Standard academic notation: `[YYYY]-[YYYY+1]` (e.g., `2020-2021`)

5. **Multi-Year Periods:**
   - For decade spans: `[YYYY]s` (e.g., `2010s`)
   - For multi-year research projects: `[YYYY]-[YYYY]` (e.g., `2020-2025`)

### Scientific References

- ISO 8601-2:2019 Date and time — Representations for information interchange — Part 2: Extensions
- Library of Congress Extended Date/Time Format (EDTF) Specification
- Dublin Core Collection Description Working Group (DCCD ODRF)
- Stanford University Libraries Data Best Practices Guide (2023)
- Cambridge University Digital Preservation Manual (Farmer, 2022)
- NASA Space Physics Data Facility Recommended File and Data Collection Naming Practices

## Date Format Scientific Research (YYYYMMDD vs YYYY-MM-DD)

Research and standards support the following findings regarding date formats:

- **ISO 8601 standard** officially specifies YYYY-MM-DD with hyphens as the primary format for human-readable dates, while compact formats (YYYYMMDD) are recommended for specific technical applications.

- **Cognitive psychology research** indicates that separators in dates (YYYY-MM-DD) improve reading speed and accuracy by creating meaningful "chunks" that reduce cognitive load (Saito et al., "Cognitive Processing of Date Information," Journal of Experimental Psychology, 2018).

- **Human factors studies** demonstrate that dates with separators are:
  - Processed approximately 20-30% faster
  - Less prone to errors during transcription
  - More accessible for international audiences
  - Better for people with cognitive or visual impairments
  (Nielsen Norman Group, "Date Format and Human Usability," 2019)

- **Error detection research** shows that people can more easily identify mistakes in separated date formats (2023-02-31 is more visibly incorrect than 20230231) (International Journal of Human-Computer Interaction, "Error Detection in Date Formats," 2020).

While both formats (YYYYMMDD and YYYY-MM-DD) ensure chronological sorting, YYYY-MM-DD provides better human readability while maintaining machine-readability benefits.

## Harvard File Naming Conventions

[File Naming Convention Harvard.edu](https://datamanagement.hms.harvard.edu/plan-design/file-naming-conventions)

- Identify what group of files your naming convention will cover
- You can use different conventions for different file sets
- Check for established file naming conventions in your discipline or group
- Think about how you will search for your files
- **Write down your naming conventions!!!**

### Use versioning

- Use versioning to indicate the most current version of a file
- Track versions of a file by adding version information to end of the file name, e.g. `filename_v2.xxx`
- Use a version number (e.g. "v01" or "v02")

### Use abbreviations and document them

- mouse = "MUS", fruit fly = "DRS"

### Deliberately separate metadata elements

- Use dashes (`-`), underscores (`_`), or capitalize the first letter of each word
  - Dashes: `file-name.xxx`
  - Underscores: `file_name.xxx`
  - No separation: `filename.xxx`
  - Camel case: `fileName.xxx` (as in `[camelCase]`)
  - Pascal case: `FileName.xxx` (as in `[PascalCase]`)
- Avoid special characters, such as: ~ ! @ # $ % ^ & * ( ) ` ; : < > ? . , [ ] { } ' " |

## Three principles for (file) names

[Harvard.edu -> Datacarpentry.org File Naming](https://datacarpentry.org/rr-organization1/01-file-naming/index.html)

- Machine readable
- Human readable
- Plays well with default ordering

### Machine readable

- Regular expression and globbing friendly
  - Avoid spaces, punctuation, accented characters, case sensitivity
  - Easy to compute on
- Deliberate use of delimiters
- Easy to search for files later
- Easy to narrow file lists based on names
- Easy to extract info from file names, e.g. by splitting
- New to regular expressions and globbing? Be kind to yourself and avoid
  - Spaces in file names
  - Punctuation
  - Accented characters
  - Different files named foo and Foo

### Human readable

- Name contains info on content
- Connects to concept of a slug from semantic URLs

### Punctuation

Deliberate use of `-` and `_` allows recovery of meta-data from the filenames:

- `_` underscore used to delimit units of meta-data I want later
- `-` hyphen used to delimit words so my eyes don't bleed

### Plays well with default ordering

- Put something numeric first
- Left pad other numbers with zeros (001, 002... instead of 1, 2...)

## Best Practices

[File Naming Best Practices tru.ca](https://www.tru.ca/__shared/assets/file-naming-best-practices-46019.pdf)

The most important things to remember about file naming are to be consistent
and descriptive in naming and organizing your files so that it's obvious where
to find a file and what it contains.

### Information to consider including in file names

1. Topic or Project name
2. Author's name/initials
3. Date or date range
4. Type of record (e.g. newsletter)
5. Version number of document (e.g. v1)

These are suggestions; include whatever information will allow you to
distinguish your files from each other and clearly indicate to you what is in them.

### Other tips for file naming

1. Don't make file names too long; longer names do not work well with all
types of software.
2. Special characters should be avoided: ~ ! @ # $ % ^ & * ( ) ` ; : < > ? , [ ] { } ' "
3. For sequential numbering, use leading zeros to ensure files sort
properly. For example, use "0001, 0002…1001, etc" instead of "1,
2…1001, etc."
4. Do not use spaces, because they are not recognized by some
software. Instead use underscores (file_name), dashes (file-name),
no separation (filename) or different capitalization (FileName, fileName).

Consider including a README.txt file in your directory that explains your
naming convention along with any abbreviations or codes you have used.

## Personal Notes

### What I discovered or experienced

- Hyphens are better to read and separate words better than underscores -> underscores are less noticeable
- **Date on beginning -> chronological file sorting**

## The Dos and Don'ts of file naming

![Filenaming convention image](uscsb-2021-filenaming.png)
