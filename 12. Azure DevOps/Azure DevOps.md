* Integration of all DevOps tools.
* Mandatory things for Azure DevOps: Organization, Project.

Main parameters to know: Boards, Repos, Pipelines, Artifacts, Test Plans.
--
* Boards: For planning purpose(Work tracking (Agile, Scrum)).
	* All task related stuff is kept here, what to do?, how to do?, how much to do?...... are tracked here.
	* We can also integrate ticketing tools like Jira and create tickets, tasks(Plan) for what to build, to fix bugs etc...
	* Backlogs: Sprint(15 days default)-time dedicated for doing task. You can define start and end time for task. You might have scrum calls.

* Repos: To store our code. Similar to Source Code Management. We can integrate our GitHub with this(Git repositories).
	* Ex: GitLab, GitHub, ButBucket.

* Pipelines: For Testing & Packaging code(CI/CD purpose). CI=Builds, CD=Releases.
	* Written in Yaml.
 	*  
 	* Library: To save dependencies.
	* Tasks: Part of builds, Releases.
	* Deployment groups: Used for releases.

* Test Plans: For testing purpose.
	* Manual test plan - free.
	* Automates test plan - costly.
 * Test Plan(A group of related test cases organized to validate a specific part of your application)
 *└── Test Suites(Logical groupings within a test plan. Can be static, requirement-based, or query-based)
 *     └── Test Cases(Step-by-step instructions for manually testing a feature. You define expected outcomes for validation)
 *          └── Test Steps (with expected results)


* Artifacts: Libraries/Dependencies for production/code(Package management).
	* To store the build artifacts produced by build pipelines. EX: jar, war, nuget, tar files. 
	* You can store and share different packages from public & private sources.
   	* Supports maven, nuget, npm packages.	
	* NOTE: If you build an normal artifact(jar, war etrc....) then push to repository & if you build an image then push to Container registry.

* Test plans: Browser based test management tool for testing your application(Manual and exploratory testing).
  	* Test plan types: Manual test plan, automated test plan.
  	* This will be executed as part of CI/CD process & test reports can be viewed.

* Release pipeline: You can have separate pipelines for CI & CD.
  	* Release pipelines are for continuous deployent.
  	* Other CI/CD platforms always have single pipeline to perform CI & CD.
 
AZURE DEVOPS ARCHITECTURE
--
* Core(main part) has boards, repos etc.... all pipeline related options are here - provided by MS Azure.
* Agent(All pipeline tasks run here) - Provided by MS hosted agent.
  
Dashboard:
--
* We can add widget to it so that it displays what we have & need to do.

Queries: To find out items from work items. You have 100's of items in that you can filter using queries.
--

Main files for Azure DevOps:
--
* .json 
* parameters.json 
* pipeline.yaml

What happend when you create a project?
--
* An empty git repo with project name is created.
-----------------------------------------------------------------------------------------------------------
# Types of agents in Azure DevOps

| Type             | Managed By | Customization | Cost                      |
| ---------------- | ---------- | ------------- | ------------------------- |
| Microsoft-hosted | Microsoft  | ❌ Limited     | Pay-per-use (free limits) |
| Self-hosted      | You        | ✅ Full        | You manage the VM         |
-----------------------------------------------------------------------------------------------------------
# ✅ Types of Pipelines in Azure DevOps

Azure DevOps provides two main types of pipelines to automate build, test, and deployment workflows. Here's a quick overview:

---

## 1. Classic Pipelines (UI-Based)

- Created using the Azure DevOps **web interface**.
- Easy to use with **drag-and-drop** steps.
- Ideal for **beginners** or simple CI/CD projects.

---

## 2. YAML Pipelines (Code-Based)

- Defined in `.yaml` files and stored in the **code repository**.
- Fully **version-controlled** and **flexible**.
- Best for teams following **DevOps practices** and needing automation at scale.

---

## 📝 Additional Pipeline Types

| Type               | Description                            |
|--------------------|----------------------------------------|
| **Build Pipeline** | Builds the code and runs tests         |
| **Release Pipeline** | Deploys the application               |
| **Multi-Stage Pipeline** | Combines build, test, and deploy in one YAML pipeline |

---

## 📌 When to Use What?

| Use Case                     | Recommended Pipeline Type |
|------------------------------|---------------------------|
| Simple or quick setup        | Classic (UI-Based)        |
| Complex automation workflow  | YAML (Code-Based)         |
| Teams practicing GitOps/DevOps | YAML (Code-Based)       |

---

