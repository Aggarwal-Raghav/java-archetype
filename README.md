# A simple archetype for Java projects

A simple `maven-archetype` for Java projects with basic style checks (using Spotless) and predefined publishing configuration for Maven central.

## Build the archetype

```
mvn clean install
```

## Generate an archetype

```bash
mvn archetype:generate \
    -DarchetypeGroupId=io.github.aggarwal-raghav \
    -DarchetypeArtifactId=java-archetype \
    -DarchetypeVersion=1.0 \
    -DgroupId=io.github.aggarwal-raghav \
    -DartifactId=test \
    -Dpackage=io.github.aggarwal_raghav \
    -B
```

> **Note on package naming:**
> My `groupId` (`io.github.aggarwal-raghav`) contains a hyphen, which is required to match my verified Maven Central namespace. However, Java package declarations cannot contain hyphens.
>
> To resolve this, always pass the `-Dpackage` flag explicitly with an underscore (as shown above). This tells Maven to use the hyphenated string for your `pom.xml` coordinates, but use the underscored string for your actual Java directories and code!

