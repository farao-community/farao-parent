# farao-parent

Set of useful POM files to start FARAO related projects either libraries or applications.

For a library you can use as a parent POM :

```
<parent>
    <artifactId>farao-lib-parent</artifactId>
    <groupId>com.farao-community.farao</groupId>
    <version>1.0</version>
</parent>
```
It will handle versioning for most of PowSybl and FARAO modules. It will also define a version for juinit-jupiter module that is commonly used.

And for an application you can use as a parent POM :

```
<parent>
    <artifactId>farao-app-parent</artifactId>
    <groupId>com.farao-community.farao</groupId>
    <version>1.0</version>
</parent>
```
It inherits from farao-lib-parent so it will embed the same modules. In addition it uses spring-boot-dependencies-bom in version 5.6.3. Then the main use case will be to build spring boot application in FARAO context. 
