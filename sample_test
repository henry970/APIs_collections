Writing tests in Postman allows you to automate checking for certain conditions or validations after an API response is received. Postman uses **JavaScript** for test scripting, and you can write tests that will be executed after a request is made.

### **How to Write Tests in Postman**

Here’s a step-by-step guide on how to write tests in Postman:



### **Step 1: Create a Request**

1. **Open Postman** and create a new request by clicking the **+** button.
2. Set the request type (e.g., **GET**, **POST**) and enter the request URL.
3. Set any required **Headers**, **Params**, or **Body** (for POST/PUT requests).


### **Step 2: Open the Tests Tab**

1. In the request window, click on the **Tests** tab (next to the **Body** tab).
2. This is where you will write the JavaScript code to validate the response.


### **Step 3: Write Test Scripts**

In the **Tests** tab, Postman provides predefined snippets to help you get started, but you can write your own custom test scripts as well.

Here are common examples of tests you can write:

#### **1. Check Status Code**
This ensures the response status code is correct (e.g., 200 for success).

  javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});


#### **2. Validate Response Time**
Ensure the response time is within a specified limit.

  javascript
pm.test("Response time is less than 200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});


#### **3. Validate JSON Response Body**
Check if the response body contains a specific value.

 javascript
pm.test("Response contains specific field", function () {
    const jsonData = pm.response.json();  // Parse the response body
    pm.expect(jsonData.name).to.eql("morpheus");  // Validate the 'name' field
});


#### **4. Check if Response Body Contains a Property**
Verify if a property exists in the response.

 javascript
pm.test("Response has a job property", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property('job');
});


#### **5. Validate Header Information**
Ensure a specific header is present in the response.

 javascript
pm.test("Content-Type is application/json", function () {
    pm.response.to.have.header("Content-Type", "application/json");
});


#### **6. Validate Array in Response**
Check if a response contains an array and validate the length.

  javascript
pm.test("Response contains an array with more than 5 items", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.be.an('array');
    pm.expect(jsonData.length).to.be.above(5);
});


### **Step 4: Run the Request and View Test Results**

1. After writing your tests, click **Send** to execute the API request.
2. Once the request is complete, scroll down to the **Tests** tab in the response area to see the results of your tests.
   - Tests that pass will have a green checkmark, and tests that fail will have a red cross.


### **Step 5: Running Collections with Tests**

You can run a collection of requests (including tests) using the **Collection Runner** or **Newman** for automation.

#### **Using Collection Runner**:
1. Go to the **Collections** tab in Postman.
2. Click **Run** on the collection you want to execute.
3. Postman will execute all requests in the collection and run the tests attached to each request.

#### **Using Newman** (Command Line Tool):
You can also automate tests and generate reports with **Newman** (Postman's command-line tool), which will run your collections and execute the tests you wrote.



### **Useful Postman Test Assertions**

Here are a few common assertions you can use in Postman tests:

- **Check for status code**: `pm.response.to.have.status(200);`
- **Check response time**: `pm.expect(pm.response.responseTime).to.be.below(300);`
- **Check JSON field value**: `pm.expect(jsonData.name).to.eql("value");`
- **Check if a property exists**: `pm.expect(jsonData).to.have.property('key');`
- **Check header exists**: `pm.response.to.have.header('Content-Type');`


### **Advanced Postman Tests**

- **Chaining Requests**: You can extract data from one request and use it in another request. For example, you can use an authentication token from one API call as a header in another call.
- **Environment Variables**: You can use environment variables in your test scripts to manage data and configurations.

pm.environment.set("token", jsonData.token);  // Save token for the next request


### **Conclusion**

Writing tests in Postman is a simple yet powerful way to validate your API responses and ensure your services are working correctly. By using tests in Postman, you can automate error checking and create robust test suites for your API workflows.

