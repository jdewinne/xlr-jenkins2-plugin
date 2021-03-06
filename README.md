# xlr-jenkins2-plugin

This plugin offers an interface from XL Release to Jenkins 2.x. 

# CI status #

[![Build Status][xlr-jenkins2-plugin-travis-image]][xlr-jenkins2-plugin-travis-url]
[![Codacy Badge][xlr-jenkins2-plugin-codacy-image] ][xlr-jenkins2-plugin-codacy-url]
[![Code Climate][xlr-jenkins2-plugin-code-climate-image] ][xlr-jenkins2-plugin-code-climate-url]

[xlr-jenkins2-plugin-travis-image]: https://travis-ci.org/xebialabs-community/xlr-jenkins2-plugin.svg?branch=master
[xlr-jenkins2-plugin-travis-url]: https://travis-ci.org/xebialabs-community/xlr-jenkins2-plugin
[xlr-jenkins2-plugin-codacy-image]: https://api.codacy.com/project/badge/Grade/a6f64efd62f341acb50f67c511d3fb42
[xlr-jenkins2-plugin-codacy-url]: https://www.codacy.com/app/joris-dewinne/xlr-jenkins2-plugin
[xlr-jenkins2-plugin-code-climate-image]: https://codeclimate.com/github/xebialabs-community/xlr-jenkins2-plugin/badges/gpa.svg
[xlr-jenkins2-plugin-code-climate-url]: https://codeclimate.com/github/xebialabs-community/xlr-jenkins2-plugin

# Installation #
+ Place the `jar` file under plugins.
+ Remark: Starting v1.1.0, XLR v6.1.0+ is required.

# Usage #
+ Trigger: You can configure a trigger by first going to your template and selecting `Triggers`
  ![Jenkins Trigger](images/jenkins_trigger.png)
  
  When selected, you can provide the Jenkins details.
  ![Jenkins Trigger Details](images/jenkins_trigger_details.png)
  
+ Tile: To be done. 
+ Tasks 
    + Jenkins.GetBuildParameters tasks allows to fetch the parameters from an executed job.
      ![Jenkins GetBuildParameters](images/jenkins_get_parameters.png)
    + Jenkins.Build: The Jenkins build task is being extended with the following property
        + `ignoreFailure`: If true, XL Release will not fail the task if the Jenkins job fails.

# Testing and Development #
If you want to start this plugin, you could use the following command `./gradlew runDockerCompose`. 
This will give you 2 containers (Jenkins and XL Release), with the plugin preloaded.

* How to retrieve the admin password for jenkins? 

`docker exec -it docker_jenkins_1 cat /var/jenkins_home/secrets/initialAdminPassword` 



