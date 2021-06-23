community-hub-release-parent
======================

Pom which can be inherited for community-hub maven releases defining some common release properties.
It allows deploying to two repositories simultaneously. One is a Nexus OSS server, the other one a Nexus Enterprise server.
It will deploy the artifacts at the end of the build to keep the window of failure small when talking to external systems.
