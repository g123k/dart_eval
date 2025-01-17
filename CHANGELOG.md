## 0.4.2
- Fix analyzer version constraint

## 0.4.1
- Fix a potential crash when resolving common base types.
- Support for calling methods on a bridge class's supertype without having to
  declare the method on the subtype's declaration.
- Documentation improvements

## 0.4.0
- (Breaking) You must now specify the `bridge` or `wrap` parameter in a
  `BridgeClassDef`
- (Breaking) You must now specify `isBridge: true` when registering a bridge
  class constructor with `runtime.registerBridgeFunc()`
- Support for bridged (only) enums
- Support for variable captures inside closures
- Support for implicit class field accesses including `this` and `super` in 
  closures
- Bridge declarations are now merged with a Dart source file of the same URI, if
  one exists
- Basic support for top-level variables and static fields
- Support for bool literals and logical and/or
- Support `String.substring()` (thanks to @maks)
- Now using continuous integration (thanks to @maks)
- Various bug fixes and code cleanups

## 0.3.0
- (Breaking) Modified public API for defining bridge classes. See Pub example.
- (Breaking) Relative import URIs may no longer work (it's unclear whether they
  worked before). Support will be re-added in a future release.
- (Deprecated) `Runtime.executeNamed()` is deprecated. Use `Runtime.executeLib()`
  instead.
- Compiler now uses graphs to compose libraries from imports, exports, and parts,
  and should now mostly follow the Dart spec.
- Partial support for `show` and `hide` on imports and exports
- Support defining `extends`, `implements`, and `with` on bridge classes
- Support for adding files to the compiler before compiling, for use in bridge
  libraries to enable exports.
- Add recursion guard for type resolution

## 0.2.0

- Partial support for anonymous functions and the Dart runtime type system
- New serializable interop descriptor classes to allow for code push in the future
- Runtime overrides
- Implement collection `if` for Lists
- Support for `async`/`await` via continuations, as well as `Future.then()`
- Basic CLI

## 0.1.0

- Rebuilt from the ground up around the new DBC bytecode compiler
- Public API changes: see readme
- Massive performance improvements, up to 350x
- Support for the Dart type system (compile-time checks only)
- Refactor class system to support `super`
- New simpler Bridge interop that also allows const classes

## 0.0.4

- Add support for `if`, basic `for`, number comparison operators, and postfix `++`
- Fix `+`, `-`, `*`, and `/` operators
- Improve performance significantly

## 0.0.3

- Make the Pub analyzer happy
- Add some Dartdoc comments

## 0.0.2

- Fix scoping
- Add support for List and Map types

## 0.0.1

- Create parser and interpreter
- Add interop