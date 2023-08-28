Below are the steps in Jenkins - 

- Create a new project in Jenkins
- Add the GitHub URL of this project in the Source Code Management section
- Select 'GitHub hook trigger for 'GITScm polling' in 'Build Triggers' section
- Now add the build steps to start the container and save the project

Below are the steps in the GitHub project - 

- Go to the settings of this project and in the webhooks section click on 'Add webhooks'
- Go to payload URL, add the public IP address with the port on which you are accessing Jenkins and 'github-webhook'
- It will look like this (just and example) 'https://1.1.1.1:8080/github-webhook/'
- Select 'application/json' in content tyoe and select 'just the push event' in next option and click on 'Add-webhook'
- Now, make any changes in this project and commit them.

In Jenkins, check that one build will be after you commit. So, GitHub webhooks are used to trigger a build in Jenkins whenever someone commits to the project if we select 'just the push event'

