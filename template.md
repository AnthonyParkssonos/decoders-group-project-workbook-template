Decoders Group Project Workbook Template
==========================================

## Summary
This project aims to build, integrate, refactor, or remove X.

## Personnel
- Surgeon - Govind Jeyeram
- Co-Pilot - Sungjun Kim
- Secretary - Anthony Parks
- Inspector General - Rob Tame

## Formatting Requirements

### Nesting

- This project workbook shall make use of nested hash symbols (let the hash
symbol be defined by ("#"). Major sections are headed by one #, while subsections
are headed by two #'s.
- The smallest acceptable headings is three #'s, to indicate a
sub-subsection. Beyond this, please make a new subsections.
- Lists shall be indicated by the dash symbol (let the dash symbol be defined by "-").
- We shall not use numbered lists in Markdown, as re-numbering can be cumbersome. Let a program like Pandoc handle numbered formatting output. We shall however, of course, number requirements, discussed below.

### Project Requirements

- We shall always number requirements with a unique identification code. This unique identification code shall always take the form "requirement category dot requirement number". For example, a feature requirement id code should take the format FR.ddd. For featurement requirement number 23, the code would be FR.023.
- Requirement identification number formats shall accomodate only the desired maximum number of requirements. This can make text base parsing and sorting easier
should we ever in the future desire to process our requirements.
- Requirements shall be listed in tabular form using the pipe symbol "|" to indicate field separators, with the last field must include |.
- The display size must be indicated by a number of dashes preceeded by a colon (":") from the second field onward.
- For long lines in tables, **we will let Markdown handle the wrapping, and your editor can toggle wrapping**. It is too cumbersome to handle manually.

```
| ID       | Description                                                                          |
|----------|:-------------------------------------------------------------------------------------|
| UID.001  | This description by necessity must exceed 100 characters in length for the simple reason that it is far too complex to be within 100 characters and cannot be broken down into separate requirements, because sometimes things can't be broken down further without risking excessive atomicity. |
| UID.002  | This field can be described succinctly and in one line which is far preferable. |
```

Which displays like this:

| ID | Description                                                                                |
|----------|:-------------------------------------------------------------------------------------|
| UID.001  | This description by necessity must exceed 100 characters in length for the simple reason that it is far too complex to be within 100 characters and cannot be broken down into separate requirements, because sometimes things can't be broken down further without risking excessive atomicity. |
| UID.002  | This field can be described succinctly and in one line which is far preferable. |

### Miscellany

- All headings shall include one line of spacing above and below.
- We shall not exceed 100 characters in line length in this document.
- We shall trim excess whitespace in this document. The VSCode plugin trim-trailing is useful for this, and can be set up to remove white space on document save, and saving can also be automated.

# Software Specification

## Supported Platforms

- Legacy support
- This project will or will not support the following legacy platforms:

## Feature Requirements

- All requirements must have a unique ID *FR.ddd* (e.g. FR.073)

| ID     | Description                                                                       |
|--------|:----------------------------------------------------------------------------------|
| FR.001 | We shall only use shall clauses, as shall-nots are infinite and untestable. |
| FR.002 | We shall decode files delivered in a fancy container type. |
| FR.003 | We shall support meta tag X from ISO-BIGNUMBER-OTHERNUMBER |
| FR.004 | We shall update this requirements table when the requirements change. |
| FR.005 | When .dts, .mp4, .aac, etc. is input, the audio pipeline shall decode the encoded content to multi-channel PCM.

## External Dependencies

- Software Dependencies
- Team Dependencies

## Performance Requirements

- All requirements must have a unique ID *FR.ddd* (e.g. FR.073)

| ID     | Desciption                                                                              |
|--------|:----------------------------------------------------------------------------------------|
| PR.001 | We shall deliver this feature with a number of dropouts that does not exceed a maximum target number of tolerable dropouts. |
| PR.002 | We shall have a cpu percentage that does not exceed X percent on any core. |
| PR.003 | We shall deliver this feature with a lip sync delay that does not exceed X milliseconds. |
| PR.004 | We shall deliver this feature with documentation of all the associated static memory requirements. |
| PR.005 | We shall deliver this feature with measurements of worst-case scenario for dynamic memory requirements, but attempt to limit if not eliminate any dynamic memory if possible, as many third party libraries use dynamic allocation. |

## Maintenance Requirements

- We expect that the changing of features related to this project, the
upgrading of this feature, or the fixing of regressions caused directly or
indirectly by the introduction of this feature will annually cost X months
per year.

## Test Plan

This section describes in detail each test case. Each test case will be assigned a single:

- unique ID in the format *T.ddd* (e.g. T.089 )
- category
- unique name
- description
- data/input
- all multimedia inputs (e.g. feature_under_test_configuration.wav) require a
separate file describing the contents and test
- multimedia input should be one file per test case and have a name matching the test case name
- purpose of the file (e.g. feature_under_test_configuration.wav.txt)
- expected result
- actual result (of course, left blank during planning)

| ID    | Category      | Name               | Expectation                                     | Result    |
|-------|:--------------|:-------------------|:------------------------------------------------|:----------|
| T.001 | channel_count | channel_count_2ch  |  stereo content should decode without artifacts | PASS/FAIL |
| T.002 | channel_count | channel_count_mono  | mono content should decode without artifacts   | PASS/FAIL |
| T.003 | channel_count | channel_count_5_1 |  5.1 content should decode without artifacts     | PASS/FAIL |
| T.004 | signals | silent_input |  silent file should decode silence without artifacts        | PASS/FAIL |

## Schedule

With the software specification and test plan in mind, here are the following
activities and the associated time estimate for each task.

- Target release version
- Target date
- Target product

## Project Milestones

- All milestones shall have the designation MS.d (e.g MS.3 for Milestone 3)
- There shall not be many milestones. If we have say, more than 7 milestones, it indicates there is insufficent clarity in the most important parts of the project and these milestones should be refined.

## Design Documentation

# Feature Design

- We shall include a high-level discussion of interface and patterns here.

# Implementation Discussion

- We shall discuss the details of implementation here.

## Analysis of Algorithms

### Overview

### Complexity Discussion

### Analysis of Data Structures

# Code Metrics

- We shall deliver some level of code metrics associated with every project to aid us in the measurement and understanding of code complexity and robustness.

## Unit Testing

- Gunit tests for this project are located in `//depot/etc./etc/`

## Valgrind Results

- We shall run Valgrind against our unit tests.
- See the following link for a Valgrind report (tbd).
- We had no unfree'd memory when running our tests against Valgrind.

## AddressSanitizier (ASAN) Results

- We shall run ASAN against our unit tests.
- We had no errors when running ASAN.

## Code Coverage percentage

- We shall use gcov to measure our code coverage.
- The link to our code coverage report is here (tbd).

## CPU Utilization

- We shall run `top` while running anacapa on our unit tests.
- The link to our cpu utilization report is tbd.

## Memory Utilization

- We shall measure dynamic memory utilization (heap usage) using valgrind-massif.
- We shall measure static memory utilization (stack usage) by compiling with -fstack-usage.

## System Level Tests

- We shall run automated tests against our build.
- We shall work with the automation team to create any new system level automated tests required to test our code.

### Automation coverage

# Documentation

- We shall use Doxygen in header files to document our code.
- Any new folders we create shall contain a README.md explaining the purpose of the folder.

## Percent of functions containing Doxygen

- We shall provide doxygen for 100% of methods used in our code.

## Percent of member variables with Doxygen strings

- We shall provide Doxygen for 100% of class member variables used in our code.

# Addendum

## What went right

- We shall discuss our successes in what we delivered and the good things that we can take forward with us to future endeavors.

## What didn't go exactly as planned

- We shall discuss lessons learned from executing this project and what we can take forward with us to future endeavors.

## Future Challenges

- We briefly discuss how this technology may change over time and what we may reasonably expect as the state-of-the-art advances.

# Acknowledgements

- Personnel are invited to express who we are grateful for in this section as no project is done in isolation.

# References

- List of important links and documents
