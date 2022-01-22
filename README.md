# Clip Dictionary Research
This is **.#CD** GTAV Format Research.<br>
Some information was taken from [Codewalker Discord](https://discord.com/invite/BxfKHkk).

## Tags
Tags control additional events embed in **Animation Clip**, such as VFX Particles, Sounds, IK Targets

### Codewalker XML Declaration:
```xml
<Item>
 <NameHash> <!-- Tag Type --> </NameHash>
 <UnkHash> <!-- Unknown --> </UnkHash>
 <Attributes>
  <Item>
   <NameHash> <!-- Tag Attribute Type --> </NameHash>
   <Type value="" /> <!-- Type of Attribute Value -->
   <Value value=""/> <!-- Attribute Value -->
  </Item>
 </Attributes>
 <!-- Tag trigger offsets relative to normalized animation length (0.0 - 1.0) -->
 <Unknown40 value="0.0" />
 <Unknown44 value="0.0" />
</Item>
```

### Known Tag Types:
Name | Hash | Description
:--- | :--- | :---
door | 0xBEF83F1B | IK Target - Vehicle Door
ik | 0xA5F6D578 | Switches Inverse-Kinematics On/Off

### Known Attribute Types:
Name | Hash | Type | Description
:--- | :--- | :--- | :---
heel | 0x2bc03824
lookik | 0x4977ab78
create | 0x629712b0
destroy | 0x6d957fee
moveevent | 0x7ea9dfc4
narrowest | 0x8008f9b5
full | 0x93147756
foot | 0xb82e430b
right | 0xb8ccc339 | bool | Switches Left / Right hand for IK
release | 0xbc7c13b5
phonering | 0xd93a7eb6
register | 0x344f0278
blocked | 0x568f620c
stop | 0x930ca7f2 | bool | Switches Tag OFF/ON
start | 0x84DC271F | bool | Switches Tag OFF/ON
loopingaudio | 0xa31d8f23
allowed | 0xa7c897b9
vfxname | 0xab95f43a
trigger | 0xc3afd061
objectvfx | 0xeea25b57

### Codewalker XML Attribute Value Types:
Name | Template | Description 
:--- | :--- | :---
HashString | hash_0x00000000 | Hash of a Resource, for i.e Script Audio Hash
Int | 0
Bool | 0
Float | 0.0

### Related Natives:
* bool FindAnimEventPhase(string animDictionary, string animName, string p2, ref Any p3, ref Any p4);
* HasAnimEventFired(int entity, uint actionHash);
