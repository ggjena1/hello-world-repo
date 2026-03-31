# hello-world-repo

# Questions Related to the hello-world.yml
Create a new repository on your own GitHub account and execute a Github Action workflow with the following details:
Repository Name - hello-world-repo
Work on the following branch - main
Workflow File Name - hello-world.yml
Workflow Name - Hello World
Trigger Workflow on push events
Workflow should have a Job named - hello-job
a. Run Job on - ubuntu-latest runner
b. Job has 1 step named - Echo text
c. Run a command - echo "Hello, world!"
Trigger Workflow on push event should execute successfully
# Answers: 
To create and configure a GitHub Actions workflow for your hello-world-repo with the specified requirements, follow these step-by-step guidelines:

Create the Repository:

Navigate to GitHub.
Sign in to your account.
Click on the "New" button to create a new repository.
Enter hello-world-repo as the Repository Name.
Choose the repository visibility (Public or Private).
Click "Create repository".
Switch to the Main Branch:

Clone the repository to your local machine using git clone.
Ensure you are on the main branch, which is usually the default branch.
Create the Workflow File:

In your local repository, navigate to the .github/workflows directory. Create it if it doesn't exist.
Inside the .github/workflows directory, create a new file named hello-world.yml.
Configure the Workflow:

Open hello-world.yml in a text editor.
Add the following content to the file:
name: Hello World
'on': push
jobs:
  hello-job:
    runs-on: ubuntu-latest
    steps:
      - name: Echo text
        run: 'echo "Hello, world!"'
This configuration sets up the workflow named Hello World that triggers on push events. It includes a job hello-job that runs on an ubuntu-latest runner and executes the command echo "Hello, world!".
Commit and Push the Workflow File:

Use git add . to stage your changes.
Commit the changes with a message, e.g., git commit -m "Add hello world workflow".
Push the changes to the main branch using git push.
Verify the Workflow:

Go back to your GitHub repository page.
Click on the "Actions" tab to view the workflow runs.
The Hello World workflow should execute automatically as a result of the push.
Verify that the workflow completes successfully. You should see a green checkmark indicating a successful execution.
By following these steps, you will have successfully created and executed a GitHub Actions workflow in your hello-world-repo that responds to push events, runs a job on an ubuntu-latest runner, and executes the command echo "Hello, world!".