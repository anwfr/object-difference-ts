# object-difference-ts
- Get the difference between two object structures
- Support for Array, Map, object properties
- Typescript
- Quick-diff for large objects/maps: compare object size instead of each property for large objects

## Usage

### Get diffs

```javascript
import {getDifference} from '../lib/object-difference-ts'

let diff = getDifference(foo, bar)
```


### Get quickdiffs (better performances for large objects)

```javascript
import {getDifference, setQuickDiffTresholdDefault} from '../lib/object-difference-ts'

// will compare objets/maps size when they have more than 1000 entries
// will compare their properties/entries when they have less than 1000 entries
let options = {quickDiffTreshold:1000}
let diff = getDifference(foo, bar, options)


// setting quickdiffTreshold globally
setQuickDiffTresholdDefault(1000)

let diff2 = getDifference(foo, bar)
```

## To do
- package as NPM module
- tests

## Credits
- [object-difference](https://github.com/xaviervia/object-difference)