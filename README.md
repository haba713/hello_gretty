This minimal Java web application was created for testing Gradle
[Gretty plugin](https://github.com/akhikhl/gretty#readme)
with [Gradle Docker image](https://hub.docker.com/_/gradle).

1. [Install Docker](https://www.docker.com/get-started).
2. Clone https://github.com/haba713/hello_gretty.
3. `cd hello_gretty`
4. Run task `tomcatRun` with Gradle Docker image:
   `docker run --rm -u gradle -it -p 8080:8080 -v "$PWD":/home/gradle/project -w /home/gradle/project gradle gradle tomcatRun`
5. Wait for Tomcat to start.
6. Browse http://localhost:8080/hello_gretty.
