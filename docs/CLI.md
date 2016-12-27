---
id: cli
title: Jest CLI Options
layout: docs
category: API Reference
permalink: docs/cli.html
---

The `jest` command line tool has a number of useful options, although you might never need any of them. You can run `jest --help` to view the options available. This document will also provide a brief overview.

If you run Jest via `npm test`, you can still use the command line arguments by inserting a `--` between `npm test` and the Jest arguments. So instead of:

```bash
jest -u -t="ColorPicker"
```

you could use:

```bash
npm test -- -u -t="ColorPicker"
```

### `jest <regexForTestFiles>`

When you run `jest` with an argument, that argument is treated as a regular expression to match against files in your project. It is possible to run test suites by providing a pattern. Only the files that the pattern matches will be picked up and executed.

### `jest --bail`

Alias: `-b`. Exit the test suite immediately upon the first failing test.

### `jest --cache`

Whether to use the transform cache. Defaults to true. Disable the cache using `--no-cache`.

### `jest --collectCoverageFrom=<glob>`

Relative to the root directory, glob pattern matching the files that coverage info needs to be collected from.

### `jest --colors`

Forces test results output highlighting even if stdout is not a TTY.

### `jest --config=<path>`

Alias: `-c`. The path to a jest config file specifying how to find and execute tests. If no `rootDir` is set in the config, the current directory is assumed to be the rootDir for the project. This can also be a JSON-encoded value which Jest will use as configuration.

### `jest --coverage`

Indicates that test coverage information should be collected and reported in the output.

### `jest --debug`

Print debugging info about your jest config.

### `jest --env=<environment>`

The test environment used for all tests. This can point to any file or node module. Examples: `jsdom`, `node` or `path/to/my-environment.js`.

### `jest --expand`

Alias: `-e`. Use this flag to show full diffs instead of a patch.

### `jest --findRelatedTests=<listOfSourceFiles>`

Find the tests that cover a list of source files that were passed in as arguments. Useful for pre-commit hook integration to run the minimal amount of tests necessary.

### `jest --forceExit`

Force Jest to exit after all tests have completed running. This is useful when resources set up by test code cannot be adequately cleaned up.

### `jest --help`

Show some helpful information, similar to this page.

### `jest --json`

Prints the test results in JSON. This mode will send all other test output and user messages to stderr.

### `jest --jsonOutputFile=<filename>`

Write test results to a file when the `--json` option is also specified.

### `jest --lastCommit`

Will run all tests affected by file changes in the last commit made.

### `jest --logHeapUsage`

Logs the heap usage after every test. Useful to debug memory leaks. Use together with `--runInBand` and `--expose-gc` in node.

### `jest --maxWorkers=<num>`

Alias: `-w`. Specifies the maximum number of workers the worker-pool will spawn for running tests. This defaults to the number of the cores available on your machine. Overriding this is rarely a good idea.

### `jest --noStackTrace`

Disables stack trace in test results output.

### `jest --notify`

Activates notifications for test results. Good for when you don't want your consciousness to be able to focus on anything except JavaScript testing.

### `jest --onlyChanged`

Alias: `-o`. Attempts to identify which tests to run based on which files have changed in the current repository. Only works if you're running tests in a git repository at the moment.

### `jest --runInBand`

Alias: `-i`. Run all tests serially in the current process, rather than creating a worker pool of child processes that run tests. This is sometimes useful for debugging, but generally discouraged.

### `jest --setupTestFrameworkScriptFile=<file>`

The path to a module that runs some code to configure or set up the testing framework before each test.

### `jest --silent`

Prevent tests from printing messages through the console.

### `jest --testNamePattern=<regex>`

Alias: `-t`. Run only tests with a name that matches the regex.

### `jest --testPathPattern=<regex>`

A regexp pattern string that is matched against all tests paths before executing the test.

### `jest --testRunner=<path>`

Lets you specify a custom test runner.

### `jest --updateSnapshot`

Alias: `-u`. Use this flag to re-record every snapshot that fails during this test run. Can be used together with a test suite pattern or with `--testNamePattern` to re-record snapshots.

### `jest --useStderr`

Divert all output to stderr.

### `jest --verbose`

Display individual test results with the test suite hierarchy.

### `jest --version`

Alias: `-v`. Print the version and exit.

### `jest --watch`

Watch files for changes and rerun tests related to changed files. If you want to re-run all tests when a file has changed, use the `--watchAll` option instead.

### `jest --watchAll`

Watch files for changes and rerun all tests when something changes. If you want to re-run only the tests that depend on the changed files, use the `--watch` option.

### `jest --watchman`

Whether to use watchman for file crawling. Defaults to true. Disable using `--no-watchman`.