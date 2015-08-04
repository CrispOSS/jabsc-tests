# `jabsc` Tests

This modules contains our reference examples of ABS code and how we use [`jabsc`][1] to generate Java code for them. 

The master use the latest SNAPSHOT version of the dependencies. You might need to clone and build [`jabs`][2] and [`jabsc`][1] locally and build them for this module. Or, you can change `pom.xml` for release versions of the dependencies:

* Java API for ABS: `jabs` ![Maven Central](https://img.shields.io/maven-central/v/com.github.crisposs/abs-api.svg?style=flat-square)
* ABS Compiler to Java: `jabsc` ![Maven Central](https://img.shields.io/maven-central/v/com.github.crisposs/jabsc.svg?style=flat-square)
* Maven Plugin for `jabsc` ![Maven Central](https://img.shields.io/maven-central/v/com.github.crisposs/jabsc-maven-plugin.svg?style=flat-square)

You can find ABS sources at

```
src/main/resources/abs
```

To generate Java sources integrated with Eclipse:

```bash
$ mvn eclipse:eclipse -DdownloadSources=true
```

To generate Java source with no integration with Eclipse:

```bash
$ mvn jabsc:jabsc 
```

In both of the above, the default generated Java location is:

```
target/generated-sources/jabsc
```

[1]: https://github.com/CrispOSS/jabsc
[2]: https://github.com/CrispOSS/abs-api-parent
