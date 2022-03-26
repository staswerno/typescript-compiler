## The Typescript Compiler

### watch mode

tsc app.ts -w  
_don't close during dev_
_won't compile with errors_

### global tsc

tsc --init  
_only required once_
_then just tsc_

tsc -w  
_for global watch mode_

### multiple files

tsconfig.json

```...
    "skipLibCheck": true
  },
 "exclude": ["", ""],
"include": ["", ""],
"files": ["", ""],
  }
```

_common to exclude node_modules, but it is excluded by default_  
_complies as include minus exclude_

### compiler options

tsconfig.json

- target
  - es6 === es2015
- modules
  - coming back to later
- lib
  - eg ["dom", "es6", "dom.iterable", "scripthost"]
    - but this is default for es6 so not needed to add
- allowJs/checkJs
  - can use some TS features in JS
- SourceMap
  - helps with dev/debugging
  - set to true to create map files to debug in dev tools
- **outDir/rootDir**
  - good for cleaner project structure
  - replicates folder structure
  - set output files to dist when ts files in src
- **remove comments**
- noEmitOnError
  - doesn't generate problematic files
- strict options
  - set various strict checks to true/false#
- code quality options
  - noUnusedLocals
  - noUnusedParameters
  - noImplicitReturns (maybe)
