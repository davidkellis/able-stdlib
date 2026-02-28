# Able Standard Library

The standard library for the [Able programming language](https://github.com/davidkellis/able).

## Installation

Add to your project's `package.yml`:

```yaml
dependencies:
  able: "0.1.0"
```

Then run:

```
able deps install
```

Or, if you don't have a manifest, run `able setup` to install the stdlib globally.

## Modules

- **core** — errors, interfaces (Display, Clone, Eq, Hash, Iterator, etc.), options (Option, Result), iteration, numeric
- **collections** — Array, HashMap, HashSet, LinkedList, Vector, Deque, Queue, Heap, TreeMap, TreeSet, BitSet, LazySeq
- **text** — string iteration/manipulation, regex (literal-only), ASCII classification
- **numbers** — BigInt, BigUInt, Rational, extended integer types
- **concurrency** — Future, Channel, Mutex wrappers
- **io** — streams, filesystem, path helpers
- **math** — math utilities

## Usage

Import modules with the `able.` prefix:

```able
import able.collections.hash_map.{HashMap}
import able.core.options.{Option, Some, None}
```

## License

EPL-2.0
