# CMPE 172 - Lab #10 Notes
# spring-gumball ci/cd example

## CI Workflow (Part 1)

Procedure:

* Created a new GitHub repository titled spring-gumball

* downloaded the starter code

* move the starter code into the repository

* In github, I went into actions and created the CI workflow:
	* JAVA CI with Gradle 

* went into deploymeny.yml to create an edit and decrease replicas to 2 to use the CI workflow

* PROBLEM:
	* the workflow was not running
	* SOLUTION: I noticed that the gradle.yml file had the worng branch name.
		* updated the branch name from "main" to "master"

* made an edit and pushed it to the branch

* the CI workflow ran and did what it was supposed to do
