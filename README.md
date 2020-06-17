# Requirements

Make sure gradle can see the `sdk.dir` and `ndk.dir` variables. If for some reason you don't have those exposed and gradle complains,
you can add them to a `local.properties` file like so:
```
sdk.dir=/path/to/Android/Sdk
ndk.dir=/path/to/Android/Ndk/android-ndk-r20b/
```

To know if you are passing the correct path, check that each path provided contains a `platforms` folder.

# Building

> Skip linting with `-x lint` as this unnecessarily pulls in dependencies

To build debug/release apks:
`gradle build -x lint`

To automatically build and install apks:
`gradle installDebug -x lint`
