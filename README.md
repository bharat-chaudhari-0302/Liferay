# How To Use Liferay Gradle Node Plugin

This script is usally need when you have any build failed issue in theme regarding node and you don't want to mess with your system node versions and npm version

## Getting Started

These instructions will help you set up and configure the Node.js environment for your project using the provided Gradle script.

### Prerequisites

- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) installed
- [Gradle](https://gradle.org/install/) installed

### Installing

1. Open your project's `build.gradle` file.

2. Add the following script at the beginning of the file:

    ```groovy
    buildscript {
        dependencies {
            classpath group: "com.liferay", name: "com.liferay.gradle.plugins.node", version: "8.0.2"
        }

        repositories {
            maven {
                url "https://repository-cdn.liferay.com/nexus/content/groups/public"
            }
        }
    }

    apply plugin: "com.liferay.node"

    allprojects {
        plugins.withId("com.liferay.node") {
            node {
                nodeVersion = "14.0.0"
                npmVersion = "6.14.4"
                download = true
                global = false
            }
        }
    }
    ```

3. You can change the versions according to your need
4. Save the `build.gradle` file.
5. update your gradle.properties file and add below line
   
    ```liferay.workspace.node.package.manager=npm```
### Usage

To use the provided Gradle script for configuring the Node.js environment in your project, follow these steps:

1. Ensure you have the prerequisites installed.
   
2. Open your project's `build.gradle` file.

3. Add the provided script to the file.

4. Save the `build.gradle` file.

5. Run the following command to build your node dependent modules:

    ```bash
    ./gradlew build
    ```

Now, your project is set up with the specified Node.js and npm versions.
