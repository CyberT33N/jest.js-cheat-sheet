# Jest.js Cheat Sheet
Jest.js Cheat Sheet with the most needed stuff..








# CLI
```
Options:
  -h, --help                        Show help                          [boolean]
      --version                     Show version number                [boolean]
      --all                         The opposite of `onlyChanged`. If
                                    `onlyChanged` is set by default, running
                                    jest with `--all` will force Jest to run all
                                    tests instead of running only tests related
                                    to changed files.                  [boolean]
      --automock                    Automock all files by default.     [boolean]
  -b, --bail                        Exit the test suite immediately after `n`
                                    number of failing tests.           [boolean]
      --cache                       Whether to use the transform cache. Disable
                                    the cache using --no-cache.        [boolean]
      --cacheDirectory              The directory where Jest should store its
                                    cached  dependency information.     [string]
      --changedFilesWithAncestor    Runs tests related to the current changes
                                    and the changes made in the last commit.
                                    Behaves similarly to `--onlyChanged`.
                                                                       [boolean]
      --changedSince                Runs tests related to the changes since the
                                    provided branch. If the current branch has
                                    diverged from the given branch, then only
                                    changes made locally will be tested. Behaves
                                    similarly to `--onlyChanged`.       [string]
      --ci                          Whether to run Jest in continuous
                                    integration (CI) mode. This option is on by
                                    default in most popular CI environments. It
                                    will prevent snapshots from being written
                                    unless explicitly requested.       [boolean]
      --clearCache                  Clears the configured Jest cache directory
                                    and then exits. Default directory can be
                                    found by calling jest --showConfig [boolean]
      --clearMocks                  Automatically clear mock calls, instances,
                                    contexts and results before every test.
                                    Equivalent to calling jest.clearAllMocks()
                                    before each test.                  [boolean]
      --collectCoverage             Alias for --coverage.              [boolean]
      --collectCoverageFrom         A glob pattern relative to <rootDir>
                                    matching the files that coverage info needs
                                    to be collected from.               [string]
      --color                       Forces test results output color
                                    highlighting (even if stdout is not a TTY).
                                    Set to false if you would like to have no
                                    colors.                            [boolean]
      --colors                      Alias for `--color`.               [boolean]
  -c, --config                      The path to a jest config file specifying
                                    how to find and execute tests. If no rootDir
                                    is set in the config, the directory
                                    containing the config file is assumed to be
                                    the rootDir for the project. This can also
                                    be a JSON encoded value which Jest will use
                                    as configuration.                   [string]
      --coverage                    Indicates that test coverage information
                                    should be collected and reported in the
                                    output.                            [boolean]
      --coverageDirectory           The directory where Jest should output its
                                    coverage files.                     [string]
      --coveragePathIgnorePatterns  An array of regexp pattern strings that are
                                    matched against all file paths before
                                    executing the test. If the file path matches
                                    any of the patterns, coverage information
                                    will be skipped.                     [array]
      --coverageProvider            Select between Babel and V8 to collect
                                    coverage            [choices: "babel", "v8"]
      --coverageReporters           A list of reporter names that Jest uses when
                                    writing coverage reports. Any istanbul
                                    reporter can be used.                [array]
      --coverageThreshold           A JSON string with which will be used to
                                    configure minimum threshold enforcement for
                                    coverage results                    [string]
      --debug                       Print debugging info about your jest config.
                                                                       [boolean]
      --detectLeaks                 **EXPERIMENTAL**: Detect memory leaks in
                                    tests. After executing a test, it will try
                                    to garbage collect the global object used,
                                    and fail if it was leaked          [boolean]
      --detectOpenHandles           Print out remaining open handles preventing
                                    Jest from exiting at the end of a test run.
                                    Implies `runInBand`.               [boolean]
      --env                         The test environment used for all tests.
                                    This can point to any file or node module.
                                    Examples: `jsdom`, `node` or
                                    `path/to/my-environment.js`         [string]
      --errorOnDeprecated           Make calling deprecated APIs throw helpful
                                    error messages.                    [boolean]
  -e, --expand                      Use this flag to show full diffs instead of
                                    a patch.                           [boolean]
      --filter                      Path to a module exporting a filtering
                                    function. This method receives a list of
                                    tests which can be manipulated to exclude
                                    tests from running. Especially useful when
                                    used in conjunction with a testing
                                    infrastructure to filter known broken tests.
                                                                        [string]
      --findRelatedTests            Find related tests for a list of source
                                    files that were passed in as arguments.
                                    Useful for pre-commit hook integration to
                                    run the minimal amount of tests necessary.
                                                                       [boolean]
      --forceExit                   Force Jest to exit after all tests have
                                    completed running. This is useful when
                                    resources set up by test code cannot be
                                    adequately cleaned up.             [boolean]
      --globalSetup                 The path to a module that runs before All
                                    Tests.                              [string]
      --globalTeardown              The path to a module that runs after All
                                    Tests.                              [string]
      --globals                     A JSON string with map of global variables
                                    that need to be available in all test
                                    environments.                       [string]
      --haste                       A JSON string with map of variables for the
                                    haste module system                 [string]
      --ignoreProjects              Ignore the tests of the specified projects.
                                    Jest uses the attribute `displayName` in the
                                    configuration to identify each project.
                                                                         [array]
      --init                        Generate a basic configuration file[boolean]
      --injectGlobals               Should Jest inject global variables or not
                                                                       [boolean]
      --json                        Prints the test results in JSON. This mode
                                    will send all other test output and user
                                    messages to stderr.                [boolean]
      --lastCommit                  Run all tests affected by file changes in
                                    the last commit made. Behaves similarly to
                                    `--onlyChanged`.                   [boolean]
      --listTests                   Lists all tests Jest will run given the
                                    arguments and exits. Most useful in a CI
                                    system together with `--findRelatedTests` to
                                    determine the tests Jest will run based on
                                    specific files                     [boolean]
      --logHeapUsage                Logs the heap usage after every test. Useful
                                    to debug memory leaks. Use together with
                                    `--runInBand` and `--expose-gc` in node.
                                                                       [boolean]
      --maxConcurrency              Specifies the maximum number of tests that
                                    are allowed to run concurrently. This only
                                    affects tests using `test.concurrent`.
                                                                        [number]
  -w, --maxWorkers                  Specifies the maximum number of workers the
                                    worker-pool will spawn for running tests.
                                    This defaults to the number of the cores
                                    available on your machine. (its usually best
                                    not to override this default)       [string]
      --moduleDirectories           An array of directory names to be searched
                                    recursively up from the requiring module's
                                    location.                            [array]
      --moduleFileExtensions        An array of file extensions your modules
                                    use. If you require modules without
                                    specifying a file extension, these are the
                                    extensions Jest will look for.       [array]
      --moduleNameMapper            A JSON string with a map from regular
                                    expressions to module names or to arrays of
                                    module names that allow to stub out
                                    resources, like images or styles with a
                                    single module                       [string]
      --modulePathIgnorePatterns    An array of regexp pattern strings that are
                                    matched against all module paths before
                                    those paths are to be considered "visible"
                                    to the module loader.                [array]
      --modulePaths                 An alternative API to setting the NODE_PATH
                                    env variable, modulePaths is an array of
                                    absolute paths to additional locations to
                                    search when resolving modules.       [array]
      --noStackTrace                Disables stack trace in test results output
                                                                       [boolean]
      --notify                      Activates notifications for test results.
                                                                       [boolean]
      --notifyMode                  Specifies when notifications will appear for
                                    test results.                       [string]
  -o, --onlyChanged                 Attempts to identify which tests to run
                                    based on which files have changed in the
                                    current repository. Only works if you're
                                    running tests in a git or hg repository at
                                    the moment.                        [boolean]
  -f, --onlyFailures                Run tests that failed in the previous
                                    execution.                         [boolean]
      --openHandlesTimeout          Print a warning about probable open handles
                                    if Jest does not exit cleanly after this
                                    number of milliseconds. `0` to disable.
                                                                        [number]
      --outputFile                  Write test results to a file when the --json
                                    option is also specified.           [string]
      --passWithNoTests             Will not fail if no tests are found (for
                                    example while using `--testPathPattern`.)
                                                                       [boolean]
      --preset                      A preset that is used as a base for Jest's
                                    configuration.                      [string]
      --prettierPath                The path to the "prettier" module used for
                                    inline snapshots.                   [string]
      --projects                    A list of projects that use Jest to run all
                                    tests of all projects in a single instance
                                    of Jest.                             [array]
      --randomize                   Shuffle the order of the tests within a
                                    file. In order to choose the seed refer to
                                    the `--seed` CLI option.           [boolean]
      --reporters                   A list of custom reporters for the test
                                    suite.                               [array]
      --resetMocks                  Automatically reset mock state before every
                                    test. Equivalent to calling
                                    jest.resetAllMocks() before each test.
                                                                       [boolean]
      --resetModules                If enabled, the module registry for every
                                    test file will be reset before running each
                                    individual test.                   [boolean]
      --resolver                    A JSON string which allows the use of a
                                    custom resolver.                    [string]
      --restoreMocks                Automatically restore mock state and
                                    implementation before every test. Equivalent
                                    to calling jest.restoreAllMocks() before
                                    each test.                         [boolean]
      --rootDir                     The root directory that Jest should scan for
                                    tests and modules within.           [string]
      --roots                       A list of paths to directories that Jest
                                    should use to search for files in.   [array]
  -i, --runInBand                   Run all tests serially in the current
                                    process (rather than creating a worker pool
                                    of child processes that run tests). This is
                                    sometimes useful for debugging, but such use
                                    cases are pretty rare.             [boolean]
      --runTestsByPath              Used when provided patterns are exact file
                                    paths. This avoids converting them into a
                                    regular expression and matching it against
                                    every single file.                 [boolean]
      --runner                      Allows to use a custom runner instead of
                                    Jest's default test runner.         [string]
      --seed                        Sets a seed value that can be retrieved in a
                                    tests file via `jest.getSeed()`. If this
                                    option is not specified Jest will randomly
                                    generate the value. The seed value must be
                                    between `-0x80000000` and `0x7fffffff`
                                    inclusive.                          [number]
      --selectProjects              Run the tests of the specified projects.
                                    Jest uses the attribute `displayName` in the
                                    configuration to identify each project.
                                                                         [array]
      --setupFiles                  A list of paths to modules that run some
                                    code to configure or set up the testing
                                    environment before each test.        [array]
      --setupFilesAfterEnv          A list of paths to modules that run some
                                    code to configure or set up the testing
                                    framework before each test           [array]
      --shard                       Shard tests and execute only the selected
                                    shard, specify in the form "current/all".
                                    1-based, for example "3/5".         [string]
      --showConfig                  Print your jest config and then exits.
                                                                       [boolean]
      --showSeed                    Prints the seed value in the test report
                                    summary. See `--seed` for how to set this
                                    value                              [boolean]
      --silent                      Prevent tests from printing messages through
                                    the console.                       [boolean]
      --skipFilter                  Disables the filter provided by --filter.
                                    Useful for CI jobs, or local enforcement
                                    when fixing tests.                 [boolean]
      --snapshotSerializers         A list of paths to snapshot serializer
                                    modules Jest should use for snapshot
                                    testing.                             [array]
      --testEnvironment             Alias for --env                     [string]
      --testEnvironmentOptions      A JSON string with options that will be
                                    passed to the `testEnvironment`. The
                                    relevant options depend on the environment.
                                                                        [string]
      --testFailureExitCode         Exit code of `jest` command if the test run
                                    failed                              [string]
      --testLocationInResults       Add `location` information to the test
                                    results                            [boolean]
      --testMatch                   The glob patterns Jest uses to detect test
                                    files.                               [array]
  -t, --testNamePattern             Run only tests with a name that matches the
                                    regex pattern.                      [string]
      --testPathIgnorePatterns      An array of regexp pattern strings that are
                                    matched against all test paths before
                                    executing the test. If the test path matches
                                    any of the patterns, it will be skipped.
                                                                         [array]
      --testPathPattern             A regexp pattern string that is matched
                                    against all tests paths before executing the
                                    test.                                [array]
      --testRegex                   A string or array of string regexp patterns
                                    that Jest uses to detect test files. [array]
      --testResultsProcessor        Allows the use of a custom results
                                    processor. This processor must be a node
                                    module that exports a function expecting as
                                    the first argument the result object.
                                                                        [string]
      --testRunner                  Allows to specify a custom test runner. The
                                    default is `jest-circus/runner`. A path to a
                                    custom test runner can be provided:
                                    `<rootDir>/path/to/testRunner.js`.  [string]
      --testSequencer               Allows to specify a custom test sequencer.
                                    The default is `@jest/test-sequencer`. A
                                    path to a custom test sequencer can be
                                    provided:
                                    `<rootDir>/path/to/testSequencer.js`[string]
      --testTimeout                 This option sets the default timeouts of
                                    test cases.                         [number]
      --transform                   A JSON string which maps from regular
                                    expressions to paths to transformers.
                                                                        [string]
      --transformIgnorePatterns     An array of regexp pattern strings that are
                                    matched against all source file paths before
                                    transformation.                      [array]
      --unmockedModulePathPatterns  An array of regexp pattern strings that are
                                    matched against all modules before the
                                    module loader will automatically return a
                                    mock for them.                       [array]
  -u, --updateSnapshot              Use this flag to re-record snapshots. Can be
                                    used together with a test suite pattern or
                                    with `--testNamePattern` to re-record
                                    snapshot for test matching the pattern
                                                                       [boolean]
      --useStderr                   Divert all output to stderr.       [boolean]
      --verbose                     Display individual test results with the
                                    test suite hierarchy.              [boolean]
      --watch                       Watch files for changes and rerun tests
                                    related to changed files. If you want to
                                    re-run all tests when a file has changed,
                                    use the `--watchAll` option.       [boolean]
      --watchAll                    Watch files for changes and rerun all tests.
                                    If you want to re-run only the tests related
                                    to the changed files, use the `--watch`
                                    option.                            [boolean]
      --watchPathIgnorePatterns     An array of regexp pattern strings that are
                                    matched against all paths before trigger
                                    test re-run in watch mode. If the test path
                                    matches any of the patterns, it will be
                                    skipped.                             [array]
      --watchman                    Whether to use watchman for file crawling.
                                    Disable using --no-watchman.       [boolean]
      --workerThreads               Whether to use worker threads for
                                    parallelization. Child processes are used by
                                    default.                           [boolean]
```






