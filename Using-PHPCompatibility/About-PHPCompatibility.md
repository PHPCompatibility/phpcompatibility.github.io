---
sort: 1
---

# About PHPCompatibility

PHPCompatibility is a set of sniffs for [PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) that checks for PHP cross-version compatibility.
It will allow you to analyse your code for compatibility with higher and lower versions of PHP.

## What PHPCompatibility can detect





## What PHPCompatibility can NOT detect

Due to the nature of static analysis, there are certain PHP cross-version incompatibilities which this PHPCompatibility will not be able to detect.

> Static analysis is a form of code analysis where the code is machine-read, not run.

In practice, this means that PHPCompatibility will not have access to the _runtime_ type or value of variables.

At times, the _type_ of a variable can be guestimated using parameter type declarations, or information provided in the docblock of a function, but any such _guestimate_ will fall short if the variable is subsequently changed within the function or if the documentation is inaccurate.

Any changes to the PHP engine which could impact code, which would require access to the _runtime_ type or value of variables, are therefore not detectable by PHPCompatibility.

Along the same lines, due to this tool having been build on top of the PHP_CodeSniffer tooling, any changes to the PHP engine which would require cross-file analysis of a code-base for accurate detection, again, are changes which PHPCompatibility can not detect.


## Current status

The project aims to cover all PHP compatibility changes, which can conceivable be "sniffed", introduced since PHP 5.0 up to the latest PHP release. This is an ongoing process and coverage is not yet 100% (if, indeed, it ever could be). Progress is tracked on [our GitHub issue tracker](https://github.com/PHPCompatibility/PHPCompatibility/issues).

Pull requests that check for compatibility issues in PHP 4 code - in particular between PHP 4 and PHP 5.0 - are very welcome as there are still situations where people need help upgrading legacy systems. However, coverage for changes introduced before PHP 5.1 will remain patchy as sniffs for this are not actively being developed at this time.
