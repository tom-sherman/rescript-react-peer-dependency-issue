Steps to reproduce:

```
cd dependency
npm link
cd ../consumer
npm i
npm link dependency
npm start
```

Expected:

Built package:

Actual:

```
FAILED: src/Dependency.cmj

  We've found a bug for you!
  ~/dependency/src/Dependency.res:2:19-21

  1 │ @react.component
  2 │ let make = () => <div> {"Hello"->React.string} </div>
  3 │ 

  The value div can't be found

FAILED: cannot make progress due to previous errors.
```
