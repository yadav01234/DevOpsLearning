# How to Create a Jenkins Job When PR has been Created

## Step 1: Set up a Webhook
1. Log in to your version control system (e.g., GitHub, Bitbucket) and navigate to your repository.
2. Look for the repository's settings or options related to webhooks.
3. Create a new webhook and provide the necessary information.
   - **Payload URL:** Enter the URL of your Jenkins server. This is where the webhook events will be sent.
   - **Content Type:** Select the appropriate content type for the webhook payload.
   - **Events or Triggers:** Choose the event that should trigger the webhook. In this case, select the option related to pull request creation.
   - Save or create the webhook.

## Step 2: Install the Necessary Plugins
1. Open your Jenkins server's dashboard.
2. Navigate to the "Manage Jenkins" section.
3. Select "Manage Plugins" or "Plugin Manager."
4. In the "Available" tab, search for and install the relevant plugin(s) for integrating with your version control system. For GitHub, you can search for "GitHub Integration" or "GitHub Pull Request Builder" plugins.
5. Restart Jenkins if prompted.

## Step 3: Create a Jenkins Job
1. Return to the Jenkins dashboard.
2. Click on "New Item" or "Create New Job" to create a new Jenkins job.
3. Enter a name for your job and select the appropriate job type (e.g., Freestyle project, Pipeline).
4. Click "OK" or "Create" to proceed to the job configuration page.

## Step 4: Configure Job Triggers
### For the "GitHub Integration" plugin:
1. Scroll down to the "Build Triggers" section.
2. Check the "GitHub Pull Request" trigger box.
3. Configure the trigger settings:
   - **Repository:** Enter the URL or name of your repository.
   - **Choose the branch to build:** Specify the branch you want to trigger the job on (e.g., "*/develop").
   - **Build on:** Select the event that should trigger the build (e.g., "Pull Request Created").
4. Adjust any other desired settings.
5. Save the job configuration.

### For the "GitHub Pull Request Builder" plugin:
1. Scroll down to the "Build Triggers" section.
2. Check the "GitHub Pull Request Builder" trigger box.
3. Configure the trigger settings:
   - **Build on pull request:** Select "Check this box if you want to build every pull request automatically."
   - **Branches to build:** Specify the branch you want to trigger the job on (e.g., "develop").
   - **Events:** Select the event that should trigger the build (e.g., "Pull Request Created").
4. Adjust any other desired settings.
5. Save the job configuration.

## Step 5: Define Build Steps
1. Scroll down to the "Build" section of the job configuration page.
2. Add the necessary build steps or actions by clicking on the "Add build step" or "+ Add" button.
3. Configure the build steps according to your requirements. This could include tasks like building the code, running tests, or deploying the changes.

## Step 6: Save and Test the Configuration
1. Save the job configuration by clicking on the "Save" or "Apply" button.
2. To test the configuration, create a new pull request on your develop branch in your version control system.
3. Observe the Jenkins job's build history or console output to verify that it was triggered and executed the desired actions.
