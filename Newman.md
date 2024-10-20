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

![WhatsApp Image 2024-10-19 at 15 46 54_d69848ef](https://github.com/user-attachments/assets/db8a95c5-f335-4faf-a38e-8e6dbb39a83d)


Running Newman on GitHub (Using GitHub Actions)
GitHub Actions is an excellent tool for running automated tests, including Postman collections via Newman, in your CI/CD pipeline.

Step 1: Create GitHub Actions Workflow
Navigate to Your Repository:

Go to your GitHub repository and click on the Actions tab.
Create a New Workflow:

Click New Workflow.
Choose Set up a workflow yourself (or select an existing template).
Create the Workflow File: check the yml file:

**Step 2:** Add Postman Collection to the GitHub Repository
Export Collection:
Export the Postman collection and environment file from Postman (in JSON format).
Add Files to Your Repo:
Commit and push these JSON files (e.g., Demo_test.postman_collection.json) into your GitHub repository.

**use command**
git add .
git commit -m "command change"
git push

**Step 3:** Trigger the Workflow
You can trigger the workflow manually or push a commit to the main branch to automatically trigger the workflow.

**Step 4:**  View Reports
Once the GitHub Actions run completes, navigate to the Actions tab.
Open the latest workflow run.
Under the Artifacts section, you’ll find the uploaded HTML report (if you added reporting).
Download the report and open it in your browser.

# Summary
Running Newman Locally: You need to install Node.js and Newman on your machine, then run the collection using the newman run command.
Running Newman on GitHub: Set up a GitHub Actions workflow to automate running your Postman collections in your CI/CD pipeline.
