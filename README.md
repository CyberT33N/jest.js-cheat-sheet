# Jest.js Cheat Sheet
Jest.js Cheat Sheet with the most needed stuff..












<br><br>
<br><br>
 _____________________________________________________
 _____________________________________________________
<br><br>
<br><br>


# jest.config.ts

<br><br>

## Next.js Example
```javascript
/**
 * For a detailed explanation regarding each configuration property, visit:
 * https://jestjs.io/docs/configuration
 */

import type {Config} from 'jest'
import nextJest from 'next/jest.js'

const createJestConfig = nextJest({
    // Provide the path to your Next.js app to load next.config.js and .env files in your test environment
    dir: './'
})

const config: Config = {
    // All imported modules in your tests should be mocked automatically
    // automock: false,

    // Stop running tests after `n` failures
    // bail: 0,

    // The directory where Jest should store its cached dependency information
    // cacheDirectory: "/tmp/jest_rs",

    // Automatically clear mock calls, instances, contexts and results before every test
    clearMocks: true,

    // Indicates whether the coverage information should be collected while executing the test
    collectCoverage: true,

    // An array of glob patterns indicating a set of files for which coverage information should be collected
    // collectCoverageFrom: undefined,

    // The directory where Jest should output its coverage files
    coverageDirectory: 'coverage',

    // An array of regexp pattern strings used to skip coverage collection
    // coveragePathIgnorePatterns: [
    //   "/node_modules/"
    // ],

    // Indicates which provider should be used to instrument code for coverage
    coverageProvider: 'v8',

    // A list of reporter names that Jest uses when writing coverage reports
    // coverageReporters: [
    //   "json",
    //   "text",
    //   "lcov",
    //   "clover"
    // ],

    // An object that configures minimum threshold enforcement for coverage results
    // coverageThreshold: undefined,

    // A path to a custom dependency extractor
    // dependencyExtractor: undefined,

    // Make calling deprecated APIs throw helpful error messages
    // errorOnDeprecated: false,

    // The default configuration for fake timers
    // fakeTimers: {
    //   "enableGlobally": false
    // },

    // Force coverage collection from ignored files using an array of glob patterns
    // forceCoverageMatch: [],

    // A path to a module which exports an async function that is triggered once before all test suites
    // globalSetup: undefined,

    // A path to a module which exports an async function that is triggered once after all test suites
    // globalTeardown: undefined,

    // A set of global variables that need to be available in all test environments
    // globals: {},

    // The maximum amount of workers used to run your tests. Can be specified as % or a number. E.g. maxWorkers: 10% will use 10% of your CPU amount + 1 as the maximum worker number. maxWorkers: 2 will use a maximum of 2 workers.
    // maxWorkers: "50%",

    // An array of directory names to be searched recursively up from the requiring module's location
    // moduleDirectories: [
    //   "node_modules"
    // ],

    // An array of file extensions your modules use
    // moduleFileExtensions: [
    //   "js",
    //   "mjs",
    //   "cjs",
    //   "jsx",
    //   "ts",
    //   "tsx",
    //   "json",
    //   "node"
    // ],

    // A map from regular expressions to module names or to arrays of module names that allow to stub out resources with a single module
    // moduleNameMapper: {},

    // An array of regexp pattern strings, matched against all module paths before considered 'visible' to the module loader
    // modulePathIgnorePatterns: [],

    // Activates notifications for test results
    // notify: false,

    // An enum that specifies notification mode. Requires { notify: true }
    // notifyMode: "failure-change",

    // A preset that is used as a base for Jest's configuration
    // preset: undefined,

    // Run tests from one or more projects
    // projects: undefined,

    // Use this configuration option to add custom reporters to Jest
    // reporters: undefined,

    // Automatically reset mock state before every test
    // resetMocks: false,

    // Reset the module registry before running each individual test
    // resetModules: false,

    // A path to a custom resolver
    // resolver: undefined,

    // Automatically restore mock state and implementation before every test
    // restoreMocks: false,

    // The root directory that Jest should scan for tests and modules within
    // rootDir: undefined,

    // A list of paths to directories that Jest should use to search for files in
    // roots: [
    //   "<rootDir>"
    // ],

    // Allows you to use a custom runner instead of Jest's default test runner
    // runner: "jest-runner",

    // The paths to modules that run some code to configure or set up the testing environment before each test
    setupFiles: ['<rootDir>/test/setup-tests.ts']

    // A list of paths to modules that run some code to configure or set up the testing framework before each test
    // setupFilesAfterEnv: [],

    // The number of seconds after which a test is considered as slow and reported as such in the results.
    // slowTestThreshold: 5,

    // A list of paths to snapshot serializer modules Jest should use for snapshot testing
    // snapshotSerializers: [],

    // The test environment that will be used for testing
    // testEnvironment: "jest-environment-node",

    // Options that will be passed to the testEnvironment
    // testEnvironmentOptions: {},

    // Adds a location field to test results
    // testLocationInResults: false,

    // The glob patterns Jest uses to detect test files
    // testMatch: [
    //   "**/__tests__/**/*.[jt]s?(x)",
    //   "**/?(*.)+(spec|test).[tj]s?(x)"
    // ],

    // An array of regexp pattern strings that are matched against all test paths, matched tests are skipped
    // testPathIgnorePatterns: [
    //   "/node_modules/"
    // ],

    // The regexp pattern or array of patterns that Jest uses to detect test files
    // testRegex: [],

    // This option allows the use of a custom results processor
    // testResultsProcessor: undefined,

    // This option allows use of a custom test runner
    // testRunner: "jest-circus/runner",

    // A map from regular expressions to paths to transformers
    // transform: undefined,

    // An array of regexp pattern strings that are matched against all source file paths, matched files will skip transformation
    // transformIgnorePatterns: [
    //   "/node_modules/",
    //   "\\.pnp\\.[^\\/]+$"
    // ],

    // An array of regexp pattern strings that are matched against all modules before the module loader will automatically return a mock for them
    // unmockedModulePathPatterns: undefined,

    // Indicates whether each individual test should be reported during the run
    // verbose: undefined,

    // An array of regexp patterns that are matched against all source file paths before re-running tests in watch mode
    // watchPathIgnorePatterns: [],

    // Whether to use watchman for file crawling
    // watchman: true,
}

// createJestConfig is exported this way to ensure that next/jest can load the Next.js config which is async
export default createJestConfig(config)
```

