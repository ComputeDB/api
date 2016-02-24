# ComputeDB API

Python API.

```python
# import the library
from computedb import compute

## perform the job
result = compute(123, 234, task='Add')

print(result) # prints 357
```

Javascript API.

```js
// import the library
var compute = require('computedb-api')

// specify what to compute
var jobSpec = {task: 'Add', 0: 123, 1: 234}

// make it so
compute(jobSpec, function (err, resp) {
  console.log(resp) // prints 357
})
```

Purescript API.

```purescript
import Database.ComputeDB (compute, CoDB)
import Control.Monad.Aff (Aff)

makeItSo :: ∀ e. Aff (con :: CONSOLE, db :: CoDB | e) Unit
makeItSo = do
  result <- compute "Add" {"0": 123, "1": 234}
  log $ show result -- prints 357
```
