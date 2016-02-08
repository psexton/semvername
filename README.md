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

`NAME-SEMVER`

In other words, a name part, followed by a hyphen, followed by a semver part. The definition of "name" and "semver" differ depending on the version of SemVerName you are using. (Yes, the SemVerName format is semantically versioned, just like the SemVer format is.)

### 2.0.0

* `NAME` consists of lowercase letters, digits, hyphens, and underscores. It cannot be empty or begin with a hyphen or underscore.
* `SEMVER` is a string that conforms to version 2.0.0 of SemVer.

### 1.0.0

* `NAME` consists of alphanumeric characters, hyphens, and underscores.
* `SEMVER` is a string that conforms to version 1.0.0 of SemVer.

### Terms

* lowercase letter: U+0061 to U+007A, inclusive.
* digits: U+0030 to U+0039, inclusive.
* hyphen: U+002D.
* underscore: U+005F.
* alphanumeric character: U+0030 to U+0039, inclusive, or U+0041 to U+005A, inclusive, or U+0061 to U+007A, inclusive.

FAQ
---

Q. Why not allow Unicode? Or spaces?

A. Thank you, that is a great question. I have a dream that someday ASCII will be as faint of a memory as EBCDIC is today, and UTF-8 will be The One True Encoding. Someday, when I'm old and gray and all of my code is rotting away, perhaps that will be true.

In the meantime, restricting the character set for a valid SemVerName allows them to exist damn near anywhere: as identifiers in URLs, and as filenames on even the most awkward of filesystems.

License
-------

[Creative Commons Attribution 4.0 International (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/)
