## Contributing to ps2-cpp20-primer

## Commit message formatting

I use a sort of variant of Andreas Kling's commit guidelines.

In the case that your commit does not change any Elfldr C++ source files, use `[ci skip]` so that Actions does not need to run for it.

```
(optional: [ci skip]) Some small commit description here

A longer description of what this commit does,
alongside any description of unrelated changes,
if applicable.
```

## Code formatting

We use clang-format. Pretty much, just make sure you run `clang-format` on any PR code.