<br><br>
<br><br>
 _____________________________________________________
 _____________________________________________________
<br><br>
<br><br>

# package.json
- console.log() is for default not be showed in your stdout. Make sure to use the --verbose Flag
- In order to archieve full coverage with integration and unit tests we use the setup below. When ever you want to make sure that your coverage is fully check run `npm run test`
  - When you only run `npm run unit-test` your coverage is maybe not fully covered 
```javascript
"scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint",
    "test-only": "bash test-only.sh",
    "test": "jest --coverage",
    "test:watch": "jest --watch",
    "test:integration": "jest --coverage --config jest.integration.config.ts",
    "test:unit": "jest --coverage --config jest.unit.config.ts"
}
```

## Run tests sequentially
- `jest --runInBand`





<br><br>
<br><br>

## test-only.sh:
- .only is not working inside of jest.. So we need a workaround
```
grep --exclude-dir=node_modules -rl . -e 'test.only\|it.only\|describe.only' --null | tr '\n' ' ' | xargs -0 npx jest | grep . || npx jest
```





<br><br>
<br><br>

# jest.integration.config.ts
```typescript
/**
 * For a detailed explanation regarding each configuration property, visit:
 * https://jestjs.io/docs/configuration
 */

import type { Config } from 'jest'
import nextJest from 'next/jest.js'

import baseConfig from './jest.config'

const createJestConfig = nextJest({
    // Provide the path to your Next.js app to load next.config.js and .env files in your test environment
    dir: './'
})

const config: Config = {
    ...baseConfig,

    // An array of glob patterns indicating a set of files for which coverage information should be collected
    collectCoverageFrom: [
        'app/api/**/route.ts'
        // '!app/api/**/*.d.ts'
    ]
}

// createJestConfig is exported this way to ensure that next/jest can load the Next.js config which is async
export default createJestConfig(config)
```





