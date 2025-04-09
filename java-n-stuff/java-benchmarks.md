# Java benchmarks

Here are some Java benchmarks I conducted in my free time.

Test system specs:

- AMD Ryzen 7 5800X3D
- AMD Radeon RX 7800 XT (Driver 25.3.1)
- ASRock X570 Pro⁴ (BIOS ver. 5.60)
- G.Skill Aegis 32 GB DDR4 3200 MT/s CL16 RAM
- Crucial P5 Plus 1 TB
- Windows 11 Pro 24H2

# Game loading times

An average of 10 runs of every Java version and garbage collector. This was tested in an [optimized StoneBlock instance](https://github.com/Radk6/MC-Optimization-Guide/blob/main/modpack-specific/packs-1.12.2.md#stoneblock). Java 8 and 21 were from Adoptium. The time was measured with VintageFix.

![time](https://github.com/user-attachments/assets/b7878deb-cb79-499c-ad3c-747e839d5664)

GraalVM 24 with G1GC performs best here, followed by GraalVM 24 with Generational ZGC. Java 8 is considerably slower than everything else.
