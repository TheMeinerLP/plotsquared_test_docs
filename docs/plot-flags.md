# Plot flags

### Introduction

The extensive flagging system allows you to do all sorts of things such as setting the plot weather.

Setting a flag is easy, just use `/plot flag set <flag> <value>`. For a boolean flag, the value would either be 'true' or 'false'.

### Default Plot and Road Flags

You can set default flags per world in the `plugins/PlotSquared/config/worlds.yml`. Default flags will be present in each claimed plot unless a different value is manually set for that plot.

The following is an **example** of setting the `use` flag to allow interaction with doors, and trapdoors, levers, gates, pressure plates, buttons and trip wires:

```
worlds:
  <world>:
    [...]
    flags:
      use: "oak_door,iron_trapdoor,lever,acacia_fence_gate,light_weighted_pressure_plate,oak_button,tripwire"
      pvp: true
```

_\`\<world>\` indicates the name of that plotworld._

The same works for road flags.

**Example:**

```
worlds:
  <world>:
    [...]
    road:
      [...]
      flags:
        use: "oak_door,iron_trapdoor,lever,acacia_fence_gate,light_weighted_pressure_plate,oak_button,tripwire"
        pvp: true
```

_\`\<world>\` indicates the name of that plotworld._

### Entity Categories

Flags such as mob caps, interaction flags, etc, make use of entity categories. PlotSquared divides entities in the following categories:

* **animal:** cod donkey squid skeleton\_horse mule trader\_llama parrot zombie\_horse cow horse bee polar\_bear pufferfish cat bat salmon fox pig llama iron\_golem turtle tropical\_fish sheep snow\_golem mooshroom ocelot dolphin chicken wolf panda rabbit
* **hostile:** blaze pillager skeleton giant elder\_guardian zombie\_pigman end\_crystal ravager ghast guardian vindicator magma\_cube spider creeper wither evoker slime illusioner phantom witch wither\_skeleton husk ender\_dragon cave\_spider stray enderman silverfish endermite vex zombie drowned zombie\_villager, shulker
* **player:** player
* **projectile:** ender\_pearl dragon\_fireball fireball wither\_skull llama\_spit fishing\_bobber experience\_bottle egg arrow small\_fireball
* **vehicle:** spawner\_minecart donkey pig llama furnace\_minecart skeleton\_horse mule hopper\_minecart trader\_llama zombie\_horse tnt\_minecart boat chest\_minecart horse command\_block\_minecart minecart
* **villager:** villager wandering\_trader snowball spectral\_arrow shulker\_bullet potion trident
* **hanging:** item\_frame leash\_knot painting
* **other:** dragon\_fireball tnt experience\_orb lightning\_bolt fireball wither\_skull area\_effect\_cloud evoker\_fangs eye\_of\_ender armor\_stand small\_fireball firework\_rocket falling\_block item
* **tamable:** cat trader\_llama parrot zombie\_horse donkey wolf llama horse skeleton\_horse mule

#### BlockTypeList

| Name  | Description                                                                                                             | Default Value |
| ----- | ----------------------------------------------------------------------------------------------------------------------- | ------------- |
| break | Define a list of materials players should be able to break in the plot even when they aren’t added to the plot.         | None          |
| place | Define a list of materials players should be able to place in the plot even when they aren’t added to the plot.         | None          |
| use   | Define a list of materials players should be able to interact with in the plot even when they aren’t added to the plot. | None          |

#### Boolean

| Name                  | Description                                                                                                             | Default Value |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------- |
| animal-attack         | Set to `true` to allow animals to be attacked in the plot.                                                              | False         |
| animal-interact       | Set to `true` to allow animals to be interacted with in the plot.                                                       | False         |
| beacon-effects        | Set to `false` to disable beacon effects on the plot.                                                                   | True          |
| block-burn            | Set to `true` to allow blocks to burn within the plot.                                                                  | False         |
| block-ignition        | Set to `false` to disallow blocks to ignite within the plot.                                                            | True          |
| chat                  | Set to `false` to prevent plot chat on the plot.                                                                        | False         |
| coral-dry             | Set to `true` to allow corals to dry within the plot.                                                                   | False         |
| crop-grow             | Set to `false` to disable crop growing on the plot.                                                                     | True          |
| copper-oxide          | Set to `true` to allow copper to oxide within the plot.                                                                 | False         |
| deny-exit             | Set to `true` to disallow players from exiting the plot.                                                                | False         |
| deny-portal-travel    | Prevents players from travelling across dimensions by using portals.                                                    | False         |
| deny-portals          | Prevents players from creating portals of any kind.                                                                     | False         |
| device-interact       | Set to `true` to allow devices to be interacted with in the plot.                                                       | False         |
| disable-physics       | Set to `true` to disable block physics in the plot.                                                                     | False         |
| drop-protection       | Set to `true` to prevent dropped items from being picked up by non-members of the plot.                                 | False         |
| entity-change-block   | Set to `true` to allow entities to change blocks within the plot, if not covered by other flags.                        | False         |
| explosion             | Set to `true` to allow explosions inside a plot.                                                                        | False         |
| fly                   | Set to `true` to enable flight within the plot.                                                                         | False         |
| forcefield            | Set to `true` to enable member forcefield in the plot.                                                                  | False         |
| grass-grow            | Set to `false` to disable grass to grow within the plot.                                                                | True          |
| hanging-break         | Set to `true` to allow guests to break hanging objects in the plot. Applies to the following entity categories: hanging | False         |
| hanging-place         | Set to `true` to allow guests to hang objects in the plot.                                                              | False         |
| hide-info             | Set to `true` to hide plot information.                                                                                 | False         |
| hostile-attack        | Set to `true` to enable players to attack hostile mobs in the plot.                                                     | False         |
| hostile-interact      | Set to `true` to allow players to interact with hostile mobs in the plot.                                               | False         |
| ice-form              | Set to `true` to allow ice to form in the plot.                                                                         | False         |
| ice-melt              | Set to `true` to allow ice to melt in the plot.                                                                         | False         |
| instabreak            | Set to `true` to allow blocks to be instantaneously broken in survival mode.                                            | False         |
| invincible            | Set to `true` to prevent players from taking damage inside the plot.                                                    | False         |
| item-drop             | Set to `false` to prevent items from being dropped inside the plot.                                                     | True          |
| keep-inventory        | Prevents players from dropping their items when they die inside the plot.                                               | False         |
| kelp-grow             | Set to `false` to disable kelp to grow in the plot.                                                                     | True          |
| leaf-decay            | Set to `false` to prevent leaves from decaying.                                                                         | True          |
| lectern-read-book     | Prevent players taking books from lecterns.                                                                             | False         |
| misc-break            | Set to `true` to allow guests to break miscellaneous items. Applies to the following entity categories: armorstands     | False         |
| misc-place            | Set to `true` to allow guests to place miscellaneous items.                                                             | False         |
| misc-interact         | Set to `true` to allow guests to interact with miscellaneous items. Applies to the following entities                   |               |
| mob-break             | Set to `true` to allow mobs to break blocks within the plot.                                                            | False         |
| mob-place             | Set to `true` to allow mobs to place blocks within the plot.                                                            | False         |
| mycel-grow            | Set to `false` to disable mycelium to grow in the plot.                                                                 | True          |
| no-worldedit          | Set to `true` to disable (FastAsync)WorldEdit usage within the plot.                                                    | False         |
| notify-enter          | Set to `true` to notify the plot owners when someone enters the plot.                                                   | False         |
| notify-leave          | Set to `true` to notify the plot owners when someone leaves the plot.                                                   | False         |
| player-interact       | Set to `true` to allow guests to interact with players in the plot.                                                     | False         |
| pve                   | Set to `true` to enable PVE inside the plot.                                                                            | False         |
| pvp                   | Set to `true` to enable PVP inside the plot.                                                                            | False         |
| prevent-creative-copy | Prevents people from copying item NBT data in the plot unless they’re added as members.                                 | False         |
| projectiles           | Prevents guests from shooting projectiles on the plot when set to false.                                                | False         |
| redstone              | Set to `false` to disable redstone in the plot.                                                                         | True          |
| server-plot           | Set to `true` to turn the plot into a server plot. This is equivalent to setting the server as the plot owner.          | False         |
| snow-form             | Set to `false` to disallow snow to form within the plot.                                                                | False         |
| snow-melt             | Set to `true` to allow snow to melt within the plot.                                                                    | True          |
| soil-dry              | Set to `true` to allow soil to dry within the plot.                                                                     | False         |
| tamed-attack          | Set to `true` to allow guests to attack tamed animals in the plot.                                                      | False         |
| tamed-interact        | Set to `true` to allow guests to interact with tamed animals in the plot.                                               | False         |
| untrusted-visit       | Set to `false` to disallow untrusted players from visiting the plot.                                                    | True          |
| vehicle-break         | Set to `true` to allow guests to break vehicles in the plot.                                                            | False         |
| vehicle-place         | Set to `true` to allow guests to place vehicles in the plot.                                                            | False         |
| vehicle-use           | Set to `true` to allow guests to use vehicles in the plot. Applies to the following entity categories: vehicle          | False         |
| villager-interact     | Set to `true` to allow guests to interact with villagers in the plot.                                                   | False         |
| vine-grow             | Set to `false` to disable vines to grow within the plot.                                                                | True          |

#### Double

| Name  | Description                                                                                                                               | Default Value |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| price | If set a plot can be bought for this price using `/plot buy`. Requires economy to be enabled and lists plots under `/plots list forsale`. | Not Buyable   |

#### Enum

| Name          | Description                                                                                                              | Default Value |
| ------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------- |
| deny-teleport | Deny a certain group from teleporting to the plot. Available groups: members, nonmembers, trusted, nontrusted, nonowners | None          |
| liquid-flow   | Set to `false` to disable liquid flowing.                                                                                | None          |
| titles        | Set to `true` to allow the plot title when someone enters the plot.                                                      | None          |
| weather       | Specifies the simulated weather inside the plot. This hasn’t an effet of weather dependent game mechanics.               | None          |

#### Integer

| Name        | Description                                                                                                                                               | Default Value |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| animal-cap  | Set to an integer value to limit the amount of animals on the plot. Applies to the following entity categories: animal, villager, tamable                 | Infinity      |
| entity-cap  | Set to an integer value to limit the amount of entities on the plot.                                                                                      | Infinity      |
| hostile-cap | Set to an integer value to limit the amount of hostile entities on the plot. Applies to the following entity categories: hostile                          | Infinity      |
| misc-cap    | Set to an integer value to limit the amount of miscellaneous entities on the plot. Applies to the following entity categories: projectile, other, hanging | Infinity      |
| mob-cap     | Set to an integer value to limit the amount of mobs on the plot. Applies to the following entity categories: animal, villager, tamable, hostile           | Infinity      |
| vehicle-cap | Set to an integer value to limit the amount of vehicles on the plot. Applies to the following entity categories: vehicle                                  | Infinity      |
| time        | Specifies the simulated time inside the plot. This has no effect of time dependent game mechanics.                                                        | Disabled      |

#### Internal

| Name     | Description                          | Default Value |
| -------- | ------------------------------------ | ------------- |
| analysis | A multi purpose debug analysis flag. | Null          |
| done     | Mark a plot as done.                 | Null          |

#### Miscellaneous

| Name           | Description                                                | Default Value |
| -------------- | ---------------------------------------------------------- | ------------- |
| blocked-cmds   | A list of commands that are blocked in the plot.           | None          |
| gamemode       | Determines the gamemode in the plot.                       | None          |
| guest-gamemode | Determines the guest gamemode in the plot.                 | None          |
| music          | Set to a music disk ID (item name) to play the music disc. | None          |

#### String

| Name        | Description                                                                                        | Default Value |
| ----------- | -------------------------------------------------------------------------------------------------- | ------------- |
| description | Plot description.                                                                                  | None          |
| farewell    | Message sent to players when leaving the plot.                                                     | None          |
| greeting    | Message sent to players on plot entry.                                                             | None          |
| plot-title  | Set the pop-up title’s title and subtitle. Format: `/plot flag set title "A title" "The subtitle"` | None          |

#### Timed

| Name | Description                                                                                                                                | Default Value |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------- |
| feed | Specify an interval in seconds and an optional amount by which the players will be fed (amount is 0 by default = vanilla-regeneration).    | None          |
| heal | Specify an interval in seconds and an optional amount by which the players will be healed (amount is 0 by default = vanilla-regeneration). | None          |