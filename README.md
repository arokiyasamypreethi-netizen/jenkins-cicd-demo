# Jenkins CI/CD Demo

This repository contains the Jenkins Pipeline used for the Week 10 DVP assignment, demonstrating CI/CD automation using Jenkins.

## What This Pipeline Does

- Prints a welcome message to the console
- Displays basic system information (date, time, disk usage) using Windows batch commands
- Simulates a build process
- Displays a success or failure message using Jenkins' native `post` block

## How It's Used

This `Jenkinsfile` is consumed by a Jenkins Pipeline job configured with:

- **Definition:** Pipeline script from SCM
- **SCM:** Git
- **Repository URL:** (this repo's URL)
- **Branch:** `main`
- **Script Path:** `Jenkinsfile`

Jenkins clones this repository on each build and executes the pipeline defined in `Jenkinsfile`, rather than using a script pasted directly into the Jenkins UI. This is known as **Pipeline as Code**.

## Pipeline Stages

| Stage | Description |
|---|---|
| Greeting | Prints the welcome message |
| System Info | Runs `date`, `time`, and disk usage commands |
| Build Simulation | Simulates a compile/test/package step |
| Post Actions | Reports success or failure via `post { }` |

## Related Work

This pipeline is part of a larger assignment that also includes a separate Jenkins **Freestyle Project** demonstrating the same CI/CD concepts through Jenkins' UI-based configuration, without using code (Jenkinsfile).

## Author

Preethi A — DVP Week 10 Assignment
