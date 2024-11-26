# Java benchmarks

TL;DR: If you want the most fps and shortest loading times, use GraalVM 21 (or newer) with G1GC. If you want less lag spikes/stutters as well, use GraalVM 24 with Generational ZGC

Here are benchmarks of 3 of the most popular JREs for Minecraft: GraalVM, Adoptium and Azul.

Each test was conducted in the same instance of StaTech Industry with 8 GB of RAM allocated, at 1440p with render distance set to 32 and latest Fabric Loader (0.16.8)

Test system specs:

- AMD Ryzen 7 5800X3D
- AMD Radeon RX 7800 XT
- ASRock X570 Pro⁴
- G.Skill Aegis 32 GB DDR4 3200 MT/s RAM
- Crucial P5 Plus 1 TB

## Game loading times:

![time](https://github.com/user-attachments/assets/81bff5ec-e734-4352-a77b-4edff52ded83)

As you can see, GraalVM with G1GC is fastest here. GraalVM with Generational ZGC is equal to Azul and Adoptium with G1, and both Azul and Adoptium are pretty much the same with Generational ZGC.

## ~~FPS~~

Temporarily removed

## Additional notes:

While not included in the tests, GraalVM 21 should have similar if not identical results to GraalVM 24 with G1GC, so if you're on a version which doesn't support Java 24 and want the highest fps, you can use that instead.
