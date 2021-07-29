## Maven Build

Access the Jenkins URL provided and create a job that has 3 parameters. The job will clone a Maven Project repository and build it.
In order to do so:
 * Create a Free-Style Job called **build_maven_user0[1-9]**
 * This job must be feeded with 3 parameters:
   * REPO
   * USER
   * BRANCH
 * The project that will be used to do so is [maven-simple](https://github.com/jitpack/maven-simple)
 * Clone the above project and build it with:
   * ```mvn clean install --settings=/opt/SCM/settings.xml -Dmaven.repo.local=${WORKSPACE}/.m2```
 * Execute the job
 * Delete the workspace after conclusion


The result must be simmilar to this:
![EX2-Output](../images/ex2-output.png)
