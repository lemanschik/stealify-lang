# Types
A Typesystem that is TypeScript Compatible but does not depend on it. 
In General this implements a so called Functional Type System in general something that you would normaly add via tooling anyway but we directly do it
in a expressiv way

```ts
const TypeUnderlyingSource = (any) => 
    /** @type {UnderlyingSource<any>} */ 
        (/** @type {unknown} */ (any));
```

This type for example solves the problem that Typescript is not Awaare of UnderlyingSource Implementations and it can be used via import
like a typeScript type but it also can get transpiled or shimed for instrumentation. This is best practieces at its best.

All type symbols can be referenced and analyzed via walking the ast for nodes that do not apply any changes to the node and return the args 
without additional side effects similar to the concept of treeShaking.
