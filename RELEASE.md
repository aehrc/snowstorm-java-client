# How to release a Snowstorm Java Client version

This page contains the steps needed to produce and publish a Snowstorm Java Client release.

## 1. Perform the release

1. Clean check out the `main` branch
2. Run `mvn gitflow:release-start` to start the release process, this will ask for a release version
   and create a new branch for the release
7. Run `mvn gitflow:release-finish -DskipTestProject=true` to finish the release process, this will
    1. merge the release branch back into `main`
    2. tag the release in git

The above will trigger a build on the CI server for the tag which `gitflow:release-finish` will
push. This will build, test and deploy a new image to the container registry.