# pipeline-library
This repository serves as a location for a starting point for Jenkins pipelines and shared libraries. There is a pipeline template for a Maven application and a Nodejs application.

## Jenkinsfiles and Pipelines

A Jenkins Pipeline is an automated expression of your process for building, testing, and deploying software. Pipelines allow us to create simple continuous integration pipelines as well as complex continuous delivery pipelines. There is a large set of tools available for modeling the delivery process "as code" using Pipeline DSL. While pipelines are normally fully automated, they can be pausable and wait for manual approval before continuing to run. Pipelines also integrate well with other Jenkins plugins, making the pipeline extendible. Pipelines are written in Groovy and `script` blocks accept any valid Groovy syntax.

A Jenkinsfile is a way of checking your pipeline into source control. This allows you to:

1. Version control your pipeline

2. Iterate upon the pipeline

3. Single source of truth

4. Share with others and collaborate on the pipeline

`agent` specifies jenkins slave node where you want to run the jobs. Can be defined per Stage as well.

`triggers` tell Jenkins the automated ways which the pipeline should be triggered to run.

`environment` specifies a list of key-value pairs that will be defined as environment variables.

`tools` specify global tool configurations.

`stages` defines different phases of a Pipeline. For eg. Build/CodeQuality/Deploy/Test.

`steps` these are the steps defined within a stage. This could be a shared library call or specific executions depending on the available plugins.

`input` allows you to prompt for manual approval before continuing the running of the pipeline.

`post` defines one or more additional steps that are run upon the completion of a pipeline stage, or at the end of the entire pipeline.

## Shared Libraries
