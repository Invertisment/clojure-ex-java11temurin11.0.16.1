# java-11-temurin_clojure1_11_1

For some reason this fails to build with using Clojure `1.11.1` and `java-11-temurin` java.

### Reproduction
Run `lein uberjar` and it will fail with this error:

```
Exception in thread "main" java.lang.ExceptionInInitializerErrorang.Compiler.checkSpecs(Compiler.java:6

<omitted>

Caused by: java.lang.Exception: Cyclic load dependency: [ /clojure/spec/alpha ]->/clojure/walk->[ /clojure/spec/alpha ]->/clojure/main->/clojure/core/server
	... 136 more
Compilation failed: Subprocess failed (exit code: 1)
```

### Info
My local version of java is this:
```
> java --version
openjdk 11.0.16.1 2022-08-12
OpenJDK Runtime Environment Temurin-11.0.16.1+1 (build 11.0.16.1+1)
OpenJDK 64-Bit Server VM Temurin-11.0.16.1+1 (build 11.0.16.1+1, mixed mode)
```
