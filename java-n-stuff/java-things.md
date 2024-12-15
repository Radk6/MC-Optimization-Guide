# This section covers Java versions for each of the supported versions of Minecraft.

[Some benchmarks for those interested](java-benchmarks.md)

## 1.18.2+

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://github.com/graalvm/oracle-graalvm-ea-builds/releases) | Best performance and Generational ZGC support |

## 1.16.5

**NOTE:** Running 1.16.5 with Java versions newer than 8 is only possible with [ModernFix' JVM arguments](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17). Not all mods may work though, so if you find an incompatible one, switch back to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Azul Java 21](https://www.azul.com/downloads/?version=java-21-lts&package=jre#zulu) | Generational ZGC support (greatly reduces stutters but requires more RAM) |
| [Azul Java 8](https://www.azul.com/downloads/?version=java-8-lts&package=jre#zulu) | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java versions newer than 8 is only possible with [Cleanroom Loader](https://github.com/CleanroomMC/Cleanroom). If you find a mod that doesn't work with it, report it to [their issue tracker](https://github.com/CleanroomMC/Cleanroom/issues).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Azul Java 21](https://www.azul.com/downloads/?version=java-21-lts&package=jre#zulu) | Generational ZGC support (greatly reduces stutters but requires more RAM) |

## 1.7.10

**NOTE:** Running 1.7.10 with Java versions newer than 8 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify).

**NOTE 2:** GraalVM 24 build 24.1 doesn't work with 1.7.10. You must use build 23.1 

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 24](https://github.com/graalvm/oracle-graalvm-ea-builds/releases) | Best performance and Generational ZGC support |

# Additional notes

If you're on a version which supports Java 21 (or newer) and your PC has at least 16 GB of RAM, I'd recommend Adoptium JDK 21 with these args:

``
-XX:+UseZGC -XX:+ZGenerational
``

If you're on Java 24 or above, you only need ``-XX:+UseZGC`` since non-Generational ZGC was removed, making the ``-XX:+ZGenerational`` argument redundant

If you are on a lower-end device and/or you have a total of 8 GB of RAM or less, stick to GraalVM without any JVM args.
