[![Community Extension](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community) [![](https://img.shields.io/badge/Lifecycle-Stable-brightgreen)](https://github.com/Camunda-Community-Hub/community/blob/main/extension-lifecycle.md#stable-) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent)

community-hub-release-parent
======================

use this parent POM to do releases via the  [Community Hub Maven release action](https://github.com/camunda-community-hub/community-action-maven-release) to:

- [Camunda Artifactory](https://artifacts.camunda.com/): Snapshots and releases
- [Sonatype](https://oss.sonatype.org/#stagingRepositories) (aka Maven Central): Releases


Usage
-----

In your pom.xml, add a parent:
```
<parent>
    <groupId>org.camunda.community</groupId>
    <artifactId>community-hub-release-parent</artifactId>
    <version>1.4.0</version>    
    <relativePath />
</parent>  
```
