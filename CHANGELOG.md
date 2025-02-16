<!-- Keep a Changelog guide -> https://keepachangelog.com -->

Changelog for intellij-elm 
==========================


**5.0.0** _(2022-03-20)_
*   Enable support for newer versions of IntelliJ (v2021.1 and greater)
*   Based on [intellij-platform-plugin-template](https://github.com/JetBrains/intellij-platform-plugin-template) (new Gradle build spec)
*   Support [Lamdera](https://dashboard.lamdera.app/docs) projects
*   Support [`elm-review`](https://github.com/jfmengels/elm-review)
*   Improved navigation and UI for compiler and `elm-review` Toolwindows with correct IntelliJ appearance setting (light, dark, ...)
*   Support multiple Elm-main entry points (compile all)

**4.4.1** _(2021-09-20)_
*   Enable support for all newer versions of IntelliJ (future versions introduce incompatibilities)

**4.4.0** _(2021-04-01)_
*   Enable support for IntelliJ 2021.1.x
*   Add intention for inserting parens around expressions
*   Reword 'new elm file' menu option

**4.3.1** _(2021-01-30)_
*   Fix 'extract variable' on pipeline expressions
*   Add intention for inserting `Debug.log` statements

**4.3.0** _(2020-11-24)_
*   Implement new project wizard for WebStorm
*   Add more control over how types are exposed.
*   Add intention to convert record constructor function to record literal
*   Optimize 'Find Usages' so that it only looks at `*.elm` files
*   Only show New Elm File option inside Elm source directories
*   Added support for IntelliJ 2020.3

**4.2.0** _(2020-09-03)_
*   Added intention for creating (and removing) pipelines
*   Added code completion for fields in record expressions
*   Fixed an exception that could occur when elm-format runs automatically on-save

**4.1.0** _(2020-08-27)_
*   Automatically configures path to Elm tools and the `elm.json` file
*   Package dependencies are now installed automatically
*   New project template has updated `elm.json` package dependencies
*   Added intentions for converting between regular and triple-quoted strings
*   Allow elm-format to run on-save even if there are syntax errors
*   Fixed bugs in the Elm Compiler tool window

**4.0.0** _(2020-08-18)_
*   Removed support for Elm 0.18
*   Added a quick-fix to convert List.map to List.foldr
*   Major improvements to dependency version resolution
*   Go-to-declaration now works for indirect dependencies

**3.5.4** _(2020-07-28)_
*   Added support for IntelliJ 2020.2

**3.5.3** _(2020-04-14)_
*   Fixed missing icons in the Elm tool window when running IntelliJ 2020.1
*   Fixed a regression in the 'add import' feature related to types in union variants

**3.5.2** _(2020-04-08)_
*   Improved sorting of modules when performing 'add import'
*   Added a hint popup to add an import to fix an unresolved reference
*   Fixed a 'add import' bug where types and values were mixed up in some cases
*   Fixed a shadowing error false negative involving `let`/`in` expressions
*   Type Inference optimizations: reduced memory usage, etc.

**3.5.1** _(2020-02-05)_
*   Fixed 2 bugs related to function/type name resolution
*   Enable support for IntelliJ 2020.1 EAP

**3.5.0** _(2020-01-23)_
*   Major performance optimizations
*   CSS colors are now shown in the gutter and can be edited using a color picker
*   Added "breadcrumbs" UI
*   Syntax highlighting can now distinguish between doc comments and other comments
*   Generated code now honors your indent size config
*   Tests can now be run from non-standard locations
*   Line markers can now be disabled individually
*   Duplicate function/type definitions are now marked as an error
*   Tuples with more than 3 elements are now marked as an error
*   Attempting to use `(..)` on a type alias is now marked as an error
*   Added troubleshooting instructions for `nvm` configurations

**3.4.6** _(2019-12-23)_
*   Live templates are now suggested in appropriate contexts only
*   Fixed a type inference bug (ConcurrentModificationException)

**3.4.5** _(2019-11-30)_
*   Added nested functions/values to Structure View
*   Added scroll-from-source in Structure View
*   Fixed 'New Project Wizard' bug on IntelliJ 2019.3

**3.4.4** _(2019-11-25)_
*   Improved generation of function params from a type annotation
*   Improved commenter to play nicely with elm-format
*   Fixed a bug with the Elm Compiler panel where it found the wrong entry-point
*   Fixed a stack overflow in type inference on some malformed programs
*   Fixed refs to union constructors in arguments to other constructors in patterns

**3.4.3** _(2019-09-29)_
*   Parser performance improvements in deeply nested functions
*   Improved type checking of case expressions
*   Fixed various cache invalidation bugs

**3.4.2** _(2019-09-06)_
*   Fix ConcurrentModificationException
*   Fix false positives for some unused record fields
*   Improve type checking of recursive functions
*   Improve type checking of de-structured record fields

**3.4.1** _(2019-08-24)_
*   Fixed bugs related to record field rename
*   Fixed a bug in Elm 0.18 projects related to the \`elm-stuff\` directory

**3.4.0** _(2019-08-18)_
*   Added record field 'rename refactoring'
*   Added go-to-declaration and find usages for record fields
*   Added intention to generate JSON encoders and decoders
*   Added intention to qualify an unresolved ref with its module name
*   Added a gutter line marker for recursive functions
*   Added quick fix to rename unused patterns to `_`
*   Added ability to suppress inspection with a comment
*   Fixed a bug when generating type annotations
*   Improved type checker errors for `case` branches
*   Improved performance in very large projects

**3.3.0** _(2019-07-29)_
*   Added "introduce variable" refactoring (creates a `let`/`in` for selected expression)
*   Added syntax highlighting for record fields and made everything more consistent
*   Improved record type errors by showing a diff of mismatched fields
*   Added an inspection for detecting unused module alias imports

*   Plus some more bug fixes
**3.2.1** _(2019-07-16)_
*   Fixed a bug in 2019.2 EAP related to the Elm Settings UI
*   Improved logic for locating packages in Elm's global package cache

**3.2.0** _(2019-07-11)_
*   Added an intention that generates a type annotation for un-annotated functions
*   Significantly reduced memory usage in large projects
*   Improved handling of nested let functions

**3.1.2** _(2019-05-28)_
*   Fixed a type inference bug related to curried functions
*   Fixed a stack overflow crash in some recursive functions
*   Allow named suffixes on special type variables: `comparable`, `number`, etc.

**3.1.1** _(2019-04-06)_
*   The type system is now fully implemented!
*   Finished full-program type unification/inference
*   Explicit imports now shadow wildcard imports
*   Elm compiler tool-window UI now shows path to file target and is scrollable
*   Allowed elm-format to run even if there are syntax errors

**3.1.0** _(2019-03-18)_
*   Add Elm compiler integration to check errors
*   Bug fixes for type inference

**3.0.1** _(2019-03-06)_
*   Added "auto test" support in the elm-test runner
*   Fixed elm-test runner on Elm 0.18 projects
*   Reduced false negatives in the unused code inspection
*   Fixed a parse error for arithmetic negation
*   Fixed a variety of minor bugs related to elm-format

**3.0.0** _(2019-02-25)_
*   Added support for elm-format: via keybinding or automatically-on-save
*   Added UI for running elm-test and viewing test results
*   Added support for WebGL/GLSL
*   Various bug fixes

**2.2.4** _(2019-02-13)_
*   The type checker now detects problems with type variables
*   Added support for introducing an aliased import from an unresolved qualified ref
*   Added a template for creating a new Elm project
*   Added quick docs for infix operators
*   Lots of bug fixes

**2.2.3** _(2019-02-06)_
*   Record field completion now works even in the presence of parse errors
*   More performance improvements
*   Bug fixes for type checker
*   Added support for exponential notation on number literals

**2.2.2** _(2019-01-28)_
*   Improvements to 'create function from type annotation' intention
*   Bug fixes for 'new Elm file' generator
*   Performance improvements

**2.2.1** _(2019-01-13)_
*   Add 'complete current statement' support for `case`/`of`, `let`/`in`, `if`/`else` and function declarations
*   Bug fixes for unused code inspections
*   Bug fixes for type checker
*   Reduced memory usage

**2.2.0** _(2019-01-06)_
*   Add inspections for unused functions, parameters, imports, etc.
*   Add 'Optimize Imports' quick fix
*   New intention actions for adding/removing a function/type from the exposing list
*   Improved 'New Elm File' action
*   Improve name resolution for test modules and dependencies
*   Improve 'extend selection' to also grab the function's type annotation
*   Importing and exposing a custom type variant constructor now exposes all
*   Performance improvements

**2.1.1** _(2018-12-20)_
*   Add inspection and enter handler to complete case branches
*   Do code completion for functions & types even when module not imported
*   Aliased imports now hide the original module name from qualified refs
*   Improved type checking

**2.1.0** _(2018-12-01)_
*   Added code completion for accessing fields in a record
*   Performance improvements
*   Improved type inference

**2.0.3** _(2018-11-16)_
*   Improved function generation from a type annotation
*   Improved type inference and added more error checking
*   Added a line marker for exposed functions/types
*   Fixed bugs related to 'test-dependencies'

**2.0.2** _(2018-11-08)_
*   Type checking bug fixes
*   Improvemented 'Find Usages'

**2.0.1** _(2018-11-03)_
*   Added 'Parameter Info' support; bug fixes

**2.0.0** _(2018-10-31)_
*   Added type inference and type checking
*   Added support for multiple Elm projects

**1.3.3** _(2018-09-20)_
*   Add Elm tool window listing attached projects
*   Parser bug fix

**1.3.2** _(2018-09-08)_
*   Add code folding; various bug fixes

**1.3.1** _(2018-08-26)_
*   Add support for Elm 0.19 package projects

**1.3.0** _(2018-08-09)_
*   Add quick docs
*   Add rename file/module refactoring
*   Add support for Elm 0.19 beta

**1.1.1** _(2018-05-15)_
*   Fix crash on PyCharm and WebStorm

**1.1.0** _(2018-05-10)_
*   Smart indent
*   Performance improvements
*   Better parse error recovery

**1.0.0** _(2018-04-11)_
*   Improved parse error recovery and added keyword completion

**0.9.1** _(2017-12-28)_
*   Added 'Import' quick fix for unresolved references
