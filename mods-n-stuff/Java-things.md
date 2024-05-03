# This section covers Java and JVM arguments for each of the supported versions.

## 1.18.2+

| Java | Notes |
|:---:|:---:|
| GraalVM Java 21 | Best raw performance, shortest loading times |
| Adoptium Java 21 | Generational ZGC support, greatly reduces stutters |

## 1.16.5

**NOTE:** 1.16.5 can run with Java versions newer than 8, however not all mods can. If you encounter issues when running modded 1.16.5 with Java 17+, try [this](https://github.com/embeddedt/ModernFix/wiki/1.16---required-arguments-for-Java-17), if it doesn't work, switch to Java 8.

| Java | Notes |
|:---:|:---:|
| GraalVM Java 21 | Best raw performance, shortest loading times |
| Adoptium Java 21 | Generational ZGC support, greatly reduces stutters |
| Adoptium Java 17 | Better performance compared to Java 8 |
| Adoptium Java 8 | Best mod compatibility |

## 1.12.2

**NOTE:** Running 1.12.2 with Java 21 is only possible with Cleanroom Loader. If a mod doesn't work with it, switch to Forge and Java 8.

| Java | Notes |
|:---:|:---:|
| GraalVM Java 21 | Best raw performance, shortest loading times |
| Adoptium Java 21 | Generational ZGC support, greatly reduces stutters |
| Adoptium Java 8 | Best mod compatibility |

## 1.7.10

**NOTE:** Running 1.7.10 with Java 21 is only possible with LWJGL3ify. If a mod doesn't work with it, switch to Java 8.

| Java | Notes |
|:---:|:---:|
| GraalVM Java 21 | Best raw performance, shortest loading times |
| Adoptium Java 21 | Generational ZGC support, greatly reduces stutters |
| Adoptium Java 8 | Best mod compatibility |
