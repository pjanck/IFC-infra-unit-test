# IFC-infra-unit-test

This repository currently (as of 2021-09-02) contains IFC 4.3 files and is used in the IFC Infrastructure Extension Deployment project.

Moved from https://github.com/buildingSMART/Sample-Test-Files on 2021-09-02 following a decision on [too large repo size](https://github.com/buildingSMART/Sample-Test-Files/issues/88).

## Contribute

- Please use a separate folder for your contributions.
- Please use the [template](./UnitTestTemplate.md).
An example is provided [here](Georeferencing_1/readme.md).
- [Fork](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/working-with-forks) this repository. 
Make changes. 
Create a [pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork) to the main repository.
    - For a brief summary of `git` process, see [here](https://github.com/tumcms/Open-Infra-Platform/blob/development/Documentation/markdown/GitProcess.md). There are also a lot of online tutorials available.

## IFC STEP file header instructions

**NOTE:** There are no official Model View Definitions defined for IFC4.3 yet (as of 2021.02.02.). To avoid any errors vs schema checking, `ViewDefinition [Ifc4X3NotAssigned]` should be added in the header section of the file., i.e.

> FILE_DESCRIPTION (('ViewDefinition [Ifc4X3NotAssigned]'), '2;1');

**NOTE:** The current (2021.01.13.) correct version of IFC4.3 file schema in the physical file is `IFC4x3_RC2`, i.e.

> FILE_SCHEMA(('IFC4X3_RC2'));

## FAQ

### I don't know how to use `markdown`.

Please see [markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
Any text editor will do,
 or use one of the free online editors (e.g. [markdown-it](https://markdown-it.github.io/)).

### I wish to participate with my own example files.

Take note of the readme files and submit a pull request.
Contact `technical@buildingsmart.org` or `infrastructure@buildingsmart.org` (depending on the type of file) for help.

### I would like to include `*.*` files to the example files for reference (asked [here](https://github.com/buildingSMART/Sample-Test-Files/issues/17)).

Yes, of course. You can include multiple JPEGs if you see fit. Or IFC4 RV files. Or DWGs. Or PDFs. You should add anything that allows the other party to understand what is present in the IFC4x3 file.

### I have a question / comment / proposal regarding the documentation (resolved [here](https://github.com/buildingSMART/Sample-Test-Files/issues/92)).

Please open an issue here: https://github.com/buildingSMART/IFC/issues.

### How do I interpret the results from the checking procedure?

Consult [schema check documentation](./docs/ifc-and-md-check.md). 

**tl;dr**:

- If `inform-ifc` fails, there are schema problems with IFC files. Consult `IFC_check_results` artifact for further information.
- If `inform-md` fails, the MD files do not comply with the guidelines. Consult `MD_check_results` artifact for further information.
