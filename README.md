# Bootstrap ![Latest version](https://img.shields.io/badge/version-1.2.0-yellowgreen.svg)

Bootstrap provides common parent pom or bom to start a application quickly.

It's a personal project to make it easy to create applications conveniently, inspired by [Spring Boot](https://github.com/spring-projects/spring-boot). So it may contains many personal features and preferences, you should use it with caution.

WITHOUT WARRANTY!!!

## Modules

- **bootstrap-starter-parent**: A parent pom for maven applications to inherit. It provides some basic dependencies (mostly declaring the version) and plugin configurations. It also import some log and test dependencies by default.
- **bootstrap-dependencies**: A maven bom to declare centralized dependency versions for common jars.

## Usage

You could pick the usage as you like.

> Replace the variable `${project.latest.version}` with current project version.

### Inheriting the starter parent

Make your pom inherit **bootstrap-starter-parent** to benefit of the dependency and plugin management:

```xml
<parent>
    <groupId>io.github.xkniu.bootstrap</groupId>
    <artifactId>bootstrap-starter-parent</artifactId>
    <version>${project.latest.version}</version>
</parent>
```

### Use as a maven BOM

If you don't like inheriting a parent pom, just use **bootstrap-dependencies** as a BOM to benefit of the dependency management (but not the plugin management):

```xml
<dependencyManagement>
     <dependencies>
        <dependency>
            <groupId>io.github.xkniu.bootstrap</groupId>
            <artifactId>bootstrap-dependencies</artifactId>
            <version>${project.latest.version}</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## License

It's a open project released under the MIT License, feel free to use it.
