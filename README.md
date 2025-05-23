[![Community Extension](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community) [![](https://img.shields.io/badge/Lifecycle-Stable-brightgreen)](https://github.com/Camunda-Community-Hub/community/blob/main/extension-lifecycle.md#stable-) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent)

# Camunda Community Hub Release Parent

Use this parent POM to do releases via the [Community Hub Maven release action](https://github.com/camunda-community-hub/community-action-maven-release) to:

- [Camunda Artifactory](https://artifacts.camunda.com/)
- [Maven Central](https://central.sonatype.com/publishing/deployments)

See [Camunda Community Hub release documentation](https://github.com/camunda-community-hub/community/blob/main/maintainers-reviewers/RELEASE.MD) for more info on this.


## Usage

In your pom.xml, add a parent using the [newest version available of this POM](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent):

```xml
<parent>
    <groupId>org.camunda.community</groupId>
    <artifactId>community-hub-release-parent</artifactId>
    <version><!-- Use the newest version available! --></version>
    <relativePath />
</parent>
```
