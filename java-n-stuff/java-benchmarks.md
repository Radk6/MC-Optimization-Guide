# Java benchmarks

Here are benchmarks of 3 of the most popular JREs for Minecraft: GraalVM, Adoptium and Zulu.

Each test was conducted on the same install of All The Mods 9, with 12288 MiB of RAM allocated. Before testing, the modpack was launched once. Loading times were taken from ModernFix' loading timer feature.

Test system specs:

- AMD Ryzen 7 5800X3D
- AMD Radeon RX 7800 XT
- ASRock X570 Pro⁴
- G.Skill Aegis 32 GB DDR4 3200 MT/s RAM
- Crucial P5 Plus 1 TB

## Game loading times:

![Game loading time (mm_ss, lower is better)](https://github.com/user-attachments/assets/b7cd6907-1862-4d20-af79-aaa410c4bb56)

GraalVM was the fastest here. Adoptium and Zulu are essentially the same across all GCs, they're pretty much withing margin of error of eachother.
