# This section covers Java versions for each of the supported versions of Minecraft.

[Some benchmarks for those interested](java-benchmarks.md)

## 1.18.2+

**NOTE:** While most mods should work fine with Java 24, there may be a few that won't. Currently the only one that I know of is Cobblemon, so if you're using it, switch to Java 21.

| Java | Notes |
|:---:|:---:|
| [Adoptium Java 25](https://adoptium.net/temurin/releases/?version=25&package=jre) | **Only works with Forge 1.20.1, NeoForge and Fabric**. Best performance, GenZGC and Compact Object Headers support |
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and GenZGC support |

## 1.16.5

**NOTE:** Running 1.16.5 with Java versions newer than 8 is only possible with [ModernFix' JVM arguments](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17). Not all mods may work though, so if you find an incompatible one, switch back to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?version=21&package=jre) | GenZGC support (greatly reduces stutters but requires more RAM) |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?version=8&package=jre) | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java versions newer than 8 is only possible with [Cleanroom Loader](https://github.com/CleanroomMC/Cleanroom). If you find a mod that doesn't work with it, report it to [their issue tracker](https://github.com/CleanroomMC/Cleanroom/issues).

| Java | Notes |
|:---:|:---:|
| [Adoptium Java 25](https://adoptium.net/temurin/releases/?version=25&package=jre) | Best performance, GenZGC and Compact Object Headers support |

## 1.7.10

**NOTE:** Running 1.7.10 with Java versions newer than 8 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and GenZGC support |

# JVM Arguments

Depending on the Java version, different JVM arguments are avaiable. Here's what I usually use:

| Java version | JVM arguments |
|:---:|:---:|
| Java 25 | `-XX:+UseCompactObjectHeaders -XX:+UseZGC` |
| Java 24 | `-XX:+UnlockExperimentalVMOptions -XX:+UseCompactObjectHeaders -XX:+UseZGC` |
| Java 21 | `-XX:+UseZGC -XX:+ZGenerational` |
| Java 8 | `-XX:+UseG1GC` |

**NOTE:** If you have an old CPU or less than 16 GB of total system RAM, I wouldn't recommend using ZGC. G1GC is a better option for such systems.

Brief explanation of what these arguments do:

`-XX:+UseG1GC` - Enables the G1 Garbage Collector. G1 is the default since Java 9, so the arg is only necessary on Java 8.

`-XX:+UseZGC` - Enables the Z Garbage Collector. It uses more RAM but eliminates GC-related stutters

`-XX:+ZGenerational` - Makes ZGC generational. ZGC is Generational by default since Java 23, so the arg is only necessary on Java 21

`-XX:+UseCompactObjectHeaders` - Enables Compact Object Headers. This feature reduces RAM usage.

`-XX:+UnlockExperimentalVMOptions` - Unlocks Experimental JVM Options. Necessary for using Compact Object Headers on Java 24

### Additional JVM arguments

`-Djava.locale.providers=JRE` Fixes `NNBSP` characters showing up in DateFormat outputs (e.g. near timestamps) on some versions when using Java 20 or newer.
