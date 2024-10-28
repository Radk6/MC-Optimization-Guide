# Java benchmarks

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

## FPS

![fps](https://github.com/user-attachments/assets/88ce06e0-0a11-408d-9da6-9d2161d27c18)

This chart shows max fps. GraalVM comes out on top, regardless whether G1GC or Generational ZGC is used. Adoptium and Azul are within margin of error with G1GC, followed by Azul with Generational ZGC. Adoptium with Generational ZGC seems to work much worse than all of the others.
