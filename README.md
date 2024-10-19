# APIs_collections
Run automation test 


# Introduction to API Testing and Postman

API (Application Programming Interface) allows different software systems to communicate. APIs expose certain functionalities or data from a system and enable others to use it, making it possible to interact with a web service without knowing how it’s built internally.

Postman is a popular tool for API development and testing. It provides an easy-to-use interface to send HTTP requests and view responses, making it essential for testing RESTful APIs. It supports various request methods, such as GET, POST, PUT, DELETE, and more.

Key Concepts
API Endpoints: URLs that define where a client application can access the API.

Example: https://api.example.com/users
HTTP Methods: The action you want to perform with an API request:

GET: Retrieve data from the server.
POST: Send data to the server to create a new resource.
PUT: Update an existing resource.
DELETE: Delete a resource from the server.
Headers: Metadata sent with an API request, such as Authorization tokens or content type (Content-Type: application/json).

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

Some API requests require query parameters, e.g., https://api.example.com/users?limit=10. You can add these in the Params tab.
Other APIs may require parameters in the body, such as JSON data. You can add this in the Body tab.
Setting Headers:

Click the Headers tab to add custom headers such as Authorization: Bearer <token> or Content-Type: application/json.
Sending Requests:

Click Send to execute the request. Postman will display the response (data, status code, time taken) below.
Example: GET Request
Let’s perform a basic GET request to retrieve a list of users.

Open Postman.
Choose GET as the method.
Enter this API endpoint: https://jsonplaceholder.typicode.com/users.
Click Send.
View the response in the lower panel. You should see a list of users returned in JSON format with a 200 OK status.
Example: POST Request
Now, let’s try creating a new resource with a POST request.

Change the method to POST.
Use this API endpoint: https://jsonplaceholder.typicode.com/posts.
In the Body tab, select raw and choose JSON as the data format.
Enter the following JSON data in the body:
json
Copy code
{
    "title": "My First Post",
    "body": "This is the content of my post.",
    "userId": 1
}
Click Send.
You should get a 201 Created status code, meaning the post was successfully created.
Postman Collections
Collections in Postman allow you to group multiple API requests together. This is useful for organizing requests related to the same project or API.

To create a collection, click New > Collection.
Add requests to the collection by selecting the collection name when saving a request.
You can also use collections to:
Run requests in sequence (great for automated API testing).
Share them with teammates.
Postman Environment Variables
Variables in Postman allow you to reuse values (e.g., URLs, tokens) across multiple requests.

Go to Environment settings and create an environment (e.g., Development, Production).
Define variables like base_url = https://api.example.com or auth_token = <token>.
Use the variables in requests like this: {{base_url}}/users.
This makes switching between environments easy, as you only need to update the environment variables.
