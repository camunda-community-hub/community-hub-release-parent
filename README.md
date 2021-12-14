[![Community Extension](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community) [![Lifecycle: Proof of Concept](https://img.shields.io/badge/Lifecycle-Proof%20of%20Concept-blueviolet)](https://github.com/Camunda-Community-Hub/community/blob/main/extension-lifecycle.md#proof-of-concept-) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.camunda.community/community-hub-release-parent)

# community-hub-release-parent

This is a POM which should inherited
for [Community Hub Maven releases](https://github.com/camunda-community-hub/community-action-maven-release), defining
some common release properties. It allows deploying to two repositories simultaneously. One is a Nexus OSS server, the
other one is the Camunda Repository. It will deploy the artifacts at the end of the build to keep the window of failure
small when talking to external systems. 

## Usage

Inherit the community-hub-release-parent POM inside your project like so:

```
<parent>
    <groupId>org.camunda.community</groupId>
    <artifactId>community-hub-release-parent</artifactId>
    <version>1.2.1</version>    
    <relativePath />
</parent>  
```
## Properties

The parent provides some properties defining the behavior of the build. By default, there is no reason to change them and 
we provide them just for reference.

| Property                    | Default value               | Meaning | 
|-----------------------------|-----------------------------|---------|
| `java.version`              | `11`                          | Java Version used for compilation | 
| `camunda-hub-encoding`      | `UTF-8`                       | Encoding used in project |
| `camunda-hub-server-id`     | `ossrh`                       | Server id used for artifact deployment     |
| `camunda-hub-nexus-url`     | `https://oss.sonatype.org/`   | Repository URL used for artifact deployment     |
| `camunda-hub-skip-staging`  | `false`                     |  Skip deployment    |


## Profiles

The POM defines several profiles used during the creation of artifacts and release / deploy of them.

### community-action-maven-release

This profile is activating Maven plugins required for creation of additional artifacts required for te publication of the
extension into a public repository. Especially, it triggers generation of Sources JARs, JavaDoc JARs and creation of
signatures required for the publication.

### camunda-repository

By default, the POM defines the `distributionManagement` section for publication of the artifacts into OSS Maven Central Repository.
Activation of this profile will overwrite the relevant properties for publication into an artifact repository maintained by Camunda.

