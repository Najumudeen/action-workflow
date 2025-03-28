# action-workflow

3 core components for github action

workflows
jobs
steps

How execute the shell script with in your workflow?

How you run multiple jobs in your single workflow

Note: Each jobs runs on different virtual machine

3 jobs run paraell

We have to setup jobs run as sequence manner

needs keyword
------ 

How to share the files from one job to another job?

Go to github market place and search for download and upload build artifact

@actions/upload-artifact
@actions/download-artifact


How store environment variable in the workflow?


Triggering a workflow? list of events link as below

https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows

workflow_dispath events

you can provide input values with input type


Using Job Concurrency

How approximately the job runs

First job will with following error

concurrency:
          group: production-deplopyment
          cancel-in-progress: true

Canceling since a higher priority waiting request for production-deplopyment exists

Second job will wait until the first job completed.

concurrency:
          group: production-deplopyment
          cancel-in-progress: flase

A job in this workflow is waiting for deploy to complete before running

Timeout for Jobs and Steps

By default github acion automatically kill after 6 hous.

step level
job level

The action 'Docker Run' has timed out after 1 minutes.

What is main use matrix keywords here?

  if we have multiple os version and run mutiple images to just avoid not use multiple line of codes.


Additional feature of matrix strategy

  jobs are run in parallel

  exclude keyword # not run 
  include keyword # only run matcing senario

strategy:
    fail-fast: false # by default it's true. it going cancel any job running on the queue when the job fails.
    max-parallel: 2  # no of jobs run simultaneously

Access Workflow Context
-------------------------

How to access the context in to your workflow

https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/accessing-contextual-information-about-workflow-runs

Using If Expression in Jobs

https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/evaluate-expressions-in-workflows-and-actions


Some random text