Feel free to customize or extend this guide based on your team's use case!
-----------------------------------------------------------------------------------------------------------
PIPELINE EXPLANATION: 
--
Building blocks of pipeline:
--
* TRIGGER: To specify your branch.

* POOL: Specifies the agent type you want to perform the task.
  	* You can specify your agent pool globally or in jobs induvidually.
  	* The agent specified globally can be overridden by pool specified in jobs.

* VARIABLES: To pass any variable values that can be used later.

* STEPS: Contains induvidual tasks to be performed.
  	* It can contain both script or tasks or both.

* POOL: Specifies the agent type you want to perform the task.

* AGENT: An agent is someone who runs jobs on him & is selected from a agent pool(linux, windows, macOS).

* JOBS: Test and deploy application on particular OS type.
  	* Parallel task execution, that helps reduce execution time.
  	* Use of multiple jobs: Execute tests on different OS.
  	* Also in multiple jobs scenario each job runs on induvidual agent and the steps in job are executed on same agent.
  	* So, with jobs we can run series of steps in different environment.

* Deployment jobs: For deployment steps, it is recomended to use specific deployment jobs.

* Templates: All the pipelines can reference other pipelines.yaml in another repository.
  	* you can create templates for jobs, stages & steps.
  	* Can refer or pass template using "template" option in pipeline.
* EX:
stages:
- stage: Install
  jobs:
  - job: npminstall
    ....
- template: templates/stages1.yml
- template: templates/stages2.yml
- ---------------------------
jobs:
- job: Linux
  ....
  steps:
  - template: templates/include-maven-steps.yml

* Parameters: you can specify parameters and their data types in templates.
* EX:
parameters:
  - name: appName
    type: string
    To refer: ${{parameters.name}}... etc
    
* ENVIRONMENTS: To deploy in different environments.

NOTE: Release pipeline can be created only using UI- no yaml file for this. 
--
  
Example Pipelines: azure-pipelines.yml
--
* Basic Pipeline
----
# Specify you branch
trigger:
- <branch>

# Can agent pool globally or in jobs
pool:
  vmImage: ubuntu-latest

# Specify variables here
variables:
  <key>: <value>
  <key>: <value>

stages:
# Stage 1: Build and Test
- stage: BuildAndTest
  displayName: Build and Test Stage
  jobs:
  - job: BuildJob
    displayName: Build and Test Job
    pool:
      vmImage: 'ubuntu-latest' # Specify the agent pool (Ubuntu Linux)
    steps:
    # Step 1: Checkout source code
    - task: Checkout@1
      displayName: Checkout Code

    # Step 2: Install dependencies
    - script: |
        echo "Installing dependencies..."
        sudo apt-get update
        sudo apt-get install -y build-essential
      displayName: Install Dependencies

    # Step 3: Build application
    - script: |
        echo "Building $(appName) in $(buildConfiguration) mode..."
        # Simulate build command here
      displayName: Build Application

    # Step 4: Run tests
    - script: |
        echo "Running tests for $(appName)..."
        # Simulate test command here
      displayName: Run Tests
----

* Multi job pipeline
----
# azure-pipelines.yml

trigger:
- main

# Variables
variables:
  appName: MyApplication
  buildConfiguration: Release

# Stages and jobs
stages:
- stage: BuildAndTest
  displayName: Build and Test Stage
  jobs:

  # Job 1: Build
  - job: BuildJob
    displayName: Build Application
    pool:
      vmImage: 'ubuntu-latest' # Specify the agent pool
    steps:
    - task: Checkout@1
      displayName: Checkout Code
    - script: |
        echo "Building $(appName) in $(buildConfiguration) mode..."
        # Simulate build command
        echo "Build complete!"
      displayName: Build Application

  # Job 2: Unit Tests
  - job: UnitTestJob
    displayName: Run Unit Tests
    pool:
      vmImage: 'ubuntu-latest'
    dependsOn: BuildJob # Ensures this job runs after BuildJob
    steps:
    - script: |
        echo "Running unit tests for $(appName)..."
        # Simulate unit test command
        echo "Unit tests completed successfully!"
      displayName: Run Unit Tests

  # Job 3: Integration Tests
  - job: IntegrationTestJob
    displayName: Run Integration Tests
    pool:
      vmImage: 'ubuntu-latest'
    dependsOn: UnitTestJob # Ensures this job runs after UnitTestJob
    steps:
    - script: |
        echo "Running integration tests for $(appName)..."
        # Simulate integration test command
        echo "Integration tests completed successfully!"
      displayName: Run Integration Tests
----
















































