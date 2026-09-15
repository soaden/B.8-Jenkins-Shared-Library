# Jenkins Shared Library Demo
This repository is checked out by Jenkins and implements a Jenkins Shared Library.

## Technologies
* Jenkins
* Groovy

## Usage
The library provides reusable pipeline functions that can be invoked from Jenkinsfiles in other repositories.  
The `buildJar` and `buildImage` functions defined in this repository are consumed by the `Jenkinsfile` in a separate Jenkins Pipeline Demo repository: https://github.com/soaden/B.8-Jenkins.  
This approach keeps reusable pipeline logic in a centralized library instead of defining the same functions separately in each pipeline.

## Repository structure
* `vars/` - contains reusable pipeline function definitions, including `buildImage.groovy` and `buildJar.groovy`.
* `src/` - contains Groovy class definitions that can be used by functions in `vars/` (also allowing logic to be reused across functions). Not used in the current implementation.
* `lib/` - standard Groovy project libraries.
* `.gitignore` - Git ignore rules.
