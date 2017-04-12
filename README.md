# Kinesis-CI - Sample Project

[![Build Status](http://jenkins.kinesis-ci.com:8081/buildStatus/icon?job=GitHub_-_Education_and_Innovation)](http://jenkins.kinesis-ci.com:8081/job/GitHub_-_Education_and_Innovation)

Education and innovation is a sample project for users of the Kinesis CI tool for Tableau.
Kinesis CI is a test framework that adds automated testing and continuous integration capability to Tableau Server.
For more information on Kinesis CI, please visit http://kinesis-ci.com

![screenshot](/screenshot.png)

## Concept

This project is designed to give you an example for setting up your testing projects in Kinesis CI.

It contains a collection of test cases for a Tableau Workbook – Education and Innovation,
including tests for the following components:
-	Load data into a database
-	Publish Tableau workbooks and data sources to Tableau Server
-	Refresh data extracts
-	Filters
-	Parameters
-	Checking data against an expected data set
-	Checking the layout of the Dashboard to an expected layout
-	Checking data against pre-defined rules and criterias
-	Checking data against the datasource by an SQL query in the underlying database

This example goes hand in hand with the documentation of Kinesis CI, which you can find under http://kinesis-ci.com/docs/


## How to use this demo project?

1.	Clone the repository in Kinesis Designer (File -> Clone Git Repository and enter https://github.com/Kinesis-CI/education-and-innovation.git) and open ``project.json``. This ``project.json`` file contains key
information to identify the individual test projects within this directory.
Alternatively, you can use the Kinesis Command Line Interface and open the files in a text editor.

2.	Edit context variables to fit your environment. i.e. reference the Tableau Server you are using within your organization and use a database you have access to. For more information on context variables visit
http://kinesis-ci.com/docs/context-variables/main.html

3.	In Load Data task tailor database reference to a database you would like to use. For detailed information visit http://kinesis-ci.com/docs/tasks/load-data.html

## Directory layout

File Type    | Description
------------ | --------------
``src`` | Contains the Tableau source files that have been imported into the given Project
``context`` | Contains the JSON files that define your context variables. For more information on context variables refer to the documentation under  http://kinesis-ci.com/docs/command-line-interface/main.html
``test`` | Contains files related to the individual Tests that have been created within the Project
``test/<TEST_NAME>/resources`` | Test resources. These are typically data files (.csv) needed to load data into source systems (i.e. databases) or validate data to expected results
``test/<TEST_NAME>/kinesis.json`` | JSON files that describe the individual Test steps that have been created within the Project
``project.json`` | JSON file that contains the key information to identify the individual Projects. This is only needed for Kinesis Designer, but not to run tests from the Command Line Interface

For more information on the Directory Layout please see http://kinesis-ci.com/docs/getting-started/create-a-new-project.html#standard-directory-layout

## Integration with CI tools

If you want to run tests automatically on a Continuous Integration Server, for example on Jenkins, TeamCity or any other similar tool, then you will need to install the Kinesis Command Line Interface to the server where your CI/CD server is running.

Command Line Interface allows you to run previously created Kinesis tests and integrate it with the CI tool of your choice.

For more information on the integration of Kinesis CI and Jenkins, please see http://kinesis-ci.com/docs/continuous-integration/main.html
