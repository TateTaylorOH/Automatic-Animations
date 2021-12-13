![](https://raw.githubusercontent.com/TateTaylorUSA/TateTaylorUSA/master/assets/images/banners/AutomaticAnimations.png)\

I stumbled across [SkyUI Weapons Pack](https://www.nexusmods.com/skyrimspecialedition/mods/37231) a while ago and really liked the new weapon icons it added. I tried to apply them to some of the mods I had in my load order but quickly got annoyed by the amount of patching it required. So instead of trying to manually add new keywords to every item I decided to try out the [Keyword Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/55728) to apply the keywrods at runtime. It worked like a charm!

Then I realized I could probably use this same method to easily add animations from [Animated Armory](https://www.nexusmods.com/skyrimspecialedition/mods/35978) ﻿to any weapon without need of a plugin. After about a night's work I had a series of KID .inis and [Dynamic Animation Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/33746) conditions set up to do all this work for me. So now to assign custom animations and icons to weapons I just need to add a simple line of text to a KID .ini and it works flawlessly!

I decided to share this little framework I jury rigged together, I am sure someone else might find this useful. Enjoy!

![](https://raw.githubusercontent.com/PierreDespereaux/PierreDespereaux/master/assets/images/banners/Features.png)

-   A set of KID .inis that will allow you to assign custom icons and animations to weapons with a simple line of text.
-   Built-in compatibility for the majority of weapon mods that add new weapon types such as Halberd and Spears to the vanilla material types.
-   Highly compatible and free from any and all plugin conflicts.\
Requirements

This mod is built around the [Keyword Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/55728)﻿ and it is required in order to properly function.

[SkyUI Weapons Pack](https://www.nexusmods.com/skyrimspecialedition/mods/37231) is required to get the custom weapons icons and [Dynamic Animation Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/33746) is required to properly assign the new animations.

While [Animated Armory](https://www.nexusmods.com/skyrimspecialedition/mods/35978)﻿ itself isn't required, you will at least need the meshes folder from the DAR version in order to make the animations work. Let this mod override Animated Armory.\
![](https://raw.githubusercontent.com/PierreDespereaux/PierreDespereaux/master/assets/images/banners/Compatibility.png)\
Compatiblity for the following mods are built directly into this framework:

-   [Animated Armory](https://www.nexusmods.com/skyrimspecialedition/mods/35978)﻿
-   [Beyond Skyrim: Bruma](https://www.nexusmods.com/skyrimspecialedition/mods/10917)﻿
-   [Beyond Skyrim: Wares of Tamriel](https://www.nexusmods.com/skyrimspecialedition/mods/31519)﻿
-   [Headman's Cleaver](https://en.uesp.net/wiki/Skyrim:Headman%27s_Cleaver)﻿
-   [Heavy Armory - New Weapons](https://www.nexusmods.com/skyrimspecialedition/mods/6308)﻿
-   [Shirley - A Skyrim Follower Mod](https://www.nexusmods.com/skyrimspecialedition/mods/45956)﻿
-   Most mods that add Goldbrand
-   Most mods that add new add new weapon types such as Halberd and Spears to the vanilla material types\

It is very easy to extend this mod to suit your own load order. Simply create a new .ini file with the suffix "_KID" and place it into your mod's folder. Then use the following template to assign the proper keywords to the weapons you want:

`Keyword = [KeywordFormID]|Weapon|[WeaponName]|NONE|NONE`

The keyword formID for each of the relevant weapon type can be found below:

`01DE5005: WeapTypeSpear\
01DE5006: WeapTypeJavelin (no animations weapons exist for this weapon type)\
01DE5007: WeapTypePike\
01DE5008: WeapTypeHalberd\
01DE5009: WeapTypeRapier\
01DE500A: WeapTypeQuarterstaff\
01DE500B: WeapTypeClaw\
01DE500C: WeapTypeScythe (no animations weapons exist for this weapon type)\
01DE500D: WeapTypeWhip\
01DE500E: WeapTypeKatana\
01DE500F: WeapTypeGun (no custom animations exist for this weapon type)`
