# clang-format extended

This project is an extension of clang format to support more formatting styles
than the upstream project is willing to take on.

## Supported format styles

See http://clang.llvm.org/docs/ClangFormatStyleOptions.html for the default list

### NamespaceOnSingleLine

If set to true all namespace blocks will occur on a single line

example
```
namespace a { namespace b { namespace c {
   
}}};
```

### BraceWrapping::AfterIfElse

An extension of the custom BraceWrapping style. To use you must set `BreakBeforeBraces: Custom`

example
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
