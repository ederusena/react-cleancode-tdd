# react-cleancode-tdd

### install these packages
    "@types/node": "^17.0.23",
    "git-commit-msg-linter": "^4.1.1",
    "typescript": "^4.6.3"

### Initialize typescript config file
```sh
npx tsc --init
```

### Avoid commit with errors
```sh
npm i -D lint-staged husk
```

#### configure .lintstagerc.json
```json
{
  "*.{ts,tsx}": ["eslint 'src/**' --fix"]
}
```

#### configure .huskyrc.json
```json
{
  "hooks": {
    "pre-commit": "lint-staged"
  }
}
```

