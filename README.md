## **USING JEST TO TEST**

| Code used              | For                                     |
| ---------------------- | --------------------------------------- |
| npm init -y            | initizling it and answering yes to all. |
| npm i jest --save-dev  | downloading jest.                       |
| npm test -- --coverage | to test the coverage of your code.      |
|nvm install node        |installs node safely without messing up current node|
### example of coverage
________
 PASS  __tests__/filterByTerm.spec.js
  Filter function
    ✓ it should filter by a search term (link) (3ms)
    ✓ it should filter by a search term (uRl) (1ms)
    ✓ it should throw when searchTerm is empty string (2ms)

-----------------|----------|----------|----------|----------|-------------------|
File             |  % Stmts | % Branch |  % Funcs |  % Lines | Uncovered Line #s |
-----------------|----------|----------|----------|----------|-------------------|
All files        |     87.5 |       75 |      100 |      100 |                   |
 filterByTerm.js |     87.5 |       75 |      100 |      100 |                 3 |
-----------------|----------|----------|----------|----------|-------------------|
Test Suites: 1 passed, 1 total
Tests:       3 passed, 3 total
________
#### in coverage/icov-report/index.html you can see your coverage for your code
- hint:  pressing hte function cna show you resluts

### in package.json I changed the following code for jest testing

` "scripts": {
    "test": "jest"
  },`

### for coverage three options below for json


---

#### 1. f you want to keep code coverage always active configure Jest in **package.json** like so:

`  "scripts": {
    "test": "jest"
  },
  "jest": {
    "collectCoverage": true
  },`

#### 2. pass the flag to the test script:

` "scripts": {
    "test": "jest --coverage"
  },`

#### 3. If you're a visual person there's also a way to have an **HTML report for code coverage**, it's simply as configuring Jest like so:

`"scripts": {
    "test": "jest"
  },
  "jest": {
    "collectCoverage": true,
    "coverageReporters": ["html"]
  },`

---
