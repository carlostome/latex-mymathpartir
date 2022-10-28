# mymathpartir

## Purpose

In [mathpartir](https://ctan.org/pkg/mathpartir) the name of an
inference rule can be specified as an optional argument to the macro
`\inferrule` as follows:

```tex
\[
  \inferrule[Name]{P}{C}
\]
```

To refer to this rule by its name, one can do so hardcoding the name
in the document (wrapped in `\LabTirName{}` to get the same
typesetting), for instance:

```tex
My rule \LabTirName{Name} does blabla
```

This is unsatisfactory because the rule name might change and the
whole document will need to be revised.

This package provides a wrapper over `\inferrule` which allows to
specify a `\label` command after an inference rule and use `\ref` to
retrieve its label. For example,

```tex
\[
  \inferrule[Name]{P}{C}\label{rule:R}
\]

My rule \ref{rule:R} does blabla.
```

For more examples see `mymathpartir.tex`.
