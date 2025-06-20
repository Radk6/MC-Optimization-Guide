# This section covers Java versions for each of the supported versions of Minecraft.

[Some benchmarks for those interested](java-benchmarks.md)

## 1.18.2+

**NOTE:** While most mods should work fine with Java 24, there may be a few that won't. Currently the only one that I know of is Cobblemon, so if you're using it, switch to Java 21.

| Java | Notes |
|:---:|:---:|
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
| [GraalVM Java 25](https://github.com/graalvm/oracle-graalvm-ea-builds/releases) | Best performance, GenZGC and Compact Object Headers support |

## 1.7.10

**NOTE:** Running 1.7.10 with Java versions newer than 8 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://www.graalvm.org/downloads/) | Best performance and GenZGC support |

# JVM Arguments

### DateFormat Fix

For versions 11w49a-23w17a, on Java 20 and newer, a NNBSP (Narrow No-Break Space) character can show up in DateFormat outputs.

This will render as a dotted box with surrounding the text "NNBSP" and will appear near timestamps (most commonly).

To fix this add the argument:

``
-Djava.locale.providers=JRE
``

### Generational ZGC (GenZGC)

If you're on a version which supports Java 21 or newer and your PC has at least 16 GB of RAM, I'd recommend using GenZGC, as it can greatly reduce stutters. You can enable it with these args:

For Java 21 and 22:

``
-XX:+UseZGC -XX:+ZGenerational
``

For Java 23 and newer: 

``
-XX:+UseZGC
``

If you are on a system with less than 6 cores and have 8 GB of total system RAM or less, I wouldn't recommend using ZGC.

### Compact Object Headers

Java 24 and newer support compact object headers, which can reduce memory usage, loading times and even increase fps. You can enable them with these args: 

``
-XX:+UnlockExperimentalVMOptions -XX:+UseCompactObjectHeaders
``

However, keep in mind that on Java 24 it comes with a speed penalty (eg. slightly longer loading times). In Java 25 this won't be the case, however not many Minecraft versions work with Java 25 yet.
