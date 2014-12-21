# android-template

Minimalistic Android app template using Gradle.

You can use this as a starting point to create new apps from scratch.

## Structure

* `build.gradle` - Root gradle config file

* `settings.gradle` - Root gradle settings file

* `App` - Our only project in this repo

* `App/build.gradle` - Project gradle config file

* `App/src` - Main project source directory

* `App/src/main` - Main project flavour

* `App/src/main/AndroidManifest.xml` - Manifest file

* `App/src/main/java` - Java source directory

* `App/src/main/res` - Resources directory

## Building

It is recommended that you run Gradle with the `--daemon` option, as starting
up the tool from scratch often takes at least a few seconds. You can kill the
java process that it leaves running once you are done running your commands.

Tasks work much like Make targets, so you may concatenate them. Tasks are not
re-done if multiple targets in a single command require them. For example,
running `assemble install` will not compile the apk twice even though
`install` depends on `assemble`.

#### Clean

	gradle clean

#### Debug

This compiles a debugging apk in `build/outputs/apk/` signed with a debug key,
ready to be installed for testing purposes.

	gradle assembleDebug

You can also install it on your attached device:

	gradle installDebug

#### Release

This compiles an unsigned release (non-debugging) apk in `build/outputs/apk/`.
It's not signed, you must sign it before it can be installed by any users.

	gradle assembleRelease

#### Test

Were you to add automated java tests, you could configure them in your
`build.gradle` file and run them within gradle as well.

	gradle test

#### Lint

This analyses the code and produces reports containing warnings about your
application in `build/outputs/lint/`.

	gradle lint

## Further reading

* [Build System Overview](https://developer.android.com/sdk/installing/studio-build.html)

* [Gradle Plugin User Guide](http://tools.android.com/tech-docs/new-build-system/user-guide)

* [Gradle Plugin Release Notes](http://tools.android.com/tech-docs/new-build-system)
