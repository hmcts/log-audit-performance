# LAU Performance Tests

Gatling performance tests for Log and Audit
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Purpose

The L&A Case Audit microservice covers case activity (case creations, updates and views) and case searches and are mainly used by the Fraud team.
'Case Activity' records the user actions, such as View, Update,Create Etc whereas 'Case Searches' relates how many cases the user accessed during their search.
The 'Logon Results' shows the results from each time the User log ins during the set time period. 
There will be two type of searches that will need to be tested: Case Audit (Which is CCD) and Logon (which is IDAM).

The deletion of cases by the case disposer is now also recorded within the Log and Audit service, which can be viewed via the deletion search. 


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


## Users
The lautest role has cft-audit-investigator role to access the audit search (you can also see deleted cases changing the activity to delete).
The lau_all user has the  role has cft-audit-investigator and cft-service-logs role to access the audit and deletion searches.
The lau_service_logs user has the cft-service-logs role to just access the deletion search.

## Building and deploying the application

### Building the application

The project uses [Gradle](https://gradle.org) as a build tool. It already contains
`./gradlew` wrapper script, so there's no need to install gradle.

To build the project execute the following command:
  ```bash
    ./gradlew build
  ```

### Running the application
The LAUSimulation runs all the searches. 

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
