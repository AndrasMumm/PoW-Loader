# Path Of Wuxia ModLoader + English Patch

Join our discord! 
https://discord.com/invite/PH4Z4Dn

We are always in search for new Translators between Chinese and English, but we are also thankful about Proof Readers, Coders and more!
You are also very welcome to just come and hang out.

-------------------------------------------
BepInEx is the actual underlying ModLoader.
This repository contains a ModAPI plugin containing base functionalities for other Mods and Plugins.
It currently allows dynamic registration of external Asset folders, which allows several mods to register asset overrides.
It also supports modifying textures inside prefabs, though that is experimental

Additionally this repository contains the EnglishPatch Plugin, which registers Mods/EnglishTranslate as a resource folder (So place the translated Asset files into Mods/EnglishTranslate) as well as fixing several issues with displaying the English Text in the game.

The Output folder contains an almost full release after building, containing more or less up to date English files and an already configured BepInEx.
If BepInEx is updated/replaced by a new version it is important to update the BepInEx.cfg and replace the following Entry.

```ini
[Preloader.Entrypoint]

## The local filename of the assembly to target.
# Setting type: String
# Default value: UnityEngine.CoreModule.dll
Assembly = UnityEngine.CoreModule.dll

## The name of the type in the entrypoint assembly to search for the entrypoint method.
# Setting type: String
# Default value: Application
Type = Object

## The name of the method in the specified entrypoint assembly and type to hook and load Chainloader from.
# Setting type: String
# Default value: .cctor
Method = .cctor
```

otherwise the Entrypoint will be too late and some language files are already loaded.

-------------------------------------------

The dependency folder contains parts of the game and unitys assembly since they are needed for plugins.
I do not hold any copyright to any file inside the Dependency folder.
