This is an image to build [facebook fresco][1] easier.

You might start it and use the bash to clone `fresco` like:

```
docker run -i -t nginlion/android-fresco-build /bin/bash
```

In order to build `fresco` in this image, you need to edit the `build.gradle` in the root of the directory which you cloned fresco from:

```
buildscript {
    repositories {
        jcenter()
    }
    ...
```

into

```
buildscript {
    repositories {
        jcenter()
        mavenCentral() // Actually just add this line
    }
    ...
```

and then just execute `./gradlew build`, enjoy~


[1]: https://github.com/facebook/fresco
