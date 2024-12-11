# Experiment Documentation 
## Experiment ID: @InsertExpIDHere@

## Purpose
This repository will be the primary means of technical communication between your team and POPROX staff throughout the course of developing, executing, and evaluating your POPROX experiment.

## Documentation

Refer to the [POPROX Researcher Guide](https://docs.poprox.ai/index.html) for information on how to use this repository and the overall process of getting your experiment to work on the platform.

## Contents
 
* [Intake form]. This was the document that you initially supplied to get your project approved for intake into the POPROX platform. It may need to be updated as your design and plans evolve. 
* Human subjects folder (`human-subjects`):
	* Protocol: We have supplied here a template protcol based on the blanket approval provided by our institutional IRB. Your institution may require a different format for this information. You will need to fill in the details of this work and edit sections that do not apply to your work. The protocol must be approved by the local IRB for you and your collaborators in order for your experiment to proceed. If your experiment design falls outside the blanket approval (see (Human subjects discussion)[https://docs.poprox.ai/guide/stages/specification.html#human-subjects] in the Researcher Guide), we will also need to seek approval from our IRB for an exception.
	* Master protocol: This is a copy of the master protocol approved for the POPROX platform. Your local IRB may request this document as part of the approval process.
	* Approval: This is a placeholder for the approval letter(s) from your local IRB(s). 
* Experiment design. This document specifies the phases of your planned study, the different experimental treatments you will apply, and the groups of users that you are studying. 
* Manifest. This TOML document is the technical specification for your experiment. A sample document is supplied, which you should edit as needed. See the (manifest specfication)[https://docs.poprox.ai/reference/experiments/manifest.html] for additional details.
* Test results. When tests are conducted, detailed results will be placed in the `test` folder for review by both the experimenter and the POPROX team.

## To instantiate for a new experiment

1. Create a new repository with this as the template
1. Copy approved intake form to repository
1. Copy this file README-repo.md to README.md
1. Delete this file README-repo.md
1. Insert experiment ID in line 2 of README.md
1. Commit changes