<br><br>
<br><br>

# jest.unit.config.ts
```typescript
/**
 * For a detailed explanation regarding each configuration property, visit:
 * https://jestjs.io/docs/configuration
 */

import type { Config } from 'jest'
import nextJest from 'next/jest.js'

import baseConfig from './jest.config'

const createJestConfig = nextJest({
    // Provide the path to your Next.js app to load next.config.js and .env files in your test environment
    dir: './'
})

const config: Config = {
    ...baseConfig,

    // An array of glob patterns indicating a set of files for which coverage information should be collected
    collectCoverageFrom: [
        'app/**/*.service.ts',
        'utils/**/*.ts',
        '!utils/**/*.d.ts'
    ]
}

// createJestConfig is exported this way to ensure that next/jest can load the Next.js config which is async
export default createJestConfig(config)
```




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
    // An array of glob patterns indicating a set of files for which coverage information should be collected
    
    // Timeout for all tests
    testTimeout: 300000,

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
- **Not needed in Next.js**
```bash
npm i expect --save-dev
```
```javascript
const expect = require('expect');
```











<br><br>
<br><br>
 _____________________________________________________
 _____________________________________________________
<br><br>
<br><br>


## Error

<br><br>

## toThrow

<br><br>

### Sync
```javascript
test('throws on octopus', () => {
  expect(() => {
    drinkFlavor('octopus');
  }).toThrow();
});
```

<br><br>


### Async
```
await expect(axiosRequestWrapper(config)).rejects.toThrow('Any crazy error..')
```













<br><br>
<br><br>
 _____________________________________________________
 _____________________________________________________
<br><br>
<br><br>


## .toBe
```javascript
// Use .toBe to compare primitive values or to check referential identity of object instances. It calls Object.is to compare values, which is even better for testing than === strict equality operator.
const add = (a, b) => a + b;
expect( add(2, 3) ).toBe(5);
expect( typeof add(2, 3) ).toBe('number');
```







<br><br>
<br><br>

## .toBeInstanceOf
- https://jestjs.io/docs/expect#tobeinstanceofclass
```javascript
class A {}

expect(new A()).toBeInstanceOf(A);
expect(() => {}).toBeInstanceOf(Function);
expect(new A()).toBeInstanceOf(Function); // throws
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
