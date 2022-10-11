[![Community Extension](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community) [![](https://img.shields.io/badge/Lifecycle-Stable-brightgreen)](https://github.com/Camunda-Community-Hub/community/blob/main/extension-lifecycle.md#stable-) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent)

community-hub-release-parent
======================

This is a POM which can be inherited for [Community Hub Maven releases](https://github.com/camunda-community-hub/community-action-maven-release), defining some common release properties. It allows deploying to two repositories simultaneously. One is a Nexus OSS server, the other one a Nexus Enterprise server.
It will deploy the artifacts at the end of the build to keep the window of failure small when talking to external systems.

Usage
-----

Inherit the community-hub-release-parent POM inside your project like so:  

```
<parent>
    <groupId>org.camunda.community</groupId>
    <artifactId>community-hub-release-parent</artifactId>
    <version>1.3.1</version>    
    <relativePath />
</parent>  
```
