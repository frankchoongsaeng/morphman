# INTRODUCTION

Morphman is an attempt at creating a package manager for [Morphir](https://morphir.finos.org/).

## Some thoughts

> Morphir itself doesn't have a runtime, so maybe package management doesn't really make sense for it.
Nonetheless, this is a fun (and potentially useful project) that will be immediately useful to the insight page.

This tool is built with other Morphir tooling as it's main benefactor. 
The immediate tool under consideration is the Morphir develop webapp that provides insight into the morphir-ir.

This project will be split into parts:
- interacting with storage platform (CR[UD] on FS/DB/Cloud etc)
- managing dependencies (dependency tree and resolution)
- packaging and distribution (creating and specifying a dependency)

The project will provide libraries in every language, starting with Scala to integrate with Morphman.
However, it must only work with the IR, ie, the IR is the primary element being processed.

## Packaging

The current structure of the IR isn't sufficient for package management. 
Morphman will introduce its own distribution format that adds additional information ontop of the IR.

### Morphman Distribution: 
- format-version: this is the distribution format for morphir
- dist-version: this is the version of the package
- dependencies: list of morphman specifications
- modules: list of modules
    
### Morphman 