# JENKINS
To Install Jenkins Successfully JDK 11 or JDK 17 is needed.

## Creating a Job

### FreeStyle Project
It allows you to create a general purpose job with customizable options but manual work is needed.

### Pipeline
This option lets you define your job as a scripted or declarative pipeline using the Jenkinsfile. Pipelines provide a powerful and entensible way to define complex workflows and continous delivery processes.

### Multibranch Pipeline
If you have a project with multiple branches, this option automatically creates a separate job for each branch, enabling you to build , test and deploy them independently.

### Github Organization
If your code is hosted on Github, this option scans your organization repositories and creates jobs for each repository automatically. It simplifies the process of setting up Jenkins jobs for multiple projects.

### Copy Existing Job
If you already have a job with similar configurations, you can use this option to create a new job by copying the settings of an existing one. It saves time by prepopulating the new job with the selected job's configurations.

### External Job
this option allows you to execute a job defined outside Jenkins, such as a script or command in your version control system. It Integrates external processes into Jenkins and captures thier outputs.

### Folder
If you have a large number of jobs or need to organize them into a hierarchical structure, you can create a folder to group related jobs together. Folders make it easier to manage and navigate through your jobs.