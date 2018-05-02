About
=====

Practical Scala combining OOP and FP.

## sbt

The sbt directory structure looks like:
```
src/
    main/
        resources/
            <files to include in main jar here>
        scala/
            <main Scala sources>
        java/
            <main Java sources>
    test/
        resources/
            <files to include in test jar here>
        scala/
            <test Scala sources>
        java/
            <test Java sources>
```

To run sbt, run `sbt` at the top of your project directory.

```
$ sbt
```

You can switch to another project.

```
sbt> project "New Project"
```

If you are using emacs with [ensime](http://ensime.github.io/), you can generate `.ensime` file by using `ensimeConfig` or `ensimeConfigProject`.

Note that you should make sure your `.sbt/1.0/plugins/plugins.sbt` contains `addSbtPlugin("org.ensime" % "sbt-ensime" % "2.1.0")`
(If your sbt version is 0.13, this file should be found in `.sbt/0.13/plugins/plugins`)

```
sbt> ensimeConfig

or

sbt> ensimeConfigProject
```

In case of encoutering some errors complaining about version mismatch, you can create `ensime.sbt` containig these lines.

```
ensimeIgnoreScalaMismatch in ThisBuild := true
ensimeIgnoreScalaMismatch in LocalProject("root") := true
```
