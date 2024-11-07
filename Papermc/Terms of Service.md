 [![PaperMC](/data/assets/logo/paperlogo512.png)](https://forums.papermc.io/)[![PaperMC](/styles/io/images/uix-brandmark.png)](https://forums.papermc.io/)

 [](https://papermc.io/search/ "Search")

[](https://papermc.io/search/ "Search")

### Search

Search titles only

By: 

Search [Advanced search…](https://papermc.io/search/)

Search titles only

By: 

Search [Advanced…](https://papermc.io/search/)

 [![PaperMC](/data/assets/logo/paperlogo512.png)](https://forums.papermc.io/)[![PaperMC](/styles/io/images/uix-brandmark.png)](https://forums.papermc.io/)

* [Home](https://papermc.io/)
    
    [What's new](https://papermc.io/whats-new/) [Latest activity](https://papermc.io/whats-new/latest-activity) [Authors](https://papermc.io/home/authors/)
    
* [Forums](https://papermc.io/forums/)
    
    [New posts](https://papermc.io/whats-new/posts/) [Search forums](https://papermc.io/search/?type=post)
    
* [What's new](https://papermc.io/whats-new/)
    
    [New posts](https://papermc.io/whats-new/posts/) [New profile posts](https://papermc.io/whats-new/profile-posts/) [Latest activity](https://papermc.io/whats-new/latest-activity)
    
* [Members](https://papermc.io/members/)
    
    [Registered members](https://papermc.io/members/list/) [Current visitors](https://papermc.io/online/) [New profile posts](https://papermc.io/whats-new/profile-posts/) [Search profile posts](https://papermc.io/search/?type=profile_post)
    
* [Plugins](https://hangar.papermc.io/)
    
* [Docs](https://docs.papermc.io/)
    
* [Downloads](https://papermc.io/downloads)
    
* [Discord](https://discord.gg/papermc)
    

[Log in](https://papermc.io/login/)

[Register](https://papermc.io/register/)

 [](https://papermc.io/search/ "Search")

[](https://papermc.io/search/ "Search")

### Search

Search titles only

By: 

Search [Advanced search…](https://papermc.io/search/)

Search titles only

By: 

Search [Advanced…](https://papermc.io/search/)

[Toggle sidebar](javascript:; "Sidebar")

Menu

Install the app

Install

JavaScript is disabled. For a better experience, please enable JavaScript in your browser before proceeding.

You are using an out of date browser. It may not display this or other websites correctly.  
You should upgrade or use an [alternative browser](https://www.google.com/chrome/).

[Announcement 1.21](https://papermc.io/threads/1-21.1221/)
----------------------------------------------------------

Jun **14**

* [Jun 14, 2024](https://papermc.io/threads/1-21.1221/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 10,148
* 2

### The 1.21 Update​

Stable Paper and Velocity 1.21 builds have been released! As always, **backups are absolutely mandatory**. **After upgrading your world to 1.21,** **you cannot downgrade back to a lower version!**  
  
We would like to thank everyone that worked on this update:  

* [4drian3d](https://github.com/4drian3d) and [Gerrygames](https://github.com/Gerrygames) for their work on Velocity
* [electronicboy](https://forums.papermc.io/members/2/) - [https://github.com/sponsors/electronicboy](https://github.com/sponsors/electronicboy)
* [jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla](https://github.com/sponsors/jpenilla)
* [kennytv](https://forums.papermc.io/members/5/)
* [lynxplay](https://forums.papermc.io/members/32/) - [https://github.com/lynxplay](https://github.com/lynxplay)
* [Lulu13022002](https://github.com/Lulu13022002)
* [Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [Ollie](https://github.com/sponsors/olijeffers0n) for his work on our docs
* [Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* and finally tal5, Dawon, yannicklamprecht and Doc94 for additional help!

If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

### spark profiler inclusion in Paper​

Thanks to riley and Luck, Paper now bundles [spark](https://spark.lucko.me/) as its main profiler for diagnosing causes of lag. Timings is now disabled by default and will be entirely removed at a later date, possibly with 1.22. As a developer, please make sure you remove any custom `Timing` uses by then. You can see our [docs page](https://docs.papermc.io/paper/profiling) as well as the [GitHub Discussions page](https://github.com/PaperMC/Paper/discussions/10565) for more details and also provide feedback there.  
  

### Configuration changes​

The `disable-teleportation-suffocation-check` config option is now gone, as this check no longer exists in vanilla. We have also changed a number of default configuration values to improve the gameplay experience:  

* `merge-radius.exp`: `3`\->`-1`(disabled). vanilla has its own less aggressive merging logic, but generally xp orbs were not a large performance concern; otherwise we might instead offer new options to change vanilla’s merge logic
* `merge-radius.item`: `2.5`\->`0.5`, reflecting the vanilla default, since the increased value was often seen as disruptive. If you expect large number of the same item types to be lying around close to one another, you can increase this again
* `entity-activation-range.raider`: `48`\->`64`
* Various values under `entity-tracking-range` have been increased to make sure you can actually see monsters and players attacking you from farther away (e.g. no longer running into invisible ghasts shooting at you in the nether. Note that this does not affect ticking, only whether they are sent to a player)
    * players: `48`\->`128`
    * animals: `48`\->`96`
    * monsters: `48`\->`96`
    * misc: `32`\->`96`

### Slower than usual startup​

In 1.20.5/6, Spigot has made additions to their plugin rewriting that resulted in poor startup performance, adding multiple seconds to each individual larger plugin. This has unfortunately been made slightly worse again in 1.21.¹  
  
We have already mildly improved on it and are working on reducing it by as much as possible, but in the meantime you can work around it by disabling the cross-version compatibility measures by either optionally using [Paper's plugin loader](https://docs.papermc.io/paper/dev/getting-started/paper-plugins) as a developer, or by using the [**`paper.disableOldApiSupport` startup flag**](https://docs.papermc.io/paper/reference/system-properties#paperdisableoldapisupport). **However, the flag will only work if all of your plugins are built against the latest API version.**  
  

### 'Done'-message changes​

The final `Done (7.392s)! For help, type "help"` message now shows the time from when the Minecraft server initially bootstrapped. Previously, it was in a kind of weird spot where it only tracked world loading, plugins, and a few other parts of server startup. We have also reinstated vanilla's original `Done preparing level` message next to the total startup time.  
  

### The .paper-remapped directory​

As per the last announcement, we now use Mojang mappings at runtime and thus have to remap plugins that might still be using Spigot's mess of mappings. The `.paper-remapped` folder in the plugin directory caused a bit of confusion, so here's what it does: It stores the remapped plugin jars as well as a cached server jar, so that all of these don't have to be processed during every single server startup. The folder is automatically cleaned up, so you don't need to (and generally shouldn't) touch it.  
  

* * *

  
For developers  
In case you skipped the 1.20.5/6 update, make sure to read [its announcement on Mojang mappings use at runtime and our new Brigadier command API](https://forums.papermc.io/threads/paper-velocity-1-20-6.1152/).  
  

### Attribute modifiers​

Attribute modifiers no longer have a name and uuid and instead make use of a single string key as its identifier. The old constructors and methods are unusable as of now, only the Paper-added get/removeModifier via uuids have had a temporary compatibility measure put in. If you are using this API, make sure to move to their replacements as soon as possible.  
  

### Removed chunk gen delegation and regeneration methods​

Our vanilla chunk gen delegation API already broke with almost every major update and this one is no exceptions. Together with the regenerateChunk method, their implementation is no longer feasible due to how hard-coupled and stateful a lot of the handling has become. The only way to properly regenerate chunks with structures and everything else attached is to generate a world with the same seeds and to copy over those chunks.  
  

### ItemStack and ItemMeta (again)​

The ItemStack class within the API module no longer holds its method implementations directly, but instead always redirects to a held internal (Craft)ItemStack instance. This won't matter to most people, but it means that you can no longer run unit tests using the API-only ItemStack. If this affects you and you aren't already using a Minecraft testing framework, we recommend using something like [Mockbukkit](https://github.com/MockBukkit/MockBukkit) to mock a running server instance.  
  
We have added `ItemMeta#hasDamageValue` to check whether the damage item data component has been added to an item. `hasDamage` will still return whether there is a non-0 amount of damage. For resetting damage, we recommend using `resetDamage` instead of setting it to 0 to improve item comparison.  
  
There's still other issues thanks to ItemMeta clashing hard with Minecraft's new item data storage, including unfortunate but not really solvable behavioral breaks to item flags. Right now, we're still working on our improved item data component API in the background and will let you know more once it has been merged.  
  

### Other changes​

* End gateway teleportation cancellation doesn't reset the portal cooldown, so you should use `EntityPortalEnterEvent` with `PortalType.END_GATEWAY` to check for initial entries
* `Projectile#getWeapon` is now nullable

### Opportunity to change the git commit author details in Paper commits​

If you have previously contributed to our main Paper repository on GitHub and want the email or name that was used on that commit to be changed, you may use the modmail command on our Discord to tell us the new details. As per our planned [repository restructure in the future](https://github.com/orgs/PaperMC/projects/6), the current git history will be overridden, so we thought we might as well fix the details for anyone that needs it.  
  

* * *

  
¹ Here are a few examples (results will vary depending on hardware and OS), which will quickly add up the more plugins you have:  

* ViaVersion takes over two seconds longer to load (from a few hundred ms to 2.5 seconds)
* WorldEdit takes two and a half seconds longer (from about 1.5 to 4 seconds)
* CoreProtect takes a second and a half longer (on a clean setup with otherwise no measurable load time at all if rewriting is disabled)

[Continue…](https://papermc.io/threads/1-21.1221/)

[](https://papermc.io/threads/1-21.1221/)

[Announcement Paper & Velocity 1.20.6](https://papermc.io/threads/paper-velocity-1-20-6.1152/)
----------------------------------------------------------------------------------------------

May **28**

* [May 28, 2024](https://papermc.io/threads/paper-velocity-1-20-6.1152/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 8,442
* 6

### The 1.20.5/6 Update​

Stable Paper and Velocity 1.20.6 builds have been released! As always, **backups are absolutely mandatory**. **After upgrading your world to 1.20.6,** **you cannot downgrade back to a lower version!**  
  
The reason for the stable announcement arriving so late is that upstream's item handling has shown to be _incredibly_ broken after the 1.20.5 changes to items. Unfortunately, there still remain a good number of smaller issues with ItemMeta API<->vanilla conversion, but at this point we should have gotten rid of the nastier ones. In any case, please make sure to report any such issues or missing functionality [on our issue tracker](https://github.com/PaperMC/Paper/issues).  
  
We would like to thank everyone that worked on this update (a lot of people and work were needed for a minor update, once again):  
  

* [4drian3d](https://github.com/4drian3d) and [Gerrygames](https://github.com/Gerrygames) for their work on Velocity
* [electronicboy](https://forums.papermc.io/members/2/) - [https://github.com/sponsors/electronicboy](https://github.com/sponsors/electronicboy)
* [jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla](https://github.com/sponsors/jpenilla)
* [lynxplay](https://forums.papermc.io/members/32/) - [https://github.com/lynxplay](https://github.com/lynxplay)
* [Lulu13022002](https://github.com/Lulu13022002)
* [Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [Noah](https://forums.papermc.io/members/81/) - [https://github.com/sponsors/NoahvdAa](https://github.com/sponsors/NoahvdAa)
* [Ollie](https://github.com/sponsors/olijeffers0n) for his work on our docs
* [Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)

If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

### Java 21 requirement​

Minecraft 1.20.6 requires you to run Java 21. See [here](https://docs.papermc.io/misc/java-install) on how to update your installed Java version.  
  

### Item format changes​

Mojang has drastically revamped the way itemstacks store their data. While they are still serialized to raw NBT in chunk and entity files, this is no longer true for commands and storage at runtime. We have created an [**item command converter page**](https://docs.papermc.io/misc/tools/item-command-converter) ([https://docs.papermc.io/misc/tools/item-command-converter](https://docs.papermc.io/misc/tools/item-command-converter)) where you can update your commands etc. If you are a developer, see the below section on how this might affect you.  
  
Unlike vanilla/Spigot, **Paper will also automatically upgrade commands in command blocks as well as text components in signs** when upgrading from an older server version. If you for whatever reason do not wish to have these upgraded, you can use the `Paper.DisableCommandConverter` system property/startup flag. For this reason, we also highly discourage upgrading your old world with non-Paper servers.  
  
Note that the `hide-item-meta` config option has not yet been updated, but everything else should work as expected.  
  

### `spawnChunkRadius` gamerule​

Our `keep-spawn-loaded` and `keep-spawn-loaded-range` config options have been removed, as Mojang has added the `spawnChunkRadius` gamerule, serving the same function.  
  

### For Developers​

### Mojang-mapped runtime without CB package relocation​

As [announced previously](https://forums.papermc.io/threads/important-dev-psa-future-removal-of-cb-package-relocation.1106/), we have dropped Spigot's mix of partially obfuscated, partially Mojang mapped, and partially Spigot mapped runtime names of classes, methods, and fields. On top of that, we have dropped the arbitrary CraftBukkit package relocation version. Plugins compiled against the reobfuscated server will still work via magical plugin remapping that is applied once on startup, as well as reflection rewriting. However, we highly recommend [using paperweight-userdev to offer plugin jars targeting the mapped server](https://docs.papermc.io/paper/dev/userdev), even if just as a secondary jar, as it would greatly benefit the vast majority of your users (well over 80-90%).  
  
If you are _not_ using internals and thus run on a Mojang mapped server fine, you should exclude your plugin from being remapped by [adding the Mojang-mapped marker to the jar manifest](https://docs.papermc.io/paper/dev/userdev#mojang-mappings) (setting `paperweight-mappings-namespace` to `mojang`). Alternatively, you can add the entry manually in your gradle or [maven](https://maven.apache.org/plugins/maven-jar-plugin/examples/manifest-customization.html) build scripts.  
  

### Brigadier Command API​

We have finally added more powerful API to interact with Brigadier commands directly. Brigadier is the command library vanilla uses for creating and parsing commands, meaning you can add much nicer auto-completions and argument handling for your commands, although this will be most interesting for command libraries wrapping around Brigadier. Basic usage is explained [on our docs page](https://docs.papermc.io/paper/dev/commands).  
  

### ItemStack and ItemMeta​

If you were using API to modify item data, then you are _largely_ fine. Since we have long deemed moving away from raw NBT data storage inevitable, we have never added API for interacting with the underlying NBT data directly. As such, only plugins unnecessarily mutating items through internals should break. The persistent data container API is also not affected. For item serialization, we highly recommend using our [ItemStack#serializeAsBytes](https://jd.papermc.io/paper/1.20.6/org/bukkit/inventory/ItemStack.html#serializeAsBytes()) method over Spigot's config serialization, so that you can guarantee proper upgrade paths, compatibility for stored items, and better performance.  
  
ItemMeta is very much not compatible with the idea of storing any data on any item, e.g. adding durability to a book, or making stone eatable. While we have tried our best at making sure that such custom data is not lost, the API has no proper way of applying these at the moment. On top of that, a lot of Spigot API that previously assumed a specific set of hardcoded enums, such as banner patterns, break when trying to add custom ones. We currently have a [better system for this in the works](https://github.com/PaperMC/Paper/pull/10613), but it will take some more time before it is fully ready.  
  
Finally, a lot of item data now has hard limits for size and length, such as lore being limited to 256 entries - most of these you shouldn't really run into. The most notable example is player profiles (including player head profiles), where player names can no longer exceed 16 characters and are limited to printable ascii characters. We strictly enforce these everywhere, as otherwise it could lead to chunks and player data unable to be saved, as well as inventory or player info updates erroring on the client.  
  

#### `canPlaceOn` and `canBreak` break​

Another piece of broken API is our canPlaceOn and canBreak methods, as these have had major changes that can now longer accurately be represented by just a list of materials. New API for this will also be added soon.  
  

#### ItemFlag behavioral changes​

Unlike before, you can no longer set most of the hide item flags without the data in question, e.g. you need to set can\_place\_on data in order to hide it.  
  

#### That's it​

Finally, here is a closing note from our master of words, electroniccat:  

> as always, BACKUP YO SHIT, so long, and thanks for the fish
> 
> Click to expand...

[Continue…](https://papermc.io/threads/paper-velocity-1-20-6.1152/)

[](https://papermc.io/threads/paper-velocity-1-20-6.1152/)

[Announcement Announcing the end of life of Waterfall](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)
--------------------------------------------------------------------------------------------------------------------------------

Mar **26**

* [Mar 26, 2024](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 18,048
* 11

Announcing the end of life of Waterfall​
----------------------------------------

As many of you might have noticed, Waterfall hasn't received much love from our team and the great contributor community in the past years. We have also seen less and less traffic in the support channels on Discord. Additionally, Mojang is making huge investments into the core engine of the game which results in big and complicated changes to the inner workings of the game. While these changes are very welcome and we have been pushing for some of them for years, they also mean that there is a bunch of work ahead of us for adapting our projects to these changes.  
We don't think we can find enough people from our team and contributors to put that work into Waterfall anymore, we want to focus our efforts on our flagship projects Paper and Velocity. We also don't feel comfortable putting out something that doesn't live up to our standards in terms of the testing that went into it.  
That's why we decided that we want to officially announce the end of life of Waterfall.  
  

### What is changing?​

Starting today, big red angry banners will appear on the Waterfall sub-pages of our documentation site and our website. These are pointing here and act as a way to inform everybody of what is going on.  
Other than that, there will be no direct change. All documentation will still be accessible, you will still be able to download all versions of Waterfall as usual.  
What will change is that you will see even more sporadic updates. You also shouldn't count on updates to new Minecraft versions, although we aren't ruling that out at this time.  
  

### What should I do?​

Migrate to [Velocity](https://papermc.io/software/velocity)! All the knowledge the people who originally worked on Waterfall gained has been put into Velocity, a proxy solution that was built from the ground up with performance, stability and security in mind. You can learn how to get started with Velocity on our [documentation site](https://docs.papermc.io/velocity/getting-started).  
You can find plugins compatible with Velocity on [Hangar, our new plugin repository](https://hangar.papermc.io/?page=0&platform=VELOCITY&sort=-stars).  
If you encounter any issues while migrating to Velocity, feel free to post on the forums or our [Discord](https://discord.gg/papermc), we are happy to help!  
  
Please join our discord community if you have any concerns about this announcement.

[Continue…](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)

[](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)

[Announcement Important dev PSA: Future removal of CB package relocation](https://papermc.io/threads/important-dev-psa-future-removal-of-cb-package-relocation.1106/)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Mar **22**

* [Mar 22, 2024](https://papermc.io/threads/important-dev-psa-future-removal-of-cb-package-relocation.1106/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 14,752
* 12

### Future removal of CB package relocation + moving away from obfuscation at runtime​

_If you are not a developer but a server owner, this might still be important for you. Check the bottom section on what action you might have to take._  
  
**Update: This change has been put into effect in 1.20.5, make sure you test with the latest Paper 1.20.5 builds.**  
  
As already announced before, at some point in the foreseeable future, **we will remove the CraftBukkit package relocation (e.g. `v1_20_R3`). This _may_ be as soon as 1.20.5**, as we expect almost every plugin using internals to break due to major changes in vanilla anyways.  
  
Note: This also includes testing of automated remapping of plugins to make them run on Mojang mapped servers, even if a plugin is compiled against the obfuscated class and method names (if you don't use any vanilla internals, this doesn't affect you). So even if you have already fixed CB package parsing, please check whether your plugins are able to run on this jar if they are using internals (or "nms").  
  
Once these changes are present in stable Paper builds, you can expect a much better experience when using the often dreaded internals by using our [userdev](https://docs.papermc.io/paper/dev/userdev) Gradle plugin. Most notably, small Minecraft updates will no longer unconditionally break your plugins.  
  

### How to make sure your plugin does not break​

**If you reflect on CB classes**  
Easy, just **don't try to parse the package version**. The following will work on servers with _and_ without CB relocation:  

Java:

    private static final String CRAFTBUKKIT_PACKAGE = Bukkit.getServer().getClass().getPackage().getName();
    
    public static String cbClass(String className) {
        return CRAFTBUKKIT_PACKAGE + "." + className);
    }
    
    Class.forName(cbClass("entity.CraftBee"))

  
**If you try to parse the server version**  
Do **NOT** do this:  

Java:

    String craftBukkitPackage = Bukkit.getServer().getClass().getPackage().getName();
    // This is the *bad* part, including any other parsing of the version
    String version = craftBukkitPackage.substring(craftBukkitPackage.lastIndexOf('.') + 1);
    if (version.equals("v1_20_R3")) {
        // ...
    } else {
      // Unsupported
    }

Instead, use **long-standing API**:  

Java:

    // Paper method that was added in 2020
    // Example value: 1.20.4
    String minecraftVersion = Bukkit.getServer().getMinecraftVersion();
    
    // Bukkit method that was added in 2011
    // Example value: 1.20.4-R0.1-SNAPSHOT
    String bukkitVersion = Bukkit.getServer().getBukkitVersion();
    
    if (minecraftVersion.equals("1.20.4")) {
        // ...
    } else {
      // Assume latest still works, or error as unsupported
      // Alternatively for extra compatibility, check if
      // the latest package version is valid by catching
      // ClassNotFoundException with: Class.forName("org.bukkit.craftbukkit.v1_20_R3.CraftServer")
    }

The Minecraft version strings you can parse and evaluate to your heart's content. Another (less recommended) alternative is getting the server protocol version from `Bukkit.getUnsafe`.  
  

### As a server owner​

If you are running a somewhat recent server version with up-to-date plugins (!), you should also test whether your plugins are able to run on the [test server jar](https://github.com/PaperMC/testing/releases/tag/no-relocation) also linked above. **Please make sure not to use the server jar on your main servers, but to copy your plugin setup to a separate test server.**  
  
The error that plugin developers need to fix will look something like this:  

> \[11:46:19\] \[Server thread/ERROR\]: Error occurred while enabling PLUGINNAME v1 (Is it up to date?)  
> java.lang.ArrayIndexOutOfBoundsException: Index 3 out of bounds for length 3  
> at ...
> 
> Click to expand...

Alternatively, they might log an error saying you are using an unknown or unsupported server version.  
  
If any of your plugins start printing new errors like these and you have made sure that they are already up-to-date, please report the error with a link to this announcement to the relevant plugin authors.

[Continue…](https://papermc.io/threads/important-dev-psa-future-removal-of-cb-package-relocation.1106/)

[](https://papermc.io/threads/important-dev-psa-future-removal-of-cb-package-relocation.1106/)

[New Years post](https://papermc.io/threads/new-years-post.1009/)
-----------------------------------------------------------------

Dec **31**

* [Dec 31, 2023](https://papermc.io/threads/new-years-post.1009/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 26,747
* 6

Happy New Year from PaperMC!​
-----------------------------

Wishing you all a super happy New Year!  
It's been a big year at Paper! We've grown a lot and have some big changes on the horizon. Our team has yet again increased in size and become even more motivated to work towards our goal of hard forking. PaperMC is powered by the contributions from everyone, and we have made it our priority that new contributions are getting out there as soon as possible. And through that, we have seen some new faces pop up and contribute more often.  
  
This year, we merged over **475** Pull Requests from over **120** unique contributors!  
Going through each one of these PRs wouldn't be possible without you, so we are so grateful for all the bugs reported, testing done, and all the new contributors who decided to give it a shot.  
  
This year was a big team effort, and we want to thank each and every person who's been a part of it. Your ideas and hard work made PaperMC even better, and we're so excited to keep growing and improving together.  
  

### The Future​

The future is bright, we have a lot of work being done behind the scenes that we hope to be able to get out into your hands in 2024.  

#### Lifecycle API​

With our new Paper Plugins introduced this year, we introduced ways of running code much earlier before the server has started.  
Using this new Lifecycle API, we will now allow plugins to start running code on an event-based system much earlier in server initialization as well.  

Java:

     @Override
        public void onEnable() {
            final LifecycleEventManager<Plugin> lifecycles = this.getLifecycleManager();
            lifecycles.registerEventHandler(LifecycleEvents.DUMMY_STATIC.newHandler(event -> {
                final DummyResourceRegistrar registrar = event.registrar();
                System.out.println("dummy_static hook FIRST");
            }).priority(-1));
            lifecycles.registerEventHandler(LifecycleEvents.DUMMY_STATIC.newHandler(event -> {
                final DummyResourceRegistrar registrar = event.registrar();
                System.out.println("dummy_static hook FOURTH (monitor)");
            }).monitor());
            lifecycles.registerEventHandler(LifecycleEvents.DUMMY_STATIC.newHandler(event -> {
                final DummyResourceRegistrar registrar = event.registrar();
                System.out.println("dummy_static hook THIRD");
            }).priority(100));
        }

  
_See more information [here](https://gist.github.com/Machine-Maker/8e3fc6063c98e81cae7cee1ac230936f)_  
  

#### Brigadier API​

Using the Lifecycle API mentioned above, we will also support command registration through this system through brigadier. This will allow these commands to be usable in things like datapack functions.  
This API will also support adding custom serverside arguments and more, allowing a more powerful approach compared to the current Bukkit command API.  

Java:

    CommandBuilder.of(plugin, "admin")
                .then(
                    LiteralArgumentBuilder.<CommandSourceStack>literal("execute")
                        .redirect(Bukkit.getCommandDispatcher().getRoot().getChild("execute"))
                )
                .then(
                    LiteralArgumentBuilder.<CommandSourceStack>literal("signed_message").then(
                        RequiredArgumentBuilder.argument("msg", VanillaArguments.signedMessage()).executes((context) -> {
                            MessageArgumentResponse argumentResponse = context.
                            getArgument("msg", MessageArgumentResponse.class); // Gets the raw argument.
    
                            // This is a better way of getting signed messages,
                            // includes the concept of "disguised" messages.
                            argumentResponse.resolveSignedMessage("msg", context)
                                .thenAccept((signedMsg) -> {
                                    Component comp = Component.text("STATIC");
                                    context.getSource()
                                                .getBukkitSender()
                                                .sendMessage(signedMsg, ChatType.SAY_COMMAND.bind(comp));
                                });
    
                            return 1;
                        })
                    )
                ))
                .description("Cool command showcasing what you can do!")
                .aliases("alias_for_admin_that_you_shouldnt_use", "a")
                .register();

_See more information [here](https://github.com/PaperMC/Paper/pull/8235)_  
  

#### Registry Manipulation API​

We've recently introduced autogenerated API keys in our [API](https://jd.papermc.io/paper/1.20/io/papermc/paper/registry/keys/package-summary.html), and in general are closing the gap allowing us to properly implement custom type registration.  
  
In this API, we finally allow custom types to be registered **and** we allow the modification of pre-existing entries, allowing you to safely make modifications to registered vanilla types.  
  

Java:

    static final TypedKey<GameEvent> NEW_EVENT = GameEventKeys.create(Key.key("machine_maker", "best_event"));
    
    @Override
    public void bootstrap(@NotNull BootstrapContext context) {
        final LifecycleEventManager<BootstrapContext> lifecycles = context.getLifecycleManager();
    
        // registers a new handler for the prefreeze event for the game event registry
        lifecycles.registerEventHandler(RegistryEvents.GAME_EVENT.preFreeze().newHandler(event -> {
            // the RegistryView provided here is writable so you can register new objects
            event.registry().register(NEW_EVENT, builder -> {
                builder.range(2);
            });
        }));
     
        // registers a handler for the addition event
        lifecycles.registerEventHandler(RegistryEvents.GAME_EVENT.newAdditionHandler(event -> {
            // checks if the object being registered is the block open game event
            if (event.key().equals(GameEventKeys.BLOCK_OPEN)) {
                // multiplies the range by 2
                event.builder().range(event.builder().range() * 2);
            }
        }));
    }

_See more information [here](https://gist.github.com/Machine-Maker/2901c790219862ef1ad6070b8872a889)_  
  

#### Mache and Codebook​

Although not directly related to Paper's API, we also have been hard at work building a stable platform for working on the server in the future. Through Mache and Codebook, we have been able to create a stable way of deobfuscating the game in a way more friendly than before.  
[![1704062422395.png](https://forums.papermc.io/data/attachments/0/491-f609fb333f543aa96debec2aef9871f9.jpg "1704062422395.png")](https://forums.papermc.io/attachments/1704062422395-png.491/)  
  
More work than ever is being put into our tech for hard forking, and we are excited to be able to work off of some of the best tech developed for deobfuscation.  
  

### Here's to a fantastic 2024!​

[Continue…](https://papermc.io/threads/new-years-post.1009/)

[](https://papermc.io/threads/new-years-post.1009/)

[Announcement Paper & Velocity 1.20.4](https://papermc.io/threads/paper-velocity-1-20-4.998/)
---------------------------------------------------------------------------------------------

Dec **25**

* [Dec 25, 2023](https://papermc.io/threads/paper-velocity-1-20-4.998/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 8,785
* 1

### The 1.20.4 Update​

Stable Paper and Velocity 1.20.4 builds have been released! As always, **backups are absolutely mandatory**. **After upgrading your world to 1.20.4,** **you cannot downgrade back to a lower version!**  
  
We would like to thank everyone that worked on this update (a lot of people and work needed for a minor update, once again):  

* [Gerrygames](https://github.com/Gerrygames), [pkt77](https://github.com/pkt77), and [electroniccat](https://github.com/electronicboy) for their work on Velocity
* [Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [lynxplay](https://forums.papermc.io/members/32/) - [https://github.com/lynxplay](https://github.com/lynxplay)
* [jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla](https://github.com/sponsors/jpenilla)
* [Lulu13022002](https://github.com/Lulu13022002)
* [Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)

If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

### Discord Update Announcements​

From now on, instead of creating a new Discord channel for every update, we will post important milestone updates (such as the availability of experimental builds) into the new `update-announcements` channel and provide more small-stepped info in the forum channel below it. You might have to add these channels to your list via "Channels & Roles" at the top of the channel list first.  
  

### For Developers​

### New API​

With the new `sendResourcePacks` and `removeResourcePacks` methods, you can give each pack its own UUID to be individually added and removed later, which means that you can have multiple packs applied at once! The existing `setResourcePack` method will override all previous ones to retain expected behavior.  
  

### `Keyed` interface may be removed on some types​

`Keyed` provides a `NamespacedKey getKey()` to get keys for biomes, item and block types, sounds, etc. However, trim patterns and trim materials mark the first two registry based objects that do not require a key in all cases, hence the nonnull `getKey` method is not valid for these.  
  
To make your plugins future proof of such cases, please use the newly added `Registry#getKey(Object)`. While the `getKey` methods will be available until actually broken, using the method on `Registry` will make sure your plugin does not suddenly break later. Note that because of the possibility of no key existing, this method is nullable. If you are sure one will exist, you can also use the nonnull `Registry#getKeyOrThrow`.  
  

#### Hangar login/signup via GitHub, Google, or Microsoft account​

As per [the last big announcement](https://forums.papermc.io/threads/hangar-papermcs-plugin-repository.691/), we now have our own website for you to upload your Paper, Bungee, and Velocity plugins to: [https://hangar.papermc.io/](https://hangar.papermc.io/)  
If you don't feel like manually uploading your builds to it, you can also check out our hangar publish gradle plugin: [https://docs.papermc.io/misc/hangar-publishing](https://docs.papermc.io/misc/hangar-publishing)  
  
Additionally, we have prepared a little Christmas gift for all (current or future) Hangar users: You can now use your GitHub, Google or Microsoft account to login to Hangar. If you don't have an account yet, you can signup using one of these OAuth providers on [the signup page](https://hangar.papermc.io/auth/signup), if you want to link an OAuth account to your existing account you can do so in [the security settings](https://hangar.papermc.io/auth/settings/security). Note that this functionality, while thoroughly tested, is still a bit experimental and the UX of the flows and the design of the UI is still subject to change. Please send us your feedback on Discord or via [the issue tracker](https://github.com/HangarMC/Hangar/issues).

[Continue…](https://papermc.io/threads/paper-velocity-1-20-4.998/)

[](https://papermc.io/threads/paper-velocity-1-20-4.998/)

[Announcement Paper & Velocity 1.20.2](https://papermc.io/threads/paper-velocity-1-20-2.920/)
---------------------------------------------------------------------------------------------

Oct **10**

* [Oct 10, 2023](https://papermc.io/threads/paper-velocity-1-20-2.920/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 15,144
* 1

### The 1.20.2 Update​

Stable Paper and Velocity 1.20.2 builds have been released! As always, **backups are absolutely mandatory**. **After upgrading your world to 1.20.2,** **you cannot downgrade back to a lower version!**  
  
We would like to thank everyone that worked on this update (a lot of people and work needed for a minor update!):  

* [Paul19988](https://github.com/Paul19988/), [Redned235](https://github.com/Redned235), and [Gerrygames](https://github.com/Gerrygames) for their work on Velocity
* [Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [Noah](https://forums.papermc.io/members/81/) - [https://github.com/sponsors/NoahvdAa](https://github.com/sponsors/NoahvdAa)
* [lynxplay](https://forums.papermc.io/members/32/) - [https://github.com/lynxplay](https://github.com/lynxplay)
* [jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla](https://github.com/sponsors/jpenilla)
* [Lulu13022002](https://github.com/Lulu13022002)
* [MiniDigger](https://forums.papermc.io/members/15/) - [https://github.com/sponsors/MiniDigger](https://github.com/sponsors/MiniDigger)
* [Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)

If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

#### Velocity & Waterfall​

Due to larger network changes and perfectly timed holidays of a few of our devs, it took a little longer to get Velocity ready for 1.20.2. **Plugins manually sending packets will need updating**. The most notable change in user behavior here is that on server switches, the Minecraft client will now drop its current resource pack, meaning it will have to be re-sent if you want to keep it across backend servers. Velocity will re-apply the pack you set via Velocity API, but if you send it on the Paper server, you will need to do so on more than just the hub. This is unavoidable at the moment, but we're hopeful that Mojang is going to address this in a future update.  
  
While Waterfall received support for 1.20.2 pretty early on as part of BungeeCord upstream updates, its support was pretty broken for the first few days and weeks after the release and still does not properly handle the new protocol changes in some places. In general, Waterfall is unlikely to receive our full attention given that Velocity is meant to be its more performant, stable, and secure successor. In similar fashion to us retiring Travertine a while ago, the same will happen to Waterfall in the future. For now though, we will continue providing you with upstream updates at the very least.  
  

### For Developers​

#### **CraftBukkit package relocation**​

This is **very** important if you for whatever reason use reflection to either  

* parse the relocated package version.
* call CB internals.

**At some point in the future**, we will only provide jars **without relocation**, given it is a nonsensical practice resulting in unavoidably bad code design and unexpected incompatibilities in a large number of plugins. While we will be able to automagically remap both direct and reflective calls to the relocated package, **parsing the package version is not supported and WILL break at some point in the future**. The changes we have planned should make working with internals a lot easier, since we recognize that _sometimes_ (though not as often as some might think) there is no better alternative.  
  
**If you reflect on CB classes**  
Easy, just **don't try to parse the package version**. The following will work on servers with _and_ without CB relocation:  

Java:

    private static final String CRAFTBUKKIT_PACKAGE = Bukkit.getServer().getClass().getPackage().getName();
    
    public static String cbClass(String clazz) {
        return CRAFTBUKKIT_PACKAGE + "." + clazz);
    }
    
    Class.forName(cbClass("entity.CraftBee"))

  
**If you try to parse the server version**  
Do **NOT** do this:  

Java:

    String craftBukkitPackage = Bukkit.getServer().getClass().getPackage().getName();
    // This is the *bad* part, including any other parsing of the version
    String version = craftBukkitPackage.substring(craftBukkitPackage.lastIndexOf('.') + 1);
    if (version.equals("v1_20_R1")) {
        // ...
    } else {
      // Unsupported
    }

Instead, use **long-standing API**:  

Java:

    // Paper method that was added in 2020
    // Example value: 1.20.1
    String minecraftVersion = Bukkit.getServer().getMinecraftVersion();
    
    // Bukkit method that was added in 2011
    // Example value: 1.20.1-R0.1-SNAPSHOT
    String bukkitVersion = Bukkit.getServer().getBukkitVersion();
    
    if (minecraftVersion.equals("1.20.1")) {
        // ...
    } else {
      // Assume latest still works, or error as unsupported
      // Alternatively for extra compatibility, check if
      // the latest package version is valid by catching
      // ClassNotFoundException with: Class.forName("org.bukkit.craftbukkit.v1_20_R1.CraftServer")
    }

The Minecraft version strings you can parse and evaluate to your heart's content. Another (less recommended) alternative is getting the server protocol version from `Bukkit.getUnsafe`.  
  

#### **Future changes regarding API enums**​

Enums such as Biome implementing the Keyed interface will be converted to classes with public static final objects at some point. While some backwards compatibility will be provided, **please try to avoid the use of switch statements, EnumMap and EnumSet on these, including the Material enum**.  
  

#### **1.20.2 API changes**​

With the protocol changes comes the ability to send a resource pack before the player has even joined the world, making previously required precautions like resource pack servers unnecessary. Finally, it also sends its client settings (including the language) before this as well. Due to heavy work on the update itself, we haven't yet been able to add API for this, but we will let you know once it is added!  
  

#### Hangar​

As per [the last big announcement](https://forums.papermc.io/threads/hangar-papermcs-plugin-repository.691/), we now have our own website for you to upload your Paper, Bungee, and Velocity plugins to: [https://hangar.papermc.io/](https://hangar.papermc.io/)  
If you don't feel like manually uploading your builds to it, you can also check out our hangar publish gradle plugin: [https://docs.papermc.io/misc/hangar-publishing](https://docs.papermc.io/misc/hangar-publishing)

[Continue…](https://papermc.io/threads/paper-velocity-1-20-2.920/)

[](https://papermc.io/threads/paper-velocity-1-20-2.920/)

[Announcement Paper & Velocity 1.20(.1)](https://papermc.io/threads/paper-velocity-1-20-1.783/)
-----------------------------------------------------------------------------------------------

Jun **11**

* [Jun 11, 2023](https://papermc.io/threads/paper-velocity-1-20-1.783/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 13,971
* 9

### The 1.20(.1) Update​

We’re happy to announce that initial builds for Paper 1.20 have been released. As always, **backups are absolutely mandatory**. **After upgrading your world to 1.20,** **you cannot downgrade back to a lower version!**  
  
We would like to thank everyone that worked on this update:  

* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [@Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [@lynxplay](https://forums.papermc.io/members/32/) - [https://github.com/lynxplay](https://github.com/lynxplay)
* [@Noah](https://forums.papermc.io/members/81/) - [https://github.com/sponsors/NoahvdAa](https://github.com/sponsors/NoahvdAa)
* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)

Next to those people, you can find links to support them individually. If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

### For Developers​

**Future changes regarding API enums**  
Enums such as Biome implementing the Keyed interface will be converted to classes with public static final objects at some point. While some backwards compatibility will be provided, **please try to avoid the use of switch statements, EnumMap and EnumSet on these, including the Material enum**.  
  
**1.20 API changes**  
With 1.20, there is of course new API for the new features. Some notable breaks are:  

* `SmithingRecipe` has been replaced with `SmithingTrimRecipe` and `SmithingTransformRecipe`
* `InventoryType.SMITHING` now uses 1.20's new smithing table interface
* `Sign#isEditable()` has been deprecated in favor of a new method called `isWaxed`, same for its setter

  
**API scheduled for removal**  
A bunch of old API has been scheduled for removal in 1.21, so please make sure you remove usages of these in your plugins:  

* [AsyncChatDecorateEvent#isPreview()](https://jd.papermc.io/paper/1.19/io/papermc/paper/event/player/AsyncChatDecorateEvent.html#isPreview())
* [PlayerLocaleChangeEvent](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/event/player/PlayerLocaleChangeEvent.html)
* [PlayerInitialSpawnEvent](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/event/player/PlayerInitialSpawnEvent.html)
* [WorldBorder#isInBounds(Location)](https://jd.papermc.io/paper/1.19/org/bukkit/WorldBorder.html#isInBounds(org.bukkit.Location))
* [EntityTransformedEvent](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/event/entity/EntityTransformedEvent.html)
* [ItemStackRecipeChoice](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/inventory/ItemStackRecipeChoice.html)
* [HeightmapType](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/HeightmapType.html)
    * All associated methods in Location and World
* All deprecated or removed GoalKeys in [VanillaGoal](https://jd.papermc.io/paper/1.19/com/destroystokyo/paper/entity/ai/VanillaGoal.html)
* [StructureLocateEvent](https://jd.papermc.io/paper/1.19/io/papermc/paper/event/world/StructureLocateEvent.html) (not the new StructuresLocateEvent)
* Duplicate Effects
* World API
    * [World#hasSkylight()](https://jd.papermc.io/paper/1.19/org/bukkit/World.html#hasSkylight())
    * [World#hasBedrockCeiling()](https://jd.papermc.io/paper/1.19/org/bukkit/World.html#hasBedrockCeiling())
    * [World#doesBedWork()](https://jd.papermc.io/paper/1.19/org/bukkit/World.html#doesBedWork())
    * [World#doesRespawnAnchorWork()](https://jd.papermc.io/paper/1.19/org/bukkit/World.html#doesRespawnAnchorWork())

### Hangar​

As per [the last big announcement](https://forums.papermc.io/threads/hangar-papermcs-plugin-repository.691/), we now have our own website for you to upload your Paper, Bungee, and Velocity plugins to. There have been little updates in the past few weeks due to us being busy with other projects, including Paper, but rest assured we'll keep working on it! [https://hangar.papermc.io/](https://hangar.papermc.io/)  
  

### Experimental channel for builds​

Our downloads API has different channels to distinguish builds - right now between `experimental` and `default`. For future updates, we will no longer provide any early experimental builds on Discord, instead using the `experimental` channel in our downloads API. **This means that you will need to distinguish between channels in your scripts to avoid getting highly experimental and potentially breaking versions. Please adjust your download scripts accordingly.** Experimental builds marked as such will be available to download on our homepage as well.

[Continue…](https://papermc.io/threads/paper-velocity-1-20-1.783/)

[](https://papermc.io/threads/paper-velocity-1-20-1.783/)

[Announcement Hangar - PaperMC's Plugin Repository](https://papermc.io/threads/hangar-papermcs-plugin-repository.691/)
----------------------------------------------------------------------------------------------------------------------

Apr **20**

* [Apr 20, 2023](https://papermc.io/threads/hangar-papermcs-plugin-repository.691/)
* [MiniDigger](https://papermc.io/home/authors/minidigger.15/)

* 6,627
* 1

Once again, we have another exciting announcement for you, this time about PaperMC's own site for uploading and downloading Paper, Velocity, and Waterfall plugins, called [**Hangar**](https://hangar.papermc.io/)! The main reason we started working on this is to finally provide a centralized place for Paper and Velocity plugins. Compared to the Spigot forums, Hangar allows you much more control over your resource in terms of:  

* adding other authors to your project,
* creating organizations with projects under them,
* managing roles per project or per organization (such as editor or developer)
* combined releases with multiple jars or external links per platform,
* customizable release channels (such as beta or snapshot),
* [a proper, documented API](https://hangar.papermc.io/api-docs) to upload and download plugins ([OpenAPI yaml](https://hangar.papermc.io/v3/api-docs.yaml)),
* creating multiple project description/wiki pages,
* selecting compatibility with minor Minecraft versions as well as specific Velocity versions,
* additional tags to mark a plugin as an addon, a library, or Folia compatible,
* a secure account system with support for modern multi factor authentication standards like TOTP and WebAuthN (YubiKeys are supported!)

... and more. As Hangar is still in beta, we intend on adding a lot more features and quality of life changes, such as the ability to set notifications per release channel and creating draft releases. You can follow up on our current plans in the Hangar roadmap project: [https://github.com/orgs/HangarMC/projects/1/views/14](https://github.com/orgs/HangarMC/projects/1/views/14). There are of course other such resource sites already, such as CurseForge and Modrinth, however, we have made Hangar specifically with Paper and Velocity plugins in mind, so that you can have the best experience looking for plugins or uploading them to Hangar.  
  
We have already made a Gradle plugin you can use to automatically upload new version releases, which you can find here with examples provided: [https://github.com/HangarMC/hangar-publish-plugin](https://github.com/HangarMC/hangar-publish-plugin) - so the only thing that stands between you and your first uploaded version is creating an account and a project on Hangar!  
  
Additionally, for developers who published to the Spigot forums before, we created an importer for that! You can find it here [https://hangar.papermc.io/tools/importer](https://hangar.papermc.io/tools/importer). It will attempt to import the description and convert it to Markdown, set the project avatar and basic settings such as the category to make it as easy as possible for you to adopt Hangar for your projects. Do note however that you will have to upload your versions manually after you imported your projects!  
  
If you happen to find any bugs, you can report them on our issue tracker: [https://github.com/HangarMC/Hangar/issues](https://github.com/HangarMC/Hangar/issues).  
If you want a testing grounds for the API, please use [our staging instance](https://hangar.papermc.dev/).  
  

### Otherwise we hope to see you and your plugins on **Hangar** over at [https://hangar.papermc.io/](https://hangar.papermc.io/)​

  
Let me end this post with a bit of a personal note:  
Hangar was born out of a discussion on the Papers Discord/IRC channel, after being annoyed by existing platforms, almost 3 years ago.  
First it was a from-scratch project, then we forked Ore (the platfrom repository made by the Sponge project), then we rewrote Ore's frontend, then we rewrote the backend, then we rewrote the frontend, again. It has been quite a wild ride, with many ups and downs.  
The lowest point was December last year: We weren't getting anywhere, I thought everything we had sucked, we were exploring alternatives internally, I started modifying existing software for our needs. Basically, I was ready to give up. In the end, we decided to not go that route, the Paper team assured me that what we had at that time was already better than other existing solutions and so I pushed through all that together with Kenny, without whom I would have never be able to do that.  
So I'll end with thanking him, Machine\_Maker, AlessioGr, mdcfe and all the other contributors, the Paper team, the people on the Hangar Discord, the plugin developers who where invited as early adopter and everybody else who tested Hangar over the years and provided valuable feedback, and generally everybody in the Paper community who pinged me daily to remind me that Hangar means something to them: You were annoying as heck, but I am glad you did it.  
And now everybody go sign up!

[Continue…](https://papermc.io/threads/hangar-papermcs-plugin-repository.691/)

[](https://papermc.io/threads/hangar-papermcs-plugin-repository.691/)

[Announcement Paper & Velocity 1.19.4](https://papermc.io/threads/paper-velocity-1-19-4.680/)
---------------------------------------------------------------------------------------------

Mar **15**

* [Mar 15, 2023](https://papermc.io/threads/paper-velocity-1-19-4.680/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 8,398
* 3

### The 1.19.4 Update​

Paper 1.19.4 and Velocity with 1.19.4 support are now available on our website! As always, we recommend that you make a backup of your server before upgrading. Remember that you cannot downgrade your Paper server after doing the update.  
  
Despite only being a minor version, once again, quite a bit of work has gone in the update. We would like to thank the following people for their work on the update process:  

* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)
* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [Gerrygames](https://github.com/Gerrygames) (for help with Velocity)

  

### Experimental Channel for Builds​

**This is the last warning regarding the experimental channel on our downloads API before we will publish experimental builds of the next major Minecraft release (1.20) to the downloads API instead of as separate builds while still considered unstable.**  
  
For future updates, we will no longer provide any early experimental builds on Discord, instead using the experimental channel in our downloads API. **This means that you will need to distinguish between channels in your scripts to avoid getting highly experimental and potentially breaking versions. Please adjust your download scripts accordingly.** Experimental builds marked as such will be available to download on our homepage as well.  
  

### Website Overhaul​

Our new website is now live at [https://papermc.io/](https://papermc.io/)! Cubxity has been working on this with us for a while, and we're happy to finally be able to replace our old site that has been an annoyance to maintain for quite some time. Feedback is of course appreciated, the same applies to code contributions: [https://github.com/PaperMC/website](https://github.com/PaperMC/website)  
  

### For Developers​

**API changes**  

* Experimental features have representation in API, but are marked as experimental and are subject to changes, as Mojang might still change them in major ways before they land in 1.20. See [here](https://www.minecraft.net/en-us/article/testing-new-minecraft-features/feature-toggles-java-edition) for more information on experimental features in general.
* Using adventure's `ClickEvent.callback` methods, you can now easily register message click event callbacks without having to keep track of them yourself. This code for example will create a click event to open a book that can be used for up to 2 minutes and has 5 uses:  
    
    Java:
    
        ClickCallback.Options options = ClickCallback.Options.builder()
            .lifetime(Duration.ofMinutes(2))
            .uses(5)
            .build();
        ClickEvent clickEvent = ClickEvent.callback(
            audience -> audience.openBook(book),
            options
        );
        player.sendMessage(Component.text().content("Click me!").clickEvent(clickEvent));
    
    In these methods, you can also make sure only a certain player/players with a certain permission are allowed to use the callback.
* `LivingEntity#setHurtDirection` throws an UnsupportedOperationException if called on a non-player
* `HopperMinecart#setCooldown` and getCooldown throw UnsupportedOperationException

  
**WIP registry modification API**  
Machine Maker has been working on API to be able to modify certain Minecraft registries, including damage events. Before merging it, we would like to gather a last round of community feedback on it: [https://github.com/PaperMC/Paper/pull/8920](https://github.com/PaperMC/Paper/pull/8920)  
  
Additionally there is a second pull request to add API for modifying tags, used by the client in a lot of different ways, including knowing which blocks are climbable and which tool you can use to faster dig a block: [https://github.com/PaperMC/Paper/pull/9002](https://github.com/PaperMC/Paper/pull/9002)  
  
**Future changes regarding API enums**  
Enums such as Biome implementing the Keyed interface will be converted to classes with public static final objects at some point. While some backwards compatibility will be provided, please try to avoid the use of switch statements, EnumMap and EnumSet on these.

[Continue…](https://papermc.io/threads/paper-velocity-1-19-4.680/)

[](https://papermc.io/threads/paper-velocity-1-19-4.680/)

[Announcement Paper & Velocity 1.19.3](https://papermc.io/threads/paper-velocity-1-19-3.592/)
---------------------------------------------------------------------------------------------

Dec **11**

* [Dec 11, 2022](https://papermc.io/threads/paper-velocity-1-19-3.592/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 13,825
* 1

### The 1.19.3 Update​

Paper 1.19.3 and Velocity with 1.19.3 support are now available on our website! Even though Paper is deemed stable, we still recommend that you make a backup of your server before upgrading. Remember that you cannot downgrade your Paper server after doing the update.  
  
Despite only being a minor version, quite a bit of work has gone in the update. We would like to thank the following people for their work on the update process:  

* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)
* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [@Noah](https://forums.papermc.io/members/81/) - [https://github.com/sponsors/NoahvdAa](https://github.com/sponsors/NoahvdAa)
* [@jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla/](https://github.com/sponsors/jpenilla/)
* [FiXed](https://github.com/CoreyShupe) (for his work on Velocity)
* [@electronicboy](https://forums.papermc.io/members/2/) - [https://paypal.me/ShaneFreeder](https://paypal.me/ShaneFreeder)

  

### Experimental Features​

As explained in a [minecraft.net article](https://www.minecraft.net/en-us/article/testing-new-minecraft-features/feature-toggles-java-edition), Mojang now includes experimental feature previews of upcoming Minecraft versions. On servers, they can be enabled by adding `update_1_20` to the `initial-enabled-packs` option in the server properties file (with entries separated with a comma) and will be applied to newly generated worlds. **We do not recommend enabling these feature packs on production servers**, as the features that come with them (such as Camels and the new bamboo blocks) will not survive world upgrades and are still riddled with bugs.  
  
We do not provide support for these experimental features and will not fix any issues with them, unless the issue in question is caused by one of our patches and can affect other parts of the server as well.  
  

### For Developers​

**Removal of Chat Previews**  
As part of 1.19.3, Mojang have removed the chat preview functionality in its entirety. This means you cannot make players sign messages that have been changed by the server (unless only formatting of the message has been changed) and other players will be able to see the unmodified chat message if they hover over a modified one.  
  
However, this does not affect `AsyncChatDecorateEvent` and `AsyncChatCommandDecorateEvent`; going forward, we will mostly likely encourage changing a message's content through the decorate events, with changes to viewers and the chat type being done in `AsyncChatEvent`. Finalized changes to API regarding chat and signed chat will be held off until 1.20 so it is less likely to break again with Mojang still doing such major changes to the system.  
  
**Experimental features**  
Plugin developers can prepare their plugins for these features with prelimary API, but be aware that most of the API representations of the experimental features are likely to change before they are finalized by Mojang. These classes, fields, etc. will be marked with an @Experimental annotation.

[Continue…](https://papermc.io/threads/paper-velocity-1-19-3.592/)

[](https://papermc.io/threads/paper-velocity-1-19-3.592/)

[Announcement Malware Announcement](https://papermc.io/threads/malware-announcement.529/)
-----------------------------------------------------------------------------------------

Sep **29**

* [Sep 29, 2022](https://papermc.io/threads/malware-announcement.529/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 35,393
* 22

We've seen a lot of reports of a new malware going around Minecraft servers. It seems to be spread by compromised Spigot plugin-author accounts, and is somewhat difficult to detect. We do know that the following exception is caused by it:  
  

Code:

    java.net.NoRouteToHostException: No route to host

  
If you see this in your logs, that server is most likely infected. There are other indicators too - the compromised JAR will have inside of it a file called plugin-config.bin. We do have a one-liner for searching for this in your plugin directories, if you're on a Linux system:  
  

Code:

    grep -R "plugin-config.bin" .

  
If you're on a Windows system you can run this command in your plugins directory:  
  

Code:

    findstr /sml /c:"plugin-config.bin" *

  
Run the above while in your server or plugin directory, and if you get a match, you likely have an infected plugin. If you do not get a match, that is a good thing - you are likely not infected.  
  
[@Optic\_Fusion1](https://forums.papermc.io/members/2180/) 's AntiMalware tool on [https://github.com/OpticFusion1/MCAntiMalware](https://github.com/OpticFusion1/MCAntiMalware) has caught onto this malware about a month ago already and catches more variants of it. We highly suggest users run this tool as it contains checks for a lot more malware sources. If this tool reports any malware found, be sure to double check whether it's a false positive or not (known example: ForceOP check falsely triggers on a handful of plugins because of how it's used in plugins).  
  
If you do get a match or think that you are infected, you should **delete all of your JAR files and re-download them**, as the malware spreads itself to other JARs. You should also **immediately reinstall your machine**, as this malware is known to install system services outside of Minecraft. It might be more effort, **but it is important that infected machines are reinstalled, or else the malware will remain**.  
  
If you frequently download plugins from third-party sources e.g. SpigotMC, it's not a bad idea to do routine checks with this tool e.g. once a month or so. **Remember to only download reputable plugins from reputable sources & authors.**  
  
Keep an eye out, and thanks.

[Continue…](https://papermc.io/threads/malware-announcement.529/)

[](https://papermc.io/threads/malware-announcement.529/)

[Announcement Paper 1.19.1](https://papermc.io/threads/paper-1-19-1.394/)
-------------------------------------------------------------------------

Jul **30**

* [Jul 30, 2022](https://papermc.io/threads/paper-1-19-1.394/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 15,096
* 1

### The 1.19.1 Update​

We are excited to announce that Paper 1.19.1 is now available! As far as we know, it is in a good state for production use - however, it is still early in the release cycle and new bugs may be discovered at any time, so we recommend that you make a backup of your server before upgrading.  
  

### Chat Signing and Reporting Concerns​

We have received a great deal of concern regarding our stance and support for the new chat signing aspect of Minecraft. As such, we figure it best to clear up a few points in this announcement.  
  
First: Paper will add support to its API so that plugins, servers, and developers that wish to use these features have the ability to without hindrance from us.  
  
Second: Servers, plugins, and developers that wish to disable chat signing will also have the ability to do so without any hindrance from us. We will not enforce the use of Minecraft's chat signing features nor will we use our software to actively prevent the bypassing of these new safety features.  
  
Third: We may choose to implement restrictions on our community's discussion of the bypassing of chat safety features. Similarly to offline mode servers, we would not at the same time prevent people's actually doing it, and will leave that decision up to each server owner and anyone using our software.  
  
Fourth: Paper is not so involved with Mojang as to be able to make changes or decisions on this new system. Mojang has generally been involved with the community for years in multiple ways, but we have done all that we can do by bringing up various concerns about the new system with them and leaving it in their hands.  
  
Finally: There is more information on the new system at [https://gist.github.com/kennytv/ed783dd244ca0321bbd882c347892874](https://gist.github.com/kennytv/ed783dd244ca0321bbd882c347892874). This is accurate information as far as we know, and will be updated as new information is made available.  
  
If you'd like to help the project's infrastructure costs, feel free to check out [https://papermc.io/sponsors](https://papermc.io/sponsors) - we greatly appreciate your continued support! Also, a special thanks to kennytv and Machine Maker for their extraordinary help on this update. They both have GitHub Sponsors if you'd like to contribute directly to them!  
  

### Chunk System Rewrite​

We recently announced on our [discord](https://discord.gg/papermc) that a new chunk system is in development and needs testing. It has been updated to include 1.19.1. You can find more information at the [PR on our GitHub](https://github.com/PaperMC/Paper/pull/8177). **_Please do not test this on worlds that are not backed up_**, or on production servers, as it is unstable and will probably break things. We appreciate any help in identifying and reporting bugs - please report anything broken on [the same PR, linked again here](https://github.com/PaperMC/Paper/pull/8177).  
  
One more reminder to please back up your server before upgrading to 1.19.1 - it is very important to do this!

[Continue…](https://papermc.io/threads/paper-1-19-1.394/)

[](https://papermc.io/threads/paper-1-19-1.394/)

[Announcement Paper 1.19](https://papermc.io/threads/paper-1-19.344/)
---------------------------------------------------------------------

Jun **12**

* [Jun 12, 2022](https://papermc.io/threads/paper-1-19.344/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 37,610
* 18

### The 1.19 Update​

We’re happy to announce that initial builds for Paper 1.19 have been released. We were able to fix a lot of issues already, but there might still be breaking ones, so as always, **backups are absolutely mandatory**. After upgrading your world to 1.19, **you cannot downgrade back to a lower version!**  
  
We would like to thank everyone that worked on this update. Not only the people actually working on the code, but everyone that provided feedback, helped us test, has been patient, and the people that joined us in VC or on Twitch (where over 400 people watched Kenny stream at one point!). We would like to especially thank the following people:  

* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)
* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [@Owen1212055](https://forums.papermc.io/members/80/) - [https://github.com/sponsors/Owen1212055](https://github.com/sponsors/Owen1212055)
* [@Noah](https://forums.papermc.io/members/81/) - [https://github.com/sponsors/NoahvdAa](https://github.com/sponsors/NoahvdAa)
* [@jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla/](https://github.com/sponsors/jpenilla/)
* [@MiniDigger](https://forums.papermc.io/members/15/) - [https://github.com/sponsors/MiniDigger](https://github.com/sponsors/MiniDigger)
* [@sulu](https://forums.papermc.io/members/12/)
* [CoreyShupe/FiXed](https://github.com/CoreyShupe)
* [@electronicboy](https://forums.papermc.io/members/2/) - [https://paypal.me/ShaneFreeder](https://paypal.me/ShaneFreeder)
* [@FivePB](https://forums.papermc.io/members/43/)
* [@Michael](https://forums.papermc.io/members/25/)
* [@aurora](https://forums.papermc.io/members/39/) - [https://github.com/sponsors/aurorasmiles](https://github.com/sponsors/aurorasmiles)

Next to those people, you can find links to support them individually. If you'd like to support PaperMC as a whole, you can find more information at [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  

### Major Configuration Changes​

Starting with 1.19, the Paper configuration files will now be split into multiple parts. Instead of having one giant paper.yml file for everything, there are now two files in a newly created `config` directory: `paper-global.yml`, where you can configure options that apply to the whole server, and `paper-world-defaults.yml`, where you can set default per-world values; you can change the directory from `config` to any directory you like with the new `--paper-settings-directory` command line argument. The per-world configuration has been split into each individual world directory (`paper-world.yml`), so for example, for the world `world_the_end`, you will find the configuration file at `world_the_end/paper-world.yml`.  
  
In addition to this, all configurable messages inside of Paper configs use the MiniMessage format from now on. This means that legacy formatting (`&` or `§` codes) will no longer work in the paper configs. Instead, you use MiniMessage, which allows modern formatting with RGB colors, gradients, translatable components, and a lot more. You can find more information about MiniMessage here: [https://docs.adventure.kyori.net/minimessage/format.html](https://docs.adventure.kyori.net/minimessage/format.html)\`  
  
To try out MiniMessage formatting, you can use this live-previewing website: [https://webui.adventure.kyori.net/](https://webui.adventure.kyori.net/).  
  
Your current configuration files will be migrated into the new format automatically while keeping all of your previous settings. Your old `paper.yml` will automatically be backed-up into `config/legacy-backup/paper.yml.old`.  
  
Our documentation will be updated over the next couple of weeks to reflect those changes.  
  
**Alternate Current redstone implementation**  
About a month ago, Space Walker ported his Fabric mod to Paper, allowing us to offer another redstone implementation: Alternate Current. You can enable it by changing the per-world setting [`redstone-implementation`](https://docs.papermc.io/paper/reference/paper-per-world-configuration#redstone-implementation) to `alternate-current`. As of now, Alternate Current is faster and more stable than the already implemented Eigencraft option (and a lot faster than Vanilla's redstone), but its behavior slightly deviates from Vanilla in certain edge cases, such as the order of surrounding block updates. Read more about Alternate Current and how it differs from other redstone implementations on [its README.](https://github.com/SpaceWalkerRS/alternate-current/blob/main/README.md)  
  

### For Developers​

**Signed chat messages**  
Minecraft 1.19 introduced client-side signing of chat messages, allowing other clients to verify a message has been sent by the player, delivered verbatim and unmodified by the server. In the future, the client will most likely visually distinguish signed player messages, unsigned player messages, and system messages. Because we want to avoid issues with upstream compatibility and duplicate work, we are not yet able to provide an API for that system. Currently, all messages will be sent as (unsigned and unverified) system messages – this has no meaningful impact on how clients display these messages yet. With Mojang trying to make the player chat more secure, we will have to make some larger additions and changes around message events and API in the future to allow features like the ability to preview formatted messages on the client.  
  
**MiniMessage methods in API**  
After the inclusion of MiniMessage in our API in 1.18, we have now added `sendPlainMessage(String)` and `sendRichMessage(String)` methods to the `CommandSender` interface to make developers more aware of the distinction between legacy, plain, and MiniMessage text formatting – we strongly discourage the use of the old `sendMessage(String)` methods using legacy formatting.  
  
**Configurate**  
We are currently **not** exposing Configurate, the library now used to manage Paper configurations, via our API. It will be exposed once Configurate receives more updates to make it more user friendly for use in plugins.  
  

### Experimental channel for builds​

Our downloads API has different channels to distinguish builds - right now between `experimental` and `default`. The first few 1.19 builds were released in the `experimental` channel, which has now been changed back to the `default` channel.  
  
For future updates, we will no longer provide any early experimental builds on Discord, instead using the `experimental` channel in our downloads API. **This means that you will need to distinguish between channels in your scripts to avoid getting highly experimental and potentially breaking versions. Please adjust your download scripts accordingly.** Experimental builds marked as such will be available to download on our homepage as well.

[Continue…](https://papermc.io/threads/paper-1-19.344/)

[](https://papermc.io/threads/paper-1-19.344/)

[Announcement Paper 1.18.2](https://papermc.io/threads/paper-1-18-2.185/)
-------------------------------------------------------------------------

Mar **04**

* [Mar 4, 2022](https://papermc.io/threads/paper-1-18-2.185/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 23,820
* 12

### The 1.18.2 Update​

We are now releasing initial builds for 1.18.2. These have been tested by our team over the last few days and we were able to iron out quite a few issues, but you should still be careful. These are early builds, they may contain breaking issues, backups are absolutely mandatory! **After you update, you cannot downgrade your world back to 1.18.1 or lower again!**  
  
As always, we would like to thank everybody who contributed to this update, be it by contributing code, reporting issues or just discussing changes with us in voice chat and cheering us on.  
  
In particular, we would like to thank the following developers:  

* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)
* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@jmp](https://forums.papermc.io/members/7/) - [https://github.com/sponsors/jpenilla/](https://github.com/sponsors/jpenilla/)
* [@kashike](https://forums.papermc.io/members/1/) - [https://github.com/sponsors/kashike](https://github.com/sponsors/kashike)
* [@Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [@electronicboy](https://forums.papermc.io/members/2/) - [https://www.paypal.com/paypalme/ShaneFreeder](https://www.paypal.com/paypalme/ShaneFreeder)

  
You can also support the PaperMC project itself, you can find more information about that here: [https://papermc.io/sponsors](https://papermc.io/sponsors)  

### For Developers​

**MiniMessage included in Paper API**  
Since MiniMessage is now stable, we have decided to include it in the Paper API. For those who don’t know what MiniMessage is yet; it’s a simple, user-friendly, string representation of Minecraft’s chat components, perfect for use in config files. You can learn more about it [here](https://docs.adventure.kyori.net/minimessage/), and be sure to check out [the Web UI](https://webui.adventure.kyori.net/) to start playing with MiniMessage now!  
  
Note: While MiniMessage is now packaged with the API and available for plugins to use, it is not currently used by Paper itself. In the future, we plan to migrate all configurable messages over to MiniMessage, allowing for much more control over the styling of configurable messages!  
  
[![1646417744506.png](https://forums.papermc.io/data/attachments/0/114-4c85677f8897c02f8a3efc2f01deed27.jpg "1646417744506.png")](https://forums.papermc.io/attachments/1646417744506-png.114/)  
[![1646417751079.png](https://forums.papermc.io/data/attachments/0/115-d0339a0a85af4a7d80fef54199dbc0c7.jpg "1646417751079.png")](https://forums.papermc.io/attachments/1646417751079-png.115/)  
  
**StructureLocateEvent replacement**  
Due to a lot of internal restructuring in Vanilla, the StructureLocateEvent has been replaced by the StructuresLocateEvent. It holds a list of ConfiguredStructures (as opposed to just one StructureType previously). The old event is no longer fired, so if you used it, you should update the API usage as soon as possible.  
  

### Docs​

Another thing we would like to note is that we are working on a new documentation site for the PaperMC organization, which will replace the various documentation sites currently in use. We are looking to open the floor for discussion, ideas, suggestions, and contributions, so please keep an eye on the [#docs channel](https://discord.gg/papermc) for more information!

[Continue…](https://papermc.io/threads/paper-1-18-2.185/)

[](https://papermc.io/threads/paper-1-18-2.185/)

[Announcement Paper 1.18 and more](https://papermc.io/threads/paper-1-18-and-more.6/)
-------------------------------------------------------------------------------------

Jan **04**

* [Jan 4, 2022](https://papermc.io/threads/paper-1-18-and-more.6/)
* [PaperMC](https://papermc.io/home/authors/papermc.44/)

* 24,263
* 17

### The 1.18 update​

After the initial release a bit over a month ago, Paper 1.18.1 is now deemed ready for use in production environments. As with any upgrade, please ensure you have a functioning backup before proceeding. **World downgrades are not supported under any circumstances.  
  
Upgrading worlds to 1.18**  
With the increased world height that 1.18 brought, Mojang has introduced retrogen to allow worlds using the old (0 to 256) height to upgrade cleanly to the new (-64 to 320) height. Retrogen will fill in new caves below the bedrock layer, allowing you to explore the new terrain in already generated chunks. Should retrogen be undesired, you can disable it by setting `below-zero-generation-in-existing-chunks` to `false` in `spigot.yml`. **This option is not recommended and may not work correctly in conjunction with `--forceUpgrade` or with worlds older than 1.14.** Mojang has also introduced world blending to cleanly transition from old to new generation at the border of chunks that have not been generated before.  
  
**Changes to Anti-Xray and ore generation**  
Ores can now generate a lot higher than before, so you might need to adjust your Anti-Xray settings. We have increased the default `max-block-height` to 64, but you might want to increase it even further. Please be aware that higher numbers might impact performance, especially with `engine-mode: 2`. See [stonar's anti-xray guide](https://gist.github.com/stonar96/ba18568bd91e5afd590e8038d14e245e) and the [updated ore distribution](https://minecraft.fandom.com/wiki/Ore#Distribution) for more information.  
  
**Security fixes to all Minecraft versions**  
Throughout December, we have pushed important security fixes to all Paper versions from 1.8 to 1.18. If you are running a build or server fork older than that on any given version, you should **update immediately**. While we decided to make an exception in pushing the fixes to legacy versions, we will never do this again, and it is only a matter of time until a new major security issue sees the light of day.  
  
We would also like to thank the member of our community that made us aware of the issue via the [exploit-report channel on our Discord](https://discord.com/channels/289587909051416579/869651180698099732/869715284511051867), which made it possible to respond to the issue before it received too much public attention and to have Minecraft as a whole be one of the first communities to warn users about it.  
  
**Contributors to 1.18**  
A big thank you to everyone who contributed to the update process:  

* [@kennytv](https://forums.papermc.io/members/5/) - [https://github.com/sponsors/kennytv](https://github.com/sponsors/kennytv)
* [@jmp](https://forums.papermc.io/members/7/) - [https://www.patreon.com/jmp\_](https://www.patreon.com/jmp_)
* [@Machine Maker](https://forums.papermc.io/members/37/) - [https://github.com/sponsors/Machine-Maker](https://github.com/sponsors/Machine-Maker)
* [@MiniDigger](https://forums.papermc.io/members/15/) - [https://github.com/sponsors/MiniDigger](https://github.com/sponsors/MiniDigger)
* [@Spottedleaf](https://forums.papermc.io/members/10/) - [https://www.patreon.com/Spottedleaf](https://www.patreon.com/Spottedleaf)
* [@DenWav](https://forums.papermc.io/members/3/)
* [@JRoy](https://forums.papermc.io/members/11/)
* [@stonar96](https://forums.papermc.io/members/45/)

  
If you want to support the PaperMC project, you can find more information here: [https://papermc.io/sponsors](https://papermc.io/sponsors).  
  
We would also like to thank everyone who watched, chatted and talked with us during the update process. You are amazing ![❤️](https://twemoji.maxcdn.com/2/72x72/2764.png "Red heart    :heart:")  
  

### For Developers​

**Changes to Paperweight (Paper contributors)**  
Instead of using the `shadowJar` and `reobfJar` Gradle tasks to create a runnable (but not distributable) jar, you now need the `createMojmapBundlerJar` or `createReobfBundlerJar` tasks. Similarly, Paperclip (distributable) jars are now created with the `createMojmapPaperclipJar` or `createReobfPaperclipJar` task. You can get a full list of tasks by running `gradlew tasks`. An updated, in-depth guide on contributing to Paper can be found [here](https://github.com/PaperMC/Paper/blob/master/CONTRIBUTING.md).  
  
**Paperweight Userdev: Working with NMS in 1.17+ (Plugin developers using NMS)**  
After upstream dropped their field mappings in 1.17, the same now happened with method names as well. Even though we generally advise against depending on server internals, we understand that not everything is possible through API. As of now, the only feasible way of depending on server internals is by coding against mapped names, which are then compiled to the obfuscated names to run with the obfuscated server. Paperweight’s Userdev allows you to do exactly that, but unlike upstream’s maven plugin, userdev uses full Mojang mappings with additional yarn parameter mappings, so you can more easily update your plugin whenever a new Minecraft version is released. Userdev is the **only supported way of working with NMS in 1.18+**. The obfuscated jar is no longer valid to compile against.  
  
To set up paperweight userdev:  

1. Add Paper’s maven [repository to your Gradle plugin repositories](https://github.com/PaperMC/paperweight-test-plugin/blob/9d2939f402b9c46454939829cf21c3ab8b8612ca/settings.gradle.kts#L1-L6) in your `settings.gradle.kts`.
2. Add the Paperweight Userdev Gradle [plugin to your build config](https://github.com/PaperMC/paperweight-test-plugin/blob/9d2939f402b9c46454939829cf21c3ab8b8612ca/build.gradle.kts#L5) with the id `io.papermc.paperweight.userdev`, keeping the version in sync with the [paperweight version used in Paper](https://github.com/PaperMC/Paper/blob/5e30e19e20670b2eac42aacb02dda82d56995bad/build.gradle.kts#L8).
3. Add the [development bundle to your dependencies](https://github.com/PaperMC/paperweight-test-plugin/blob/9d2939f402b9c46454939829cf21c3ab8b8612ca/build.gradle.kts#L20).
4. Make the [`assemble` task depend on the `reobfJar` task](https://github.com/PaperMC/paperweight-test-plugin/blob/9d2939f402b9c46454939829cf21c3ab8b8612ca/build.gradle.kts#L31).

  
A full, working example can be found [on GitHub](https://github.com/PaperMC/paperweight-test-plugin). Both `settings.gradle.kts` and `build.gradle.kts` are important! Paperweight Userdev integrates with the Gradle Shadow plugin, no special configuration is required.  
  
If you have previously used Apache Maven, Gradle supports [automatic migration for the majority of project configurations](https://docs.gradle.org/current/userguide/migrating_from_maven.html#migmvn:automatic_conversion). We would recommend the Kotlin DSL, which can be selected via `gradle init --dsl kotlin`. If you have any issues getting started with Userdev, please come by the `#paper-dev` channel on our [Discord](https://discord.gg/papermc).  

### ​

### Miscellaneous​

**Downloads API**  
We have shut down v1 of our downloads API at the end of November. Please make sure you are using v2 of our downloads API when trying to download Paper via scripts and automated tools. For reference, see the [Downloads API documentation](https://papermc.io/api/docs/). We have also introduced a `channel` field to the `build` response, allowing builds to be marked as experimental.  
  
**Changes to the PaperMC team**  
Over the past couple of months, there have been a number of changes to the PaperMC team. Larry has been promoted to the role of Community Manager and will be focusing on the moderation aspects of the community. We would also like to welcome ocelotpotpie to our moderation team. sulu has taken the position of Triage lead and will be responsible for managing the Triage team, which looks after our GitHub issues. jmp has joined the Maintainer team; Proximyst has left the team, and we wish her all the best! aurora has left the development team to focus more on her responsibilities as a community manager.

[Continue…](https://papermc.io/threads/paper-1-18-and-more.6/)

[](https://papermc.io/threads/paper-1-18-and-more.6/)

[Welcome to PaperMC](https://papermc.io/threads/welcome-to-papermc.1/)
----------------------------------------------------------------------

Dec **14**

* [Dec 14, 2021](https://papermc.io/threads/welcome-to-papermc.1/)
* [kashike](https://papermc.io/home/authors/kashike.1/)

* 8,844
* 2

[![kashike](https://secure.gravatar.com/avatar/c50766d24721f3cdd0ff9e8ead43134b?s=48)](https://papermc.io/members/kashike.1/)

Welcome to PaperMC! This is the community forum space for our Minecraft software community - here, we ask questions, give answers, and talk about everything to do with our projects.  
  
**Paper**: This is our Minecraft server software. It's designed to be fast, bug-free, and a breeze to use. With an extensive API for plugin developers to boot, we work hard on Paper and we're proud of it.  
  
**Velocity**: A recent addition to the PaperMC community, Velocity is the most modern, secure, and highly performant proxy for Minecraft servers out there.  
  
**Waterfall**: A BungeeCord-compatible Minecraft server proxy that might not be quite as fast as Velocity, but is fully supported and fully supports any BungeeCord plugins you might need to use!  
  
Overall, PaperMC is a community that's excited about Minecraft software and making it better, while also providing a community space that's fun to be in. We have a strong culture of helping people and sharing knowledge for the betterment of everyone involved. Regardless of if you're a developer, run a Minecraft server yourself, or help someone else do it, we hope that you find yourself welcomed (and welcome others!) whenever you join us. Whether here, on [Discord](https://discord.gg/papermc), or on [GitHub](https://github.com/PaperMC), enjoy your time in the PaperMC community!

[Continue…](https://papermc.io/threads/welcome-to-papermc.1/)

[](https://papermc.io/threads/welcome-to-papermc.1/)

### [Members online](https://papermc.io/online/)

No members online now.

Total: 30 (members: 0, guests: 30)

### [Latest posts](https://papermc.io/whats-new/posts/?skip=1)

[K](https://papermc.io/members/khunchang888.12313/)

* Question

Question [How to set up Velocity Mysql Idk to start](https://papermc.io/threads/how-to-set-up-velocity-mysql-idk-to-start.1434/)

* [khunchang888](https://papermc.io/members/khunchang888.12313/)
* [Yesterday at 10:43 AM](https://papermc.io/threads/how-to-set-up-velocity-mysql-idk-to-start.1434/)
* [Help](https://papermc.io/forums/velocity-help/)

Replies

0

Views

23

[Help](https://papermc.io/forums/velocity-help/) [Yesterday at 10:43 AM](https://papermc.io/threads/how-to-set-up-velocity-mysql-idk-to-start.1434/latest)

[khunchang888](https://papermc.io/members/khunchang888.12313/)

[K](https://papermc.io/members/khunchang888.12313/)

[1](https://papermc.io/members/1234567s.6717/)

* Question

Question [TNT behaiving wierdly on papermc](https://papermc.io/threads/tnt-behaiving-wierdly-on-papermc.981/)

* [1234567s](https://papermc.io/members/1234567s.6717/)
* [Dec 10, 2023](https://papermc.io/threads/tnt-behaiving-wierdly-on-papermc.981/)
* [Help](https://papermc.io/forums/paper-help/)

Replies

6

Views

1K

[Help](https://papermc.io/forums/paper-help/) [Tuesday at 11:44 AM](https://papermc.io/threads/tnt-behaiving-wierdly-on-papermc.981/latest)

[electronicboy](https://papermc.io/members/electronicboy.2/)

[![electronicboy](/data/avatars/s/0/2.jpg?1639525591)](https://papermc.io/members/electronicboy.2/)

[T](https://papermc.io/members/tayshawn.12268/)

* Question

Question [Item despawning upon death](https://papermc.io/threads/item-despawning-upon-death.1433/)

* [Tayshawn](https://papermc.io/members/tayshawn.12268/)
* [Monday at 7:26 PM](https://papermc.io/threads/item-despawning-upon-death.1433/)
* [Help](https://papermc.io/forums/paper-help/)

Replies

0

Views

48

[Help](https://papermc.io/forums/paper-help/) [Monday at 7:26 PM](https://papermc.io/threads/item-despawning-upon-death.1433/latest)

[Tayshawn](https://papermc.io/members/tayshawn.12268/)

[T](https://papermc.io/members/tayshawn.12268/)

[M](https://papermc.io/members/mixter213.12040/)

* Question

Question [Paper - Velocity command aliases](https://papermc.io/threads/paper-velocity-command-aliases.1429/)

* [Mixter213](https://papermc.io/members/mixter213.12040/)
* [Oct 27, 2024](https://papermc.io/threads/paper-velocity-command-aliases.1429/)
* [Help](https://papermc.io/forums/velocity-help/)

Replies

4

Views

174

[Help](https://papermc.io/forums/velocity-help/) [Friday at 9:08 AM](https://papermc.io/threads/paper-velocity-command-aliases.1429/latest)

[YuanYuanOwO](https://papermc.io/members/yuanyuanowo.12188/)

[Y](https://papermc.io/members/yuanyuanowo.12188/)

[C](https://papermc.io/members/creamgod45.12166/)

Question [try createBlockData got java.lang.NullPointerException: null](https://papermc.io/threads/try-createblockdata-got-java-lang-nullpointerexception-null.1432/)

* [creamgod45](https://papermc.io/members/creamgod45.12166/)
* [Oct 31, 2024](https://papermc.io/threads/try-createblockdata-got-java-lang-nullpointerexception-null.1432/)
* [Plugin Development](https://papermc.io/forums/paper-plugin-development/)

Replies

4

Views

111

[Plugin Development](https://papermc.io/forums/paper-plugin-development/) [Oct 31, 2024](https://papermc.io/threads/try-createblockdata-got-java-lang-nullpointerexception-null.1432/latest)

[stefvanschie](https://papermc.io/members/stefvanschie.38/)

[S](https://papermc.io/members/stefvanschie.38/)

[H](https://papermc.io/members/harttman.12079/)

* Question

Question [command error](https://papermc.io/threads/command-error.1431/)

* [harttman](https://papermc.io/members/harttman.12079/)
* [Oct 29, 2024](https://papermc.io/threads/command-error.1431/)
* [Help](https://papermc.io/forums/paper-help/)

Replies

0

Views

83

[Help](https://papermc.io/forums/paper-help/) [Oct 29, 2024](https://papermc.io/threads/command-error.1431/latest)

[harttman](https://papermc.io/members/harttman.12079/)

[H](https://papermc.io/members/harttman.12079/)

[G](https://papermc.io/members/goilev.12016/)

* Question

Question [the problem with the time of despawn of discarded items](https://papermc.io/threads/the-problem-with-the-time-of-despawn-of-discarded-items.1428/)

* [Goilev](https://papermc.io/members/goilev.12016/)
* [Oct 27, 2024](https://papermc.io/threads/the-problem-with-the-time-of-despawn-of-discarded-items.1428/)
* [Help](https://papermc.io/forums/paper-help/)

Replies

1

Views

114

[Help](https://papermc.io/forums/paper-help/) [Oct 27, 2024](https://papermc.io/threads/the-problem-with-the-time-of-despawn-of-discarded-items.1428/latest)

[stefvanschie](https://papermc.io/members/stefvanschie.38/)

[S](https://papermc.io/members/stefvanschie.38/)

[P](https://papermc.io/members/pepf.11981/)

[Why do my commands not work?](https://papermc.io/threads/why-do-my-commands-not-work.1427/)

* [Pepf](https://papermc.io/members/pepf.11981/)
* [Oct 25, 2024](https://papermc.io/threads/why-do-my-commands-not-work.1427/)
* [Plugin Development](https://papermc.io/forums/paper-plugin-development/)

Replies

1

Views

115

[Plugin Development](https://papermc.io/forums/paper-plugin-development/) [Oct 26, 2024](https://papermc.io/threads/why-do-my-commands-not-work.1427/latest)

[electronicboy](https://papermc.io/members/electronicboy.2/)

[![electronicboy](/data/avatars/s/0/2.jpg?1639525591)](https://papermc.io/members/electronicboy.2/)

[R](https://papermc.io/members/rechords25.10801/)

[Villager restocking differences to Vanilla](https://papermc.io/threads/villager-restocking-differences-to-vanilla.1321/)

* [rechords25](https://papermc.io/members/rechords25.10801/)
* [Aug 27, 2024](https://papermc.io/threads/villager-restocking-differences-to-vanilla.1321/)
* [Discussion](https://papermc.io/forums/paper-discussion/)

Replies

1

Views

277

[Discussion](https://papermc.io/forums/paper-discussion/) [Oct 26, 2024](https://papermc.io/threads/villager-restocking-differences-to-vanilla.1321/latest)

[User670](https://papermc.io/members/user670.11999/)

[U](https://papermc.io/members/user670.11999/)

[![PaperMC](/data/avatars/s/0/44.jpg?1692045896)](https://papermc.io/members/papermc.44/)

* Article

Announcement [Announcing the end of life of Waterfall](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)

* [PaperMC](https://papermc.io/members/papermc.44/)
* [Mar 26, 2024](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/)
* [Announcements](https://papermc.io/forums/papermc-announcements/)

Replies

11

Views

18K

[Announcements](https://papermc.io/forums/papermc-announcements/) [Oct 25, 2024](https://papermc.io/threads/announcing-the-end-of-life-of-waterfall.1088/latest)

[brettdesilets](https://papermc.io/members/brettdesilets.11965/)

[B](https://papermc.io/members/brettdesilets.11965/)

[View more…](https://papermc.io/whats-new/posts/?skip=1)

* 
* [PaperMC - Light Theme](https://papermc.io/misc/style "Style chooser")

* [Terms and rules](https://papermc.io/help/terms/)
* [Privacy policy](https://papermc.io/help/privacy-policy/)
* [Help](https://papermc.io/help/)
* [Home](https://forums.papermc.io/)
* [](#top "Top")
* [RSS](https://papermc.io/forums/-/index.rss "RSS")

[Community platform by XenForo® © 2010-2021 XenForo Ltd.](https://xenforo.com/) | [Style and add-ons by ThemeHouse](https://www.themehouse.com/?utm_source=forums.papermc.io&utm_medium=xf2product&utm_campaign=product_branding)

* [](https://discord.gg/papermc "Discord URL")
* [](https://github.com/PaperMC "GitHub")
* [](https://twitter.com/PaperPowered "Twitter")

* This site uses cookies to help personalise content, tailor your experience and to keep you logged in if you register.  
    By continuing to use this site, you are consenting to our use of cookies.
    
    [Accept](https://papermc.io/account/dismiss-notice) [Learn more…](https://papermc.io/help/cookies)