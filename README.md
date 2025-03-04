# RedLib
RedLib is a Spigot plugin development library, designed to make your life easier and soothe the pain points of plugin development. Below, find instructions for the various components of RedLib.

Support Discord: https://discord.gg/agu5xGy2YZ

# Installation for Development

RedLib is a standalone plugin, but can also be used as a shaded dependency if you do not want to distribute RedLib directly. To use it as a plugin dependency, you must add it as a dependency in your plugin.yml:

```yaml
depend: [RedLib]
```

To get the jar, either download it from the releases tab either here on [GitHub](https://github.com/Redempt/RedLib/releases) or on [Spigot](https://www.spigotmc.org/resources/redlib.78713/), or [build it locally](https://github.com/Redempt/RedLib#build-locally).

## With Jitpack:

Gradle:

```groovy
repositories {
        maven { url 'https://jitpack.io' }
}

```

```groovy
dependencies {
        compileOnly 'com.github.Redempt:RedLib:Tag'
}
```

Replace `Tag` with a release tag for RedLib. Example: `6.0`. You can also use `master` as the tag to get the latest version, though you will have to clear your gradle caches in order to update it.

To shade RedLib, change the dependency from `compileOnly` to `implementation`, and install the [gradle shadow plugin](https://github.com/johnrengelman/shadow).

Maven:

```xml
<repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
</repository>
```

```xml
<dependency>
        <groupId>com.github.Redempt</groupId>
        <artifactId>RedLib</artifactId>
        <version>Tag</version>
        <scope>provided</scope>
</dependency>
```
Replace `Tag` with a release tag for RedLib. Example: `6.0`. You can also use `master` as the tag to get the latest version, though you will have to clear your maven caches in order to update it.

To shade RedLib, change the scope from `provided` to `compile`.

## Build locally:

For Windows, use Git Bash. For Linux or OSX, just ensure you have Git installed.Navigate to the directory where you want to clone the repository, and run:

```
git clone https://github.com/Redempt/RedLib
cd RedLib
./gradlew jar
```

After running these commands, the jar will be at `build/libs/RedLib.jar`.
You may also need to add the jar to your classpath. After that, you should be good to go!

# Usage

For info on how to use RedLib, please see the [wiki](https://github.com/Redempt/RedLib/wiki).
