# This section covers Java versions for each of the supported versions of Minecraft.

[Some benchmarks for those interested](java-benchmarks.md)

## 1.18.2+

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and Generational ZGC support |

## 1.16.5

**NOTE:** Running 1.16.5 with Java versions newer than 8 is only possible with [ModernFix' JVM arguments](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17). Not all mods may work though, so if you find an incompatible one, switch back to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?version=21&package=jre) | Generational ZGC support (greatly reduces stutters but requires more RAM) |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?version=8&package=jre) | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java versions newer than 8 is only possible with [Cleanroom Loader](https://github.com/CleanroomMC/Cleanroom). If you find a mod that doesn't work with it, report it to [their issue tracker](https://github.com/CleanroomMC/Cleanroom/issues).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and Generational ZGC support |

## 1.7.10

**NOTE:** Running 1.7.10 with Java versions newer than 8 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and Generational ZGC support |

# JVM Arguments

### Generational ZGC

If you're on a version which supports Java 21 (or newer) and your PC has at least 16 GB of RAM, I'd recommend Adoptium JDK 21 with these args:

``
-XX:+UseZGC -XX:+ZGenerational
``

Java 23 and newer only need `-XX:+UseZGC`, since it's generational by default.

If you are on a system with less than 6 cores and have 8 GB of total system RAM or less, I wouldn't recommend using ZGC.

### Compact Object Headers

Java 24 and newer support compact object headers, which can improve performance. You can enable them with these args: 

``
-XX:+UnlockExperimentalVMOptions -XX:+UseCompactObjectHeaders
``
