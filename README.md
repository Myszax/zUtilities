# zUtilities

This is a simple plugin made in [Union](https://worldofplayers.ru/threads/40376/) **1.0l** for Gothic 1 and 2.

### Features

- Allows to quickly save / load game with `F10` and `F12` keys.

  - Range of save slots used for quick save can be adjusted in `gothic.ini` with `MinSaveSlot`, `MaxSaveSlot` options. Default, it's 6 bottom slots.
  - Notice strings are set automatically depending on system language but still can be changed manually in `gothic.ini` with `CantSave`, `CantLoad` and `NoSave` options.
  - This feature can be disabled in `gothic.ini` with `UseQuickSave` option.

- Changes name color of focused npcs, containers, doors and items.

  - Npcs: `Red` - hostile / wants to kill you, `Orange` - angry / pissed off, `Cyan` - partymember, `Green` - friendly, `Slightly green` - friendly guild, `White` - neutral / dead, `Grey` - dead and looted.
  - Doors: `Red` - locked on key, `Orange` - locked, `White` - open.
  - Containers: `Red` - locked on key, `Orange` - locked, `Green` - open with items, `Grey` - open and empty.
  - Items: `White` - default / item can be taken, `Slightly orange` - someone will catch the hero stealing.
  - Each group can be disabled separately in `gothic.ini` with `ColorNpcs`, `ColorChests`, `ColorDoors` and `ColorItems` options.

- Renders the selected inventory item in the center of the screen instead of in the item description box.

  - Camera in inventory will be shifted a bit, so the item doesn't cover the hero.
  - In Gothic 2 item will be animated only if item has `inv_animate` property set to true.
  - In Gothic 1 item will be displayed on the left or right when trading.
  - This feature can be disabled in `gothic.ini` with `CenterInvItems` option.

- Renders labels for items in the inventory based on item parameters.

  - All icons are made via [Game-icons.net](https://game-icons.net/) website.
  - There are many possible icons to appear when item has right parameters. There are labels even for items that don't exist in original game like shields, helmets, armors requiring attribute and more.
  - Label can be set to render behind item model, so it doesn't cover it. Set `PutLabelBehind` option to `1` in order to do that.
  - `LabelMissionItems` option allows items with `ITEM_MISSION` flag to have special mission flag. This option is disabled by default.
  - Label scale can be adjusted in `gothic.ini` with `LabelScale` option.
  - This feature can be disabled in `gothic.ini` with `LabelItems` option.

- Displays a popup when dealing damage.

  - This feature is inspired by [New World](https://www.newworld.com/)'s damage label and based on [AlterDamage](https://github.com/UnresolvedExternal/Union_AlterDamage) popup code.
  - Set `DamagePopupMode` option to `1` for _Alter Damage_ style, `2` for _New World_ style and `0` to disable this feature completely.
  - Popup scale depends on the amount of damage dealt compared to the target's max hp, the fact if the hit was critical or not and `Scale` option from `SystemPack.ini`. Base scale can also be adjusted in `gothic.ini` with `DamagePopupScale`.
  - Icons and base colors are unique for every damage type and each can be separately disabled in `gothic.ini` with `DamagePopupShowIcons` and,`DamagePopupColorDmgTypes`options.
  - By default the number has the same color as the icon, but it can be disabled in `gothic.ini` with `DamagePopupColorOnlyIcon` option.

- Allows killing meatbugs by stepping on them.

  - This feature can be disabled in `gothic.ini` with `TrampleMeatbugs` option.

- Allows to check currently used plugin version through in game console with `zutilities version` command.

### Options

<details>
  <summary>Automatically generated plugin section with default settings.</summary>

```ini
[ZUTILITIES]
TrampleMeatbugs=1
; ... enables (1) or disables (0) a way of killing meatbugs by stepping on them

CenterInvItems=1
; ... enables (1) or disables (0) inventory item rendering in the center of the screen instead of the item description box

UseQuickSave=1
; ... enables (1) or disables (0) QuickSaving with [F10] and QuickLoading with [F12]

MinSaveSlot=15
; ... defines min range of used save slots

MaxSaveSlot=20
; ... defines max range of used save slots

CantSave=The game cannot be saved now!
; ... text appearing when game cannot be saved

CantLoad=The game cannot be loaded now!
; ... text appearing when game cannot be loaded

NoSave=Such a save does not exist!
; ... text appearing when something went wrong and incorrect save slot tried to be loaded

SaveName=QuickSave
; ... name used for quicksaves

ColorNpcs=1
; ... enables (1) or disables (0) coloring of focused Npcs

ColorChests=1
; ... enables (1) or disables (0) coloring of focused Chests

ColorDoors=1
; ... enables (1) or disables (0) coloring of focused Doors

ColorItems=1
; ... enables (1) or disables (0) coloring of focused Items

LabelItems=1
; ... enables (1) or disables (0) inventory item labeling

LabelScale=1.25
; ... defines scale of the label

LabelMissionItems=0
; ... enables (1) or disables (0) labeling of item missions, this will overwrite previous label on any item with ITEM_MISSION flag

PutLabelBehind=0
; ... specifies if the label should be rendered behind the item

DamagePopupMode=1
; ... specifies DamagePopup mode, (0) - Disabled, (1) - 'Alter Damage', (2) - 'New World'

DamagePopupScale=1.10000002
; ... defines base scale of the popup

DamagePopupShowIcons=1
; ... enables (1) or disables (0) icons for the popup

DamagePopupColorDmgTypes=1
; ... enables (1) or disables (0) popup coloring by the damage type

DamagePopupColorOnlyIcon=0
; ... enables (1) or disables (0) coloring only the popup icon
```

</details>
