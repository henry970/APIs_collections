# APIs_collections
Run automation test 


# Introduction to API Testing and Postman
![image](https://github.com/user-attachments/assets/d635632b-bd53-4338-abbc-4a2e6c72c90a)


API (Application Programming Interface) allows different software systems to communicate. APIs expose certain functionalities or data from a system and enable others to use it, making it possible to interact with a web service without knowing how it’s built internally.

Postman is a popular tool for API development and testing. It provides an easy-to-use interface to send HTTP requests and view responses, making it essential for testing RESTful APIs. It supports various request methods, such as GET, POST, PUT, DELETE, and more.

**Key Concepts**
API Endpoints: URLs that define where a client application can access the API.

Example: https://api.example.com/users
HTTP Methods: The action you want to perform with an API request:

**GET:** Retrieve data from the server.
**POST:** Send data to the server to create a new resource.
**PUT:** Update an existing resource.
**DELETE:** Delete a resource from the server.
**Headers:** Metadata sent with an API request, such as Authorization tokens or content type (Content-Type: application/json).

Body: Data sent to the API, usually for POST or PUT requests. This could be in JSON, XML, or other formats.

Status Codes: The server's response code tells you the result of the request:

200 OK: Success.
201 Created: Resource successfully created.
400 Bad Request: The request was malformed.
401 Unauthorized: Authentication needed.
404 Not Found: Resource not found.
500 Internal Server Error: Something went wrong on the server.
How to Use Postman for API Testing
Install Postman: If you’re using Postman Web, you can access it directly at Postman Web, or download the desktop app.

Create a Request:

Open Postman and create a new request by clicking New > HTTP Request.
Choose the method (GET, POST, etc.) and enter the API endpoint URL.
Adding Parameters:

Some API requests require query parameters, e.g., https://reqres.in/api/users?page=2. You can add these in the Params tab.
Other APIs may require parameters in the body, such as JSON data. You can add this in the Body tab.
Setting Headers:

Click the Headers tab to add custom headers such as Authorization: Bearer <token> or Content-Type: application/json.
Sending Requests:

Click Send to execute the request. Postman will display the response (data, status code, time taken) below.
Example: GET Request
Let’s perform a basic GET request to retrieve a list of users.

Open Postman.
Choose GET as the method.
Enter this API endpoint: https://reqres.in/api/users?page=2.
Click Send.
View the response in the lower panel. You should see a list of users returned in JSON format with a 200 OK status.
Example: POST Request
Now, let’s try creating a new resource with a POST request.

Change the method to POST.
Use this API endpoint: https://reqres.in/api/login.
In the Body tab, select raw and choose JSON as the data format.
Enter the following JSON data in the body:
JSON


{
    "email": "eve.holt@reqres.in",
    "password": "Pistol@12"
}
Click Send.
You should get a 201 Created status code, meaning the post was successfully created.
Postman Collections
Collections in Postman allow you to group multiple API requests. This is useful for organizing requests related to the same project or API.

To create a collection, click New > Collection.
Add requests to the collection by selecting the collection name when saving a request.
You can also use collections to:
Run requests in sequence (great for automated API testing).

Share them with teammates.
Postman Environment Variables
Variables in Postman allow you to reuse values (e.g., URLs, tokens) across multiple requests.

Go to Environment settings and create an environment (e.g., Development, Production).
Define variables like base_url = (https://reqres.in) or auth_token = <token>.
Use the variables in requests like this: {{base_url}}/users.
This makes switching between environments easy, as you only need to update the environment variables.


# Creating a collection and Request on PostMan

Creating collections and requests in Postman is fundamental for organizing and managing your API tests. Below is a **step-by-step** guide on how to create a collection and add requests in Postman.

**Step 1:** Create a Collection
A collection in Postman is a group of requests that can be run together, organized, and shared.

**Open Postman:**

Launch the Postman application on your desktop or use the web version.
Click on Collections:

On the left-hand panel, select Collections.
Create a New Collection:

Click the "+" button next to Collections or use the New button at the top, then choose Collection from the options.
Name the Collection:

A pop-up window will appear. Give your collection a meaningful name (e.g., "Demo_test_Collection").
Save the Collection:

**Step 2:** Add a Request to the Collection
A request is used to send data to an API endpoint and receive a response.

Create a New Request:

Once you’ve created the collection, click the "Add a request" button within your collection or the "+" icon next to the Request tab at the top.
Set Request Type:

In the new request tab, choose the request type (GET, POST, PUT, DELETE, etc.) by clicking the dropdown to the left of the URL input field.
Enter the Request URL:

In the URL input field, type the API endpoint you want to call (e.g., https://reqres.in/user).
Add Request to Collection:

After configuring the request, click the Save button (disk icon), and you will be prompted to save the request to a collection.
Select your collection (e.g., "Demo API Collection") and give your request a name (e.g., "Get All Posts").
Click Save to Demo_test_Collection.

**Step 3:** Customize Request (Optional)
You can customize your request further by adding headers, parameters, body, and authentication.

Headers: Click the Headers tab to add any headers required for the request (e.g., Authorization token).

Params: Use the Params tab to add URL parameters (e.g., ?userId=1).

Body (for POST/PUT requests): Select the Body tab and choose the appropriate format (e.g., JSON, Form-data) to send data in the request body.


**Step 4:** Send the Request

Once the request is ready, click the Send button.
You will see the response at the bottom section of the Postman window, where it shows the status code, time taken, and size of the response.
The response body will be displayed in a readable format (JSON, XML, etc.).


**Step 5:** Add More Requests to the Collection

Repeat the steps to add additional requests (e.g., POST, PUT, DELETE) to the same collection by clicking the "+" icon next to the request tab or by clicking Add request in the collection sidebar.
Step 6: Organize and Run the Collection
You can organize requests into folders within a collection to group related requests.
You can run the entire collection using the Collection Runner by clicking on the collection, then selecting the Run button.

