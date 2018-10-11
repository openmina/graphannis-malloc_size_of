Linux & MacOS: [![Build Status Linux & MacOS](https://travis-ci.org/corpus-tools/graphannis-malloc_size_of.svg?branch=develop)](https://travis-ci.org/corpus-tools/graphannis-malloc_size_of)
Windows: [![Build status Windows](https://ci.appveyor.com/api/projects/status/2gsjtakjpnpjvlnp/branch/develop?svg=true)](https://ci.appveyor.com/project/thomaskrause/graphannis-malloc-size-of/branch/develop)

# graphannis-malloc_size_of

This is a fork of the `malloc_size_of` crate, which is part of the [Servo codebase](https://github.com/servo/servo/tree/master/components/malloc_size_of) but not published on crates.io yet. 
The intention of this fork is to make the functionaility of the original crate available to the [graphANNIS](https://github.com/corpus-tools/graphANNIS) corpus search library, which is published on [crates.io](https://crates.io/crates/graphannis).


The following changes have been made in comparision to the original crate:
- References and implementations to internal/unpublished Servo crates have been removed.
- All dependencies have been made optional, so if you want to use the memory size calculation for types not the standard library you have to activate these as a feature. The following crates are available as optional dependencies/features:
    - app_units
    - cssparser
    - euclid
    - hyper
    - hyper_serde
    - serde
    - serde_bytes
    - smallbitvec
    - smallvec
    - string_cache 
    - thin-slice
    - time
    - url
    - void
    - xml5ever
