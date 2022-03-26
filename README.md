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
