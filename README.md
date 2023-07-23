# Plugins
The Unethical plugins are actively maintained and should be working.

The Hoot plugins are not maintained, they were created purely to experiment with and should be deemed unstable.


# To build

- Download the client from official repo (https://github.com/jbx5/devious-launcher/releases) and follow these build instructions https://github.com/open-osrs/runelite/wiki/Building-with-IntelliJ-IDEA
- refresh this gradle when its clones



 ![image](https://github.com/Salam-Boy/devious-plugins-extended/assets/139904240/132a64f7-5b61-40c7-8ee5-135d25aa4031)



- build jar on each script as needed
 ![image](https://github.com/Salam-Boy/devious-plugins-extended/assets/139904240/d4095b1d-25c8-40bd-b53f-df8861e25e37)

- add this to into build.gradle.kts inside tasks { } <- should be at the bottom
```
withType<Jar> {
            doLast {
                copy {
                    from("./build/libs/")
                    into("my plugins folder path")
                }
            }
        }
```

- plugins will be in ~/.openosrs/plugins this is where your plugin folder is!

- Enable HotSWAP:

 ![image](https://github.com/Salam-Boy/devious-plugins-extended/assets/139904240/406ba07e-361f-4a99-93ec-f92686423d35)

 You need to point the path like in the picture to your plugins folder.

 Dont forget the to add the plugin to settings.gradle.kts this will allow gradle build to detect it, the plugin must also have a corresponding gradle build file (plugin-name.gradle.kts) in the    
 source folder of the plugin!

