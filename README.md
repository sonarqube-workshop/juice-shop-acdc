Welcome to SonarQube workshop. In this exercise we will look at core SonarQube features.

<details>
  <summary>Task 1. Initial setup</summary>
If the Action gods were merciful today, the automation has already invited you to SonarQube Workshop organisation, created a repository from the template and used your GutHub username for repository name.

If you haven't done so yet, please log into SonarQube Cloud from https://sonarcloud.io/login. Please make sure to use GitHub for authentication.

![GitHub Login](workshop_images/github_login.jpg)

While it's possible to log in with other DevOps platforms, we will be using GitHub in this exercise. Your SonarQube Cloud account will be created if this is the first time you are logging into the platform. Once your account is created, you automatically will be added to the SonarQube Workshop organisation.
</details>

<details>
  <summary>Task 2. Create a SonarQube Cloud project from a GitHub Repository</summary>

To create a new project in SonarQube Cloud from your GitHub repository, follow these steps:
  1. Log in to [SonarQube Cloud](https://sonarcloud.io/login) using your GitHub account.
  2. Click on **"+ Analyze new project"** 
  ![Create project](workshop_images/create_project.jpg)
  
  3. Make sure to select **SonarQube Workshop** in organisation list. In the list of repositories, find and select the repository that was created for you. Make sure the repository name includes your GitHub username (e.g., `sq-workshop-yourusername`). Click on **Set Up** button.
  ![Select the repository](workshop_images/select_reporitory.jpg)
  
</details>


<details>
  <summary>Task 3. Setup Sonar scanning in GitHub Actions</summary>
  
  1. Go to `Administration` -> `Analisys Method`. 
  
  ![Analysis Method](workshop_images/analysis_method.jpg)

  As you can see, the automated analysis is enabled by default. We will need to turn that off and set up the analysis with GitHub Actions. Disable the automatic analysis and click on `With GitHub Actions`:
  
  ![Setup analysis](workshop_images/setup_analysis.jpg)

  Follow these steps to setup the scanning in GitHub Actions:
  
  2. Create `SONAR_TOKEN` secret in your test repository in GitHub. Use the value from the previous screen.

  ![Create new secret](workshop_images/new_repository_secret.jpg)

  ![Create SONAR_TOKEN](workshop_images/sonar_token.jpg)

  3. The workshop automation should have created a `sonar.yml` workflow in `.github/workflows` directory. If so - go to next step. Ohterwise - create a new workflow in `.github/workflows` directory in your test repository in GitHub. Click on `JS/TS & Web` to get the code for the workflow:

  ![Workflow details](workshop_images/workflow_details.jpg)

  ![Add new file](workshop_images/create_new_file.jpg)

  ![Create the workflow](workshop_images/create_workflow.jpg)

  Pro tips:
  - change the default `build.yml` name to `sonar.yml`
  - change the name of the workflow in the file (line #1) to `SonarQube Scan`

  ![Commit the workflow](workshop_images/commit_workflow.jpg)

  4. The workshop automation should have created a `sonar-project.properties` in your your repository. If so - update the first line with your SonarQube project's key and commit to main branch. Otherwise - create `sonar-project.properties` file in root directory in your test repository in GitHub:

  ![sonar-project.properties file](workshop_images/sonar_project_properties.jpg)

  Creation of `sonar-project.properties` will trigger the workflow which you will be able to monitor in Actions tab:

  ![Actions](workshop_images/actions.jpg)

  ![Sonar workflow run](workshop_images/sonar_workflow_run.jpg)
  
</details>

<details>
  <summary>Task 4. Set up your AC/DC tooling</summary>

  Some blurp.

  To set up the tolling:
  1. Do this
  2. Do this 
</details>