<br><br>
<br><br>


## setupFiles
- Diese Option ermöglicht es Ihnen, eine Liste von Modulen anzugeben, die vor dem Starten Ihrer Tests ausgeführt werden sollen. Diese Dateien werden einmalig vor dem Laden von Jest selbst ausgeführt. Sie eignen sich gut für Setup-Aufgaben, die nicht von Jest abhängen.
```javascript
setupFiles: ['<rootDir>/test/setup-tests.ts']
```

- setup-tests.ts
```javascript
import * as dotenv from 'dotenv';
dotenv.config({ path: './config.env.test' });
```

<br><br>
<br><br>


## setupFiles
- setupFilesAfterEnv: Im Gegensatz dazu führt Jest diese Dateien nach dem Einrichten der Testumgebung (beforeEach, afterEach, etc.) und vor dem Ausführen der Tests aus. Dies ist nützlich, wenn Sie spezifische Setup-Aufgaben ausführen müssen, die Jest-Konstrukte wie describe und it verwenden.





















<br><br>
<br><br>
 _____________________________________________________
 _____________________________________________________
<br><br>
<br><br>

# Expect (https://jestjs.io/docs/en/expect)
```bash
npm i expect --save-dev
```
```javascript
const expect = require('expect');
```

<br>
<br>

## .toBe
```javascript
// Use .toBe to compare primitive values or to check referential identity of object instances. It calls Object.is to compare values, which is even better for testing than === strict equality operator.
const add = (a, b) => a + b;
expect( add(2, 3) ).toBe(5);
expect( typeof add(2, 3) ).toBe('number');
```

<br>
<br>

## .toEqual (https://jestjs.io/docs/en/expect#toequalvalue)
```javascript
// Use .toEqual to compare recursively all properties of object instances (also known as "deep" equality). It calls Object.is to compare primitive values, which is even better for testing than === strict equality operator.
expect( {a: undefined, b: 2} ).toEqual( {b: 2} );
```

## .toStrictEqual (https://jestjs.io/docs/en/expect#tostrictequalvalue)
```javascript
// test that objects have the same types as well as structure. Check above .toEqual for compare difference
expect( {"test": 1} ).toStrictEqual( {"test": 1} );
```


<br>
<br>


## .objectContaining (https://jestjs.io/docs/en/expect#expectobjectcontainingobject)
```javascript
/*expect.objectContaining(object) matches any received object that recursively matches the expected properties. That is, the expected object is a subset of the received object. Therefore, it matches a received object which contains properties that are present in the expected object.

Instead of literal property values in the expected object, you can use matchers, expect.anything(), and so on.*/
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.any(Number),
    geo: expect.any(Array),
    isFetching: expect.any(Boolean)
}));
```


<br>
<br>

## .any (https://jestjs.io/docs/en/expect#expectanyconstructor)
```javascript
// expect.any(constructor) matches anything that was created with the given constructor. You can use it inside toEqual or toBeCalledWith instead of a literal value.
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.any(Number)
}));
```

## .anything (https://jestjs.io/docs/en/expect#expectanything)
```javascript
// expect.anything() matches anything but null or undefined. You can use it inside toEqual or toBeCalledWith instead of a literal value. For example, if you want to check that a mock function is called with a non-null argument:
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.anything()
}));
```


<br><br>



## .toBeTruthy (https://jestjs.io/docs/en/expect#tobetruthy)
```javascript
// Use .toBeTruthy when you don't care what a value is and you want to ensure a value is true in a boolean context. 
expect( location() ).toBeTruthy();
```

<br><br>



## .toMatch (https://jestjs.io/docs/en/expect#tomatchregexp--string)
```javascript
// Use .toMatch to check that a string matches a regular expression.
expect( getDate() ).toMatch(/\d\d\/\d\d\/\d\d\d\d/gmi);
```

<br><br>

## .include (https://www.chaijs.com/api/bdd/#method_include)
```javascript
expect('foobar').to.include('foo');

expect([1, 2, 3]).to.include(2);
```









<br><br>




## Operators
```javascript
// You can use operators to check for multiple conditions
expect(msg).toEqual( expect.objectContaining({date: expect.anything()}) &&
expect.objectContaining({msg: expect.anything()}) &&
expect.objectContaining({room: expect.anything()}) &&
expect.objectContaining({usertoken: expect.anything()}) );
```
