# APInf platform API testing

## Practices

## Postman

### Postman configurations

### Use existing tests

Existing tests are in platform repository https://github.com/apinf/platform/tree/develop/tests/rest-api-tests. Each platform API has own set of tests in separate file. 

You can import tests to Postman or newman (CLI tool). Alternatively you can use Newman CLI tool. 

## Newman

[Newman is CLI interface to Postman](https://github.com/postmanlabs/newman). You can run Postman generated tests from commandline with this tool. For example, to run tests against Catalog REST API

```
newman run APIs_OK.postman_collection.json > catalog-test-results.txt
```

The above runs the tests and writes the report to 'catalog-test-results.txt' file. 

### Add new test
