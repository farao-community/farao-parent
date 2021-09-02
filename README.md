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
It will provide a set of building profiles for FARAO projects. It will also define a version for juinit-jupiter and slf4j modules that are commonly used.

And for web service application you can use as a parent POM :

```
<parent>
    <artifactId>farao-parent-ws</artifactId>
    <groupId>com.farao-community.farao</groupId>
    <version>${farao.parent.version}</version>
</parent>
```
It inherits from farao-parent so it will embed the same modules. In addition it uses spring-boot-dependencies-bom in version 5.6.3. Then the main use case will be to build spring boot application in FARAO context. 

Additionally two BOMs are defined: powsybl-bom and farao-bom. It defines versions for respectively PowSyBl and FARAO modules. They can be used additionally FARAO to parent POM to use harmonized versions for these modules.

```
<dependency>
    <groupId>com.farao-community.farao</groupId>
    <artifactId>powsybl-bom</artifactId>
    <version>${farao.parent.version}</version>
    <scope>import</scope>
    <type>pom</type>
</dependency>
<dependency>
    <groupId>com.farao-community.farao</groupId>
    <artifactId>farao-bom</artifactId>
    <version>${farao.parent.version}</version>
    <scope>import</scope>
    <type>pom</type>
</dependency>
```
