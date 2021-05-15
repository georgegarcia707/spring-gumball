# CMPE 172 - Lab #10 Notes
# spring-gumball ci/cd example

## CI Workflow (Part 1)

Procedure:

* Created a new GitHub repository titled spring-gumball

* downloaded the starter code

* move the starter code into the repository

* In github, I went into actions and created the CI workflow:
	* JAVA CI with Gradle 

	![ci t](images/Screen%20Shot%202021-05-14%20at%206.49.21%20PM.png)

* went into deployment.yml to create an edit and decrease replicas to 2 to use the CI workflow

* PROBLEM:
	* the workflow was not running
	* SOLUTION: I noticed that the gradle.yml file had the wrong branch name.
		* updated the branch name from "main" to "master"

* made an edit and pushed it to the branch

* the CI workflow ran and did what it was supposed to do

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.43.06%20PM.png)

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.44.01%20PM.png)

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.45.25%20PM.png)

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.54.45%20PM.png)



## CD Workflow (Part 2)

* went into actions again and created the google.yml workflow

* went into GoogleCloud to create the service account and generate the key

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.20.25%20PM.png)

	![ci t](images/Screen%20Shot%202021-05-14%20at%207.54.45%20PM.png)

