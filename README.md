# LAU Performance Tests

 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

 ## Purpose

 This is the Log And Audit Performance Tests implemented in Scala using Gatling.

 ## Overview

 <p align="center">
 <b><a href="https://github.com/hmcts/lau-performance">lau-performance</a></b> • <a href="https://github.com/hmcts/lau-frontend">lau-frontend</a> • <a href="https://github.com/hmcts/lau-idam-backend">lau-idam-backend</a> • <a href="https://github.com/hmcts/lau-case-backend">lau-case-backend</a> • <a href="https://github.com/hmcts/lau-shared-infrastructure">lau-shared-infrastructure</a>
 </p>

 ## Getting Started

 This is repository for the LAU Performance Tests
 - Step1: Clone the repo to your local/VM to run
 - Step2: cd into the lau-performance directory
 - Step3: Edit the run time settings from the LAU.scala simulation file
 - Step4: Run the test with the command `gradle gatlingRun`               
 
 ## Building and deploying the application

 ### Building the application

 The project uses [Gradle](https://gradle.org) as a build tool. It already contains
 `./gradlew` wrapper script, so there's no need to install gradle.

 To build the project execute the following command:
 ```bash
   ./gradlew build
 ```

 ### Running the application

 To run locally: - Performance test against the perftest environment: 

 ```bash
 ./gradlew gatlingRun
 ```

 Flags: - Debug (single-user mode): -Ddebug=on e.g. ./gradlew gatlingRun -Ddebug=on - Run against AAT: Denv=aat e.g.:
 ```bash
 ./gradlew gatlingRun -Denv=aat
 ```

 ## License

 This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details..
