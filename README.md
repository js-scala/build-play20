These scripts build Play 2.0.2 (and its Scala dependencies) with a local
build of Scala-Virtualized, as required for
[play-js-validation](http://github.com/namin/play-js-validation)
and the [js.scala samples](http://github.com/js-scala/samples).

### Setup

1. Locally deploy [Scala-Virtualized](http://github.com/namin/scala/tree/js) with the following commands:
  * `ant fastdist && ant distpack`
  * `(cd dists/maven/latest; ant deploy.release.local)`

2. Export the `SCALA_VIRTUALIZED_VERSION` environment variable to point
   to your locally released Scala-Virtualized version. You can find
   which versions you have locally released with the command
   * `ls -t1 ~/.m2/repository/org/scala-lang/scala-compiler | egrep -v xml`

3. Run `./build-play.sh`.
  * In case of problems with sbt's compiler interface, run this [script](https://gist.github.com/1643715).
