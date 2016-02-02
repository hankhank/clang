# clang-format extended

This project is an extension of clang format to support more formatting styles
than the upstream project is willing to take on.

This branch is occasionally rebased against the upstream projects master branch but hankhank/llvm and hankhank/clang-tools-extra
are always kept in step.

## Supported format styles

See http://clang.llvm.org/docs/ClangFormatStyleOptions.html for the default list

### NamespaceOnSingleLine

Controls whether a namespace is all on a single line. It supports
* None - All namespaces will be on a separate line
* ExceptAnonymous - All namespaces will be on single line except anonymous namespace braces
* All - All namespaces will be on a single line

All example

    namespace a { namespace b { namespace c {
       
    }}}

ExceptAnonymous example

    namespace
    {
    }
    
    namespace a { namespace b { namespace c {
       
    }}}

### BraceWrapping::AfterIfElse

An extension of the custom BraceWrapping style intended to be used inconjunction with `BraceWrapping::BeforeElse`
To use you must set `BreakBeforeBraces: Custom` and ` raceWrapping: AfterIfElse: true`

example with BeforeElse and AfterIfElse enabled

     if (cond_1)
     {
     }
     else if (cond_2)
     {
     }
     else
     {
     }

### SpaceAfterTemplateKeyword
If `true`, a space may be inserted between the 'template' keyword and the following '<'.

example

     template<> class Foo<int> {}

### BreakInheritanceBeforeComma
Always break inheritance lists before commas and align the commas with the colon.
Mirror of BreakConstructorInitializersBeforeComma.

### InheritanceAllOnOneLineOrOnePerLine
If the base class list doesn't fit on a line, put each base class on its own line.
Mirror of ConstructorInitializerAllOnOneLineOrOnePerLine.

### SpacesBetweenFunctionParameter
If ``true``, a space will be inserted between several function parameters.

### DisableRegion
Turns off clang formatting between DisableRegionBegin DisableRegionEnd regexes matches

# Contributors

Thanks to all those contributing!

1. Andrew Hankins(hankhank)
2. strager
3. Kai Wolf(NewProggie)
