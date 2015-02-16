# JCyclic Introduction
This API provides a simple a mechanism for finding cyclic dependencies in you classpath.
# Usage
From a test class instantiate the 'Cycles' class with a package name then call one of the methods that searches for dependencies:
```java
    @Test
    public void testForPackageCyclicDependencies() {
        ClassFinder classFinder = new ClassFinder("se.cyclic.jcycles");
        ClassDependencies classDependencies = new ClassDependencies(classFinder, "se.cyclic.jcycles");

        List<List<String>> cycles = classDependencies.getPackageCycles();
        List<List<String>> classCycles = classDependencies.getClassCycles();
    }}
```
# Coming soon
- Better performance
- Class cycles
- Exclusions for classes and packages
- Gradle plugin
  
    
