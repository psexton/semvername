semvername
==========

A specification for semanticly versioned names. http://semvername.org

Why Do Names Need To Be Versioned?
----------------------------------

Semantic Versioning (or SemVer) is great. Version numbering for any project should use that. There's no need to reinvent it. If you haven't heard of Semantic Versioning, go spend 5 minutes at [semver.org](http://www.semver.org).

But sometimes just a version number isn't enough.

* I have a list of releases that I need to display/sort/etc. What data type do I shove this info into?
* I have more than one tool in the same repository. What do I call my tags?
* What do I call the folder this tool lives in? Or its executable? or its installer?

Semanticly Versioned Names (or SemVerNames) are a documented way to combine a project name and a version in a single string.

They make an excellent choice for standardizing whenever you have a project name + release version combination.

Syntax
------

The syntax for a semvername is very simple. A valid SemVerName has the form:

NAME-SEMVER

where SEMVER is a valid Semantic Version, and NAME consists of alphanumeric characters, hyphens, and underscores.

Version 1.0.0 of SemVerName uses version 1.0.0 of SemVer.
Version 2.0.0 of SemVerName uses version 2.0.0 of SemVer.

(Yes, the SemVerName format is semantically versioned, just like the SemVer format is.)

FAQ
---

Q. Why not allow Unicode? Or spaces?

A. Thank you, that is a great question. I have a dream that someday ASCII will be as faint of a memory as EBCDIC is today, and UTF-8 will be The One True Encoding. Someday, when I'm old and gray and all of my code is rotting away, perhaps that will be true.

In the meantime, restricting the character set for a valid SemVerName allows them to exist damn near anywhere: as identifiers in URLs, and as filenames on even the most awkward of filesystem.s  
