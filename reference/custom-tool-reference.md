---
description: >-
  This is a description of all the possible values and keys of a custom tool
  hjson file for ConfigurableArmory.
---

# Custom Tool Reference

### 'id' key

The id key is used for reference in the game's code, as it's the second half of your custom item's id (configurablearmory:id). So this is quite important, make sure to set it! It can be any String value.

```
Possible values: Any string 
```

### 'type' key

This value can only be 'tool'. Don't bother changing it to anything else yet, nothing else has been implemented. You will be able to change it to 'armor' once custom armor is in the mod, though.

```
Possible values: tool
```

### 'translationKey' key

The value for this key is used as the lang key for your custom item. Very important, don't forget it. You'll regret forgetting it...

```
Possible values: Any string (format.like.this)
```

### 'material' key

A string referencing a material made with ConfigurableArmory. Don't reference materials don't exist, it could do anything from crash your game to destroy the planet.

```
Possible values: Any string (as long as it references a material you made :))
```

### 'tab' key

An integer id that maps to a creative tab that your custom tool will show up in.

```
Possible values:
    0: Building Blocks
    1: Decorations
    2: Redstone
    3: Transportation
    4: Misc
    5: Food
    6: Tools
    7: Combat
    8: Brewing
    anything else: defaults to Combat 
```

### 'attackSpeed' key

This is used to set the attack speed of the weapon or tool, it's a double value. Not needed if you set the 'template' value, otherwise important and your game will not boot without it.

```
Possible values: any double
```

### 'attackDamage' key

This is used to set the additional attack damage of the weapon or tool. Not needed if you set the 'template' value, otherwise important and your game will not boot without it. Adds ON TOP of your material's attack damage value, not instead of. A material with an attack damage of 5 and a sword with an attack damage of 4 will result in a sword with an attack damage of 9!

```
Possible values: any double
```

### 'template' key

Important! Used to set the attackSpeed, attackDamage, durability multiplier (not yet implemented), and tool types of a weapon or tool to one of the five vanilla tool types (sword, axe, pickaxe, shovel, hoe). You can also set it to 'none', which will do the same thing as not having the template key in your hjson file at all. Don't do this, I don't know why you would.

```
Possible values: axe, pickaxe, shovel, hoe, sword
```

### 'extraAttributes' key

A list of lists, used to define the extra attributes the weapon modifies. You can use this to make weapons with longer reach, that grant the user increased movement speed, extra max health, or even extra swim speed. Hopefully useful

```
Possible values: one list like this: [
        with other lists inside formatted like this:
        ["attributeName", attributeValue]
]
Possible attributeName values:
        speed
        health
        reach
        swimSpeed
Possible attributeValue values:
        any double lol
```

