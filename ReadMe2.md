# Jenkins :cd:

Jenkins is an open source automation tool written in Java with plugins built for Continuous Integration purpose. Jenkins is used to build and test your software projects continuously making it easier for developers to integrate changes to the project, and making it easier for users to obtain a fresh build

## What is CI CD ?
Continuous Integration is a development practice where developers Integrate rate code into a shared repository, frequently. This means that the code is tested through an automated build and automated test, in which code is only pushed if it works. If the code does not work it wont be pushed.

Continuous Deployment is related to Continuous Integration, yet is about continuously Deploying working code several times a days.   

## What is an Automation Server?

An automation server is a system like Jenkins that allows us to use CI and CD for development. 

## Why do we restrict a build and how?

We restrict the build to only build on the test environment that way we avoid breaking the main code in the automation server.
