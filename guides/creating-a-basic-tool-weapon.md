---
description: >-
  Tool/weapon creation is very easy with ConfigurableArmory! I swear, please
  don't get angry at me please i
---

# Creating a basic tool/weapon

### Basic Setup

After installing and running ConfigurableArmory at least once, there should now be a "configurablearmory" directory in your root Minecraft folder. This directory contains three folders- items, materials, and cosmetic. We'll go over what these are in a second. For now, just create a .hjson file in the items folder, with some basic [hjson](https://hjson.github.io/) syntax and fields.

```
{
    id: exampletool
    type: tool
    translationKey: custom.exampletool
    material: examplematerial
    tab: 7
    template: pickaxe
}
```

Basic descriptions of each of these fields:

**id**: This is the resource location/id of your tool. Your tool's id in-game will be referenced by configurablearmory: and then the id you enter here. This means it's possible to give yourself the tool using commands or similar.

**type**: This is the type of item you're making. For now, the only type is 'tool'. Don't be alarmed; This type works for weapons as well, it's just called 'tool' to differentiate it from armor (armor not yet implemented).

**translationKey**: This is what you use to refer to your custom item in a .lang file. You'll be able to put a .lang file in the cosmetic folder, but that will be explained soon.

**material**: This is a custom material you create yourself in the materials folder. This lets you define the various attributes of your tools, and reuse them for multiple items.

**tab**: Creative tab the tool shows up in. For reference of what number is what creative tab, see the Custom Tool Reference page.

**template**: The base for your tool. Can be pickaxe, shovel, axe, sword, or hoe.&#x20;

There are other keys than this, but these are the most important ones to keep in mind, and it's possible to make a functional tool or weapon with only these keys in your .hjson file. If you want do anything else, like make a weapon with a custom swing speed or attack damage relative to it's material, check the Custom Tool Reference below.

### Material Creation

Next, you need to create your material's .hjson file. Make another .hjson file, this time in the materials folder, and populate it with keys again:

```
{
    type: tool
    name: examplematerial
    harvestLevel: 1
    maxDurability: 1
    miningSpeed: 1.0
    attackDamage: 0.0
    enchantability: 1
}
```

These fields, respectively:

**type**: The type of item this material is for. Just, put tool in here, we don't have armor yet as a thing.

**name**: The name of your material. This is what you use in materialName in your tool's .hjson file.

**harvestLevel**: The harvest level of the tools and weapons made with this material. Important for progression in modpacks.

**maxDurability**: The maximum possible durability that a tool could have that uses this material. Most tools that use your material have less max durability then this, so set it accordingly.

**miningSpeed**: The speed that it mines. Bigger number = faster dig blocks.

**attackDamage**: The "base" attack damage that most tools and weapons add on to. Don't set this too high.

**enchantability**: How 'enchantable' items made with this material are. The higher the integer, the more powerful enchantments items made with this material tend to have.

That's all you really need to know to make a material file, but you can see the Custom Material Reference for more information.

### Textures, Models, and Lang

Once you have the material and item files complete, you're pretty much done. But unless you want a purple and black block in your game instead of a cool texture or something, you'll probably want to give your item a model, texture, and translations for it's name.

[Making a model](https://minecraft.fandom.com/wiki/Model) is pretty straightforward, though it is done with regular JSON because Minecraft is annoying sometimes. Just put this model under cosmetic/configurablearmory/models/item/ and name it whatever you put as "id" in your item's hjson file. Make sure to name the model's texture in the model file accordingly, and put that texture in cosmetic/configurablearmory/textures/item/.&#x20;

Lang follows the same principle. Since "cosmetic" is basically a resource pack, just put the language file under cosmetic/configurablearmory/lang/ and name it whatever the language you're translating your item to is (Usually en\_us.lang for us troglodytes in Amerikkka). Put a line in that file that references your item's translationKey, and gives it an actual display name, like so:

```
custom.exampletool=Example Tool
```

Once you have your language files, model, and texture in place, you're done. You should be able to just launch the game and see the fruits of your labor immediately in the world. If that doesn't work, feel free to contact me for help (somehow), or see the references below just in case you entered the wrong variable type or a similar syntax issue.



Thank you for using ConfigurableArmory

{% content-ref url="../reference/custom-material-reference.md" %}
[custom-material-reference.md](../reference/custom-material-reference.md)
{% endcontent-ref %}

{% content-ref url="../reference/custom-tool-reference.md" %}
[custom-tool-reference.md](../reference/custom-tool-reference.md)
{% endcontent-ref %}
