# This section covers Java versions for each of the supported versions of Minecraft.

## 1.18.2+

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters at the cost of a higher RAM requirement |

## 1.16.5

**NOTE:** 1.16.5 can run with Java versions newer than 8, however not all mods can. Make sure to follow [this](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17), but if it doesn't work, switch to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters at the cost of a higher RAM requirement |
| [Adoptium Java 17](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=17) | Better performance compared to Java 8 |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=8) | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java 21 is only possible with [Cleanroom Loader](https://github.com/CleanroomMC/Cleanroom). If you find a mod that doesn't work with it, report it to [their issue tracker](https://github.com/CleanroomMC/Cleanroom/issues) and use Forge with Java 8 until the issue is resolved.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters at the cost of a higher RAM requirement |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=8) | Best mod compatibility |

## 1.7.10

**NOTE:** Running 1.7.10 with Java 21 is only possible with [LWJGL3ify](https://modrinth.com/mod/lwjgl3ify). If a mod doesn't work with it, switch to Java 8.

| Java | Notes |
|:---:|:---:|
| [GraalVM Java 21](https://www.graalvm.org/downloads/) | Best raw performance, shortest loading times |
| [Adoptium Java 21](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=21) | Generational ZGC support, greatly reduces stutters at the cost of a higher RAM requirement |
| [Adoptium Java 8](https://adoptium.net/temurin/releases/?package=jre&arch=x64&version=8) | Best mod compatibility |

# Additional notes

If you're on a version which supports Java 21 and your PC has at least 16 GB of RAM, I'd recommend Adoptium JDK 21 with these args:

``
-XX:+UseZGC -XX:+ZGenerational
``

If you are on a lower-end device and/or you have a total of 8 GB of RAM or less, stick to GraalVM without any JVM args.
