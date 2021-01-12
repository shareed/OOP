## Packages
- a group of similar types of classes, interfaces and sub-packages
- can be categorized in two form, built-in package and user-defined package( [built-in packages such as java, lang, awt, javax, swing, net, io, util, sql etc.](../img/javapackage.png))

#### Advantages Of Packages
- Java package is used to categorize the classes and interfaces so that they can be easily maintained.
- Java package provides access protection.
- Java package removes naming collision.

### Accessing a package from other packages
There are three ways to access the package from outside the package.
- **[packagename.*](../img/package1.png)** `import package.*;`
    - import keyword is used to make the classes and interface of another package accessible to the current package
    - all the classes and interfaces of this package will be accessible but not subpackages
- **[packagename.classname](../img/package2.png)**`import package.classname;`
    - only declared class of this package will be accessible
- **[fully qualified name](../img/package3.png)** fully qualified name
    - only declared class of this package will be accessible
    - no need to import, you need to use fully qualified name every time when you are accessing the class or interface
    - generally used when two packages have same class name e.g. java.util and java.sql packages contain Date class.

**Sequence of the program must be package then import then class**