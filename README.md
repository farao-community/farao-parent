# farao-parent

Set of useful POM files to start FARAO related projects either libraries or applications.

For a library you can use as a parent POM :

```
<parent>
    <artifactId>farao-parent</artifactId>
    <groupId>com.farao-community.farao</groupId>
    <version>${farao.parent.version}</version>
</parent>
```
It will provide a set of building profiles for FARAO projects. It will also define a version for junit-jupiter and slf4j modules that are commonly used.

And for web service application you can use as a parent POM :

```
<parent>
    <artifactId>farao-parent-ws</artifactId>
    <groupId>com.farao-community.farao</groupId>
    <version>${farao.parent.version}</version>
</parent>
```
It inherits from farao-parent so it will embed the same modules. In addition it imports spring-boot-dependencies and spring-cloud-dependencies. Then the main use case will be to build spring boot application in FARAO context. 
