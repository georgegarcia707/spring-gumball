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

	![cd t](images/Screen%20Shot%202021-05-15%20at%203.18.34%20PM.png)

* went into GoogleCloud to create the service account and generate the key

	![cd t](images/Screen%20Shot%202021-05-14%20at%207.20.25%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-14%20at%207.19.57%20PM.png)

* in github I set the action secrets:

	![cd t](images/Screen%20Shot%202021-05-14%20at%207.24.59%20PM.png)

* created the GKE cluster "cmpe172"

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.33.53%20PM.png)

* triggered the CD workflow deployment by creating a new release
	
	![cd t](images/Screen%20Shot%202021-05-15%20at%203.52.21%20PM.png)

* PROBLEM: gave me an authentication error
	* SOLUTION: set role for the service account in GoogleCloud

* re-ran the CD workflow deployment and successfully deployed

	![cd t](images/Screen%20Shot%202021-05-15%20at%201.44.04%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.14.38%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.14.54%20PM.png)


* GKE Workload
	
	![cd t](images/Screen%20Shot%202021-05-15%20at%202.15.48%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.17.06%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.17.19%20PM.png)

* GKE Service

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.16.18%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.17.36%20PM.png)

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.17.45%20PM.png)

* created the Ingress
	* waited for ingress to get created

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.40.01%20PM.png)

* successfully deployed spring gumball

	![cd t](images/Screen%20Shot%202021-05-15%20at%202.40.24%20PM.png)

