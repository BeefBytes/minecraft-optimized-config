# 📚 About
Optimized Minecraft server configs ready for production use. All of the modifications were made following guides and best practices.

- https://github.com/YouHaveTrouble/minecraft-optimization
- https://docs.papermc.io/paper/aikars-flags
- https://www.spigotmc.org/threads/guide-server-optimization%E2%9A%A1.283181 (outdated)

It is recommended to use Purpur due to further optimization and the sheer amount of available options, which may replaces a lot of additional plugins.

# 🏗️ Deployment

Pick one of the provided Minecraft versions and copy the contents of the folder into root of your Minecraft server. 

## Purpur
Download Purpur from: https://purpurmc.org

## Recommended JVM Startup Flags
```
java -Xms10G -Xmx10G -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 -Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true -jar paper.jar --nogui
```
Source: https://docs.papermc.io/paper/aikars-flags

## Other Recommendations
- Pregenerate world using Chunky: https://www.spigotmc.org/resources/chunky.81534
- Use Spark as performance profiler: https://spark.lucko.me/ (Spark is already built in if using Purpur)