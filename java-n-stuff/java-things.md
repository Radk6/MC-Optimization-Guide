# This section covers Java versions for each of the supported versions of Minecraft.

[Some benchmarks for those interested](java-benchmarks.md)

## 1.18.2+

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters but requires more RAM |

## 1.16.5

**NOTE:** Running 1.16.5 with Java 17 or 21 is only possible with [ModernFix' JVM arguments](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17). Not all mods may work though, so if you find an incompatible one, switch back to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters but requires more RAM |
| [Adoptium Java 17](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=17) | Better performance compared to Java 8 |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=8) | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java 21 is only possible with [Cleanroom Loader](https://github.com/CleanroomMC/Cleanroom). If you find a mod that doesn't work with it, report it to [their issue tracker](https://github.com/CleanroomMC/Cleanroom/issues) and use Forge with Java 8 until the issue is resolved.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters but requires more RAM |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=8) | Best mod compatibility |

## 1.7.10

**NOTE:** Running 1.7.10 with Java 21 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify).

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters but requires more RAM |

# Additional notes

If you're on a version which supports Java 21 and your PC has at least 16 GB of RAM, I'd recommend Adoptium JDK 21 with these args:

``
-XX:+UseZGC -XX:+ZGenerational
``

If you are on a lower-end device and/or you have a total of 8 GB of RAM or less, stick to GraalVM without any JVM args.
