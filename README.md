# Node.js path delimiter test on Windows


```javascript
require('..\\sub\\sub');   // OK✅
require('../sub\\sub');    // OK✅
require('.\\sub');         // NG❌
require('./sub');          // OK✅
import '..\\sub\\sub.mjs'; // NG❌
import '../sub\\sub.mjs';  // OK✅
import '.\\sub.mjs';       // NG❌
import './sub.mjs';        // OK✅
```

prepending `./`:

```javascript
require('./..\\sub\\sub');   // OK✅
require('./../sub\\sub');    // OK✅
require('./.\\sub');         // OK✅
require('././sub');          // OK✅
import './..\\sub\\sub.mjs'; // OK✅
import './../sub\\sub.mjs';  // OK✅
import './.\\sub.mjs';       // OK✅
import '././sub.mjs';        // OK✅
```
