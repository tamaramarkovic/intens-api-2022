# Installations
Install Java 8 and Docker.

# Running the application
Open PoweShell or CommandLine in the folder where is application stored to build and run the Docker image:
1. `docker build --platform linux/amd64 -t intenspraksa .`
2. `docker run -p 8080:8080 -t intenspraksa`

# Workflows
In this repository there are two workflows:
1. Integration workflow (integration.yml) is happening after the pull request on master branch.

2. Deployment workflow (deployment.yml) is happening after the push command on master branch.
   - Through Docker metadata action image version is set up.
   - For image deployment Github Container Registry is used.
