# Janis Gertulla

Zig, Linux, and the low-level machinery underneath them.

I work on compilers, numerics, and asynchronous systems — mostly in Zig 0.16,
occasionally in Rust and C. My interest is in the parts that are specified
precisely and can be checked: floating-point rounding, interval enclosures,
instruction selection, the shape of an `Io`.

## Things I build

Most of this is private while it is in progress. What is public is finished
enough to read.

| | |
|---|---|
| [`zmath`](https://github.com/CoffeeImpliesCode/zmath) | IEC 60559 elementary functions for Zig, across `f16`/`f32`/`f64` and `@Vector`s, implemented against the standard rather than the platform libm |
| [`zmath-testing`](https://github.com/CoffeeImpliesCode/zmath-testing) | Independent verification for the above — differential oracles, corpus replay, fuzzing, benchmarks |
| [`zig-interval`](https://github.com/CoffeeImpliesCode/zig-interval) | Rigorous interval arithmetic with outward rounding |
| [`zig-agent-proto`](https://github.com/CoffeeImpliesCode/zig-agent-proto) | MCP and ACP protocol library and runtime for Zig |
| [`ocean`](https://github.com/CoffeeImpliesCode/ocean) | Compiler infrastructure and the `occ` driver |
| [`vain`](https://github.com/CoffeeImpliesCode/vain) | SSA-form intermediate representation |
| [`kernel`](https://github.com/CoffeeImpliesCode/kernel) | `io_uring`-shaped async I/O micro kernel, freestanding |

Also: `zautomerge` (a direct Zig translation of the Automerge CRDT),
[`zio`](https://github.com/lalinsky/zio) (async I/O), `ozai`, `skript`,
`tinyfold` (biomolecular structure), `zcov`, `zbc`, `ziglint`.

## How I work

Specifications first, and tests that can disagree with the code. A test suite
that shares code with the thing it checks only confirms the code agrees with
itself, so the verification for each library lives in a separate repository that
reaches it through its published API.

Correctness claims get evidence attached: pinned identities, retained receipts,
differential runs against implementations that were not written alongside the
thing under test.

## Elsewhere

- [coffeeimpliescode.com](https://coffeeimpliescode.com)
- Most of my work-in-progress is private; ask if something interests you.

<!-- vim: set filetype=markdown -->