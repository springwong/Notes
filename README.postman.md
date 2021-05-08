#Postman

Advantages:
With scripts, even non-technical member could work with  API calls with instructions.\
With teams, a consistent structure API clients can be created.\
Mass test is possbile.
Logic avaiable to run flow.

## Usage

### Basic
#### Request
1. Params
2. Authorization, supported Basic, Bearer, etc
3. Headers
4. Body

#### Response
1. Body
2. Cookie
3. Header

#### Code Snippets
1. Curl

### Environment Variables
#### Types
1. Local (in pre / post script)
2. Collection
3. Environment
4. Global
5. Iteration data (Runner)

#### How to use
1. {{key}} in request parameter
2. pm.environment.set
3. pm.variables.get

#### Storage
Environment and global variables is stored in local only

### Pre and Post Scripts
1. Get / Set variables
```
pm.environment.set("test", "1234);
pm.variables.get('key')
```
2. Further post-processing on data response
```
// plain text
const text = pm.response.text()
// json response
var jsonData = JSON.parse(responseBody);
```
3. Unit Test on API response
```
pm.test("Name", function () { 
    pm.expect(input, "fetch csrf fail").to.not.eq("value"); 
});
```
4. Visualizer
```
pm.visualizer.set(htmlTemplate, dataSet);
```
5. Logging

### Import
1. Postman Collection
2. Curl
3. Swagger

### Runner
1. Data Set with .csv or .json
2. Capture request / response for each calls
3. Run a collection with specific ordering
4. Save response variables to environment variables
5. Unit test with imported csv.

### Teams (Paid)
1. Share collection between teammates
2. Source control with fork, merge, pull request
3. Role Management

### Settings
1. SSL certification verification is not a must in some cases
2. Automatically follow redirect can be turned off in some cases.

### Possible Flows
A list page to detail page flow
List API call > post script to save detail id to environment variable > Detail API call with saved variable