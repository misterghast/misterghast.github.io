---
description: >-
  This is a reference for all of the keys and values for a custom material
  .hjson file for ConfigurableArmory
---

# Custom Material Reference

### 'type' key

This key is used to denote the kind of item this material is used for. For now, only 'tool' is a valid value for this key.

```
Possible values: tool
```

### 'name' key

Used to define the name of the material in code. This is what you refer to for the 'material' key in item .hjson files. Can be any string, without spaces, please.

```
Possible values: any string (no spaces)
```

### 'harvestLevel' key

Sets the harvest level of tools that use this material.

```
Possible values: any integer
```

### 'maxDurability' key

Maximum durability possible for tools and weapons that use this material. Use any integer, usually at least in the double digits.

```
Possible values: any integer
```

### 'miningSpeed' key

How fast pick go mine fast how fast tool go mine dig. Most tools actually remove from this, not add to it, especially vanilla tool types, so keep that in mind when setting this.

```
Possible values: any double
```

### 'attackDamage' key

The base attack damage of tools and weapons that use this material.&#x20;

```
Possible values: any double
```

### 'enchantability' key

How enchantable and magical and cool and awesome and awesome and awesome and awesome and

```
Possible values: any integer
```
