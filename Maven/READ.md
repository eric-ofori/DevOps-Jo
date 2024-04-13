# What is Maven and what is it used for?
- Maven is a powerful open - source build automation tool primarily used for Java projects, designed to simplify and streamline the software development process.
- It manages project dependencies, builds, and documentation generation, providing a standardized approach to project management.
- Maven employs a project object model (POM) to define project structure, dependencies, and build configurations in XML format, allowing developers to easily define project settings and      manage dependencies.

- One of the key features of Maven is its dependency management system, which automatically resolves and downloads project dependencies from remote repositories, eliminating the need for     manual dependency management.
- Maven also supports convention over configuration, providing default project layouts and build lifecycles, which can be customized to suit specific project requirements.
- Overall, Maven enhances developer productivity by automating repetitive tasks, enforcing project structure and best practices, and facilitating collaboration among team members through     standardized project configurations.

## Maven:
  - enforces specific standard to write the source code
  - uses a standardized directory/layout
  - has a project lifecyle
  - has a dependency management system
  - logic for execution at various lifecyle of project

## Main directory:
- build script ---> pom.xml
- source code ---> src/main  directory
- unit test case --> another directory

### Maven will create:
  - resource 
  - built artifact - target

### POM file - Project Object Model
- The POM.xml file is a Project Object Model (POM) file used by Apache Maven, 
  a popular build automation tool, to manage and build Java-based projects. 
- The POM.xml file contains project information, configuration details, and dependencies required for building the project.

### Here are some common elements found in a POM.xml file:
  - Project information: includes project name, description, version, and organization information.
  - Build configuration: includes information about the build process, such as source directories, target directories, and plugins used       for building the project.
  - Dependencies: lists all the external libraries and frameworks that the project depends on.
  - Plugins: lists all the Maven plugins used to build the project.
  - Profiles: allow developers to define different build configurations for different environments, such as development, testing, and         production. 

### Maven Lifecycle:
 - The phases maven passes through to create deployable artifact. A phase specific goal.

### Lifecycles:
  1. Clean: cleaning out any old build. Starting your project on a clean file structure
  2. Site/Swagger: - create java classes (byte codes [1010101010])
                    JVM will interpret the byte codes.
  3. Default:

```mvn validate``` - Maven will validate the project is correct and all necessary information is available

```mvn compile``` - Compile the source code of the project

```mvn test``` - Test the compiled source code using a unit testing framework

```mvn package``` - Package the compiled code in a deployable/distributable format e.g a  Java program will be packaged as a Java file       or a Java archive file (WAR, JAR, EAR)

```mvn install``` - Install the package into the local repository for use as a dependency in other projects locally.

```mvn deploy``` - It copies the final package to the remote repository for sharing with other developers and projects.


### Maven Repositories:
- Local repository ---> ~/.m2/repository
- Remote repository    NEXUS/Artifactory
- Central repository (on the website)
