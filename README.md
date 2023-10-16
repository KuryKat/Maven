# Maven

A Maven Repository for KuryKat's Mods

Simply add the following maven to your `build.gradle`
```gradle
repositories {
    maven {
        name = "KuryKat (GitHub)"
        url = "https://maven.pkg.github.com/KuryKat/Maven"
        credentials {
            // For your security, retrieve these from a non-public file or environment variables
            username = <GITHUB_USERNAME>
            password = <GITHUB_PERSONAL_TOKEN>
        }
    }
}
```

You can then use any published package in your build with the following
```gradle
dependencies {
    // Forge
    compileOnly fg.deobf("dev.kurykat:<mod_id>-common:<mc_version>-<mod_version>")
    runtimeOnly fg.deobf("dev.kurykat:<mod_id>-forge:<mc_version>-<mod_version>")
    
    // Fabric
    modCompileOnly "dev.kurykat:<mod_id>-common:<mc_version>-<mod_version>"
    modRuntimeOnly "dev.kurykat:<mod_id>-fabric:<mc_version>-<mod_version>"
}
```
