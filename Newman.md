# Running Newman Locally
**Step 1:** Install Node.js
To use Newman, you must have Node.js installed on your local machine.

Download and install Node.js from https://nodejs.org.
# Verify installation by running:

**command**
node -v
npm -v
**Step 2:** Install Newman
Once Node.js is installed, you can install Newman globally using npm:

**Command:**
npm install -g newman
**Step 3:** Run a Postman Collection
To run a Postman collection using Newman locally:

**Export Postman Collection:**

In Postman, go to your collection.
Click the three dots next to the collection name and choose Export.
Save the collection as a .json file on your computer.
**Run the Collection:**

Open your terminal or command prompt, navigate to the folder where your collection is saved, and run the following command:

**Command:**
newman run Dome_test.postman_collection.json
Example:

**Command:**
newman run ./Demo_test.postman_collection.json
Optional: Run with Environment Variables: If you have environment variables for your API requests, you can also export and include an environment file:

**Command:**
newman run Dome_test.postman_collection.json -e 
Optional: Generate Reports: You can generate different types of reports, such as HTML:

**Command:**
newman run Dome_test.postman_collection.json -r htmlextra --reporter-htmlextra-export ./report.ht
