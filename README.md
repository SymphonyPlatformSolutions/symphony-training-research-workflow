# symphony-training-research-workflow

This is the example SWADL workflows from the [Symphony Developer Certification Program](https://learn.symphony.com).  Please use this project while or after reviewing the course *Implementing Workflows with Symphony WDK 1.0*

This repository is divided into branches, each representing the end state of each demo in the course.
* [Chapter 4: Creating a Workflow](https://github.com/SymphonyPlatformSolutions/symphony-training-research-workflow/tree/chapter-4)
* [Chapter 5: Activities, Events & Variables](https://github.com/SymphonyPlatformSolutions/symphony-training-research-workflow/tree/chapter-5)

## Sample WDK 1.0 project
To get started, follow these commands below:

1. Install the Symphony Generator:
    - `npm install -g yo @finos/generator-symphony`

2. Launch the Symphony Generator:
    - `yo @finos/symphony`


# Symphony Workflow Developer Kit (WDK)

## Getting started
Check out the [Getting starting guide](https://github.com/finos/symphony-wdk/blob/master/docs/getting-started.md) for an introduction.

## Project's structure
The generated project has 4 folders:
- **[rsa]:** contains generated RSA public and private keys for the workflow bot.
- **[workflows]:** can contain workflows to be executed by the bot.
- **[src]:** contains custom activities with Java models and activity executors.
- **[lib]:** can contain JAR files and dependencies of custom activities.

## How to run the generated bot
After placing your _swadl.yaml_ workflow file in _[workflows]_ folder, you can execute _workflow-bot-app.jar_.
````shell
    java -jar workflow-bot-app.jar
````
_nb: Java 11 is required to run the WDK_

## Useful tasks to use
This project comes with the following Gradle tasks:
- ``./gradlew botJar`` used to download the WDK jar (executed upon bot's generation)
- ``./gradlew customActivityLibs`` used to copy custom activity dependencies in [lib] folder.
- For more details, use ``./gradlew task --all``