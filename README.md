This minimal Java web application was created for testing Gradle
[Gretty plugin](https://github.com/akhikhl/gretty#readme)
with [Gradle Docker image](https://hub.docker.com/_/gradle).

1. [Install Docker](https://www.docker.com/get-started).
2. Clone https://github.com/haba713/hello_gretty.
3. `cd hello_gretty`
4. Install Gradle wrapper:
   `docker run --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle wrapper`
5. Run task `tomcatRun`: `./gradlew tomcatRun`
6. Browse http://localhost:8080/hello_gretty.
7. Terminate the task by pressing enter in terminal.
8. Run task `tomcatRun` with Gradle Docker image:
   `docker run --rm -u gradle -p 8080:8080 -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle tomcatRun`
9. The task `tomcatRun` is started (takes some time) but for some reason the
   container terminates immediately after that. Maybe the task was completed
   without pressing any key.
