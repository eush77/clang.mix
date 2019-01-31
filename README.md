# clang.mix

This is a Clang front-end to [llvm.mix] extension. See the other repository
for details.

# Usage

To print results of the binding-time analysis for functions annotated with
`stage` attributes, pipe the output to `opt -analyze`:

    $ clang -S -emit-llvm -O1 tmp.c -o - | opt -analyze -bta

The specializer generator is already built into the Clang pipeline. Just print
the IR to take a look:

    $ clang -S -emit-llvm -O1 tmp.c

# Links

- [Extension to LLVM][llvm.mix]
- [Examples and micro benchmarks][mix-examples]

[llvm.mix]: https://github.com/eush77/llvm.mix
[mix-examples]: https://github.com/eush77/mix-examples
