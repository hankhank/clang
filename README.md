# clang-format extended

This project is an extension of clang format to support more formatting styles
than the upstream project is willing to take on.

## Supported format styles

See http://clang.llvm.org/docs/ClangFormatStyleOptions.html for the default list

### NamespaceOnSingleLine

Controls whether a namespace is all on a single line. It supports
* None - All namespaces will be on a separate line
* ExceptAnonymous - All namespaces will be on single line except anonymous namespace braces
* All - All namespaces will be on a single line

All example
```
namespace a { namespace b { namespace c {
   
}}}
```

ExceptAnonymous example
```
namespace
{
}

namespace a { namespace b { namespace c {
   
}}}
```

### BraceWrapping::AfterIfElse

An extension of the custom BraceWrapping style intended to be used inconjunction with `BraceWrapping::BeforeElse`
To use you must set `BreakBeforeBraces: Custom` and ` raceWrapping: AfterIfElse: true`

example with BeforeElse and AfterIfElse enabled
```
if (cond_1)
{
}
else if (cond_2)
{
}
else
{
}
```
