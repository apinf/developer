# APInf platform API testing

## Practices

With testing tool Postman there are [done sets of automated tests](https://github.com/apinf/platform/tree/develop/tests/rest-api-tests) for APInf Platform REST APIs.

The master collection contains all subcollections
* test sets of REST APIs for APIs, Organizations and Users
  * each test set for REST API contains
    * collection of tests for successful requests (2xx HTTP code expected)
    * tests for each endpoint in REST API in question, covering all unsuccessful (3xx/4xx/5xx expected) cases


## Postman - GUI tool

### Postman configurations

To run API tests succesfully, you need to set some global and environment variables:
- Add used URL to global variables
  -  Postman > environment options > Manage environments > Globals
     - Add parameter: url = http://nightly.apinf.io/rest/v1
     - Save
- Add username and password to an environment.
  - Postman > environment options > Manage environments
    - select or create an environment
      - add parameter username = <existing username>
      - add parameter password = <password related to username>
      - Update


### Use existing tests

Existing tests are in platform repository, [rest-api-tests](https://github.com/apinf/platform/tree/develop/tests/rest-api-tests). Each platform API has own set of tests in separate file. 

- Open Postman Runner
- Select the collection of tests you want to run
- Select the environment where you stored username and password
- Click big blue button that says [Run <collection_name>]
- Verify, that tests are run with expected results


Alternatively you can use Newman CLI tool. 

## Newman - CLI tool

[Newman is CLI interface to Postman](https://github.com/postmanlabs/newman). You can run Postman generated tests from commandline with this tool. Here's a few examples. 

**Start with cloning the platform repository and go to tests folder**

```
git clone https://github.com/apinf/platform
cd platform/tests/rest-api-tests/
```

**Runs given test collection and writes the report to 'catalog-test-results.txt' file.**

```
newman run APIs_OK.postman_collection.json > catalog-test-results.txt
```

**Runs given test collection and uses environment defined in separate file called 'environment.json'. Prints results to screen.**

```
newman run APIs_OK.postman_collection.json -e environment.json
```



### Add new test with Postman (TODO: clarify this, leave no space for error)

- Clone the platform repository if you have not done so already

```
git clone https://github.com/apinf/platform
cd platform/tests/rest-api-tests/
```

- Create branch for the new test

```
git checkout -b [name_of_your_new_branch]
```

- Load existing tests to Postman. 
- Create new test
- Export collection and replace old test collection with new one.
- Run the tests locally to vefify that it behaves as expected. Either in Postman Runner or newman
- Commit to branch you created and push to github.

```
git add [name_of_your_new_branch]
git commit -m "Added new test X"
git push origin [name_of_your_new_branch]
```
- Make a pull request. 
