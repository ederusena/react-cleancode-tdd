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

### Add jest
```sh
npm i -D jest @types/jest ts-jest
```

#### configure jest.config.js
```js
module.exports = {
  roots: ['<rootDir>/src'],
  collectCoverageFrom: ['src/**/*.{js,jsx,ts,tsx}'],
  coverageDirectory: 'coverage',
  testEnvironment: 'node',
  transform: {
    '.+\\.(js|jsx|ts|tsx)$': 'ts-jest'
  }
}
```