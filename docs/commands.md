# Commands

#### SETOWNER

Set the plot owner.

**Usage:** `/plot [[world;]X;Z] setowner <player>`

**Aliases:** `[ owner, so, seto ]`

**Permissions:**

Primary:

* `plots.admin.command.setowner`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Owner.java)

#### ADD

With this command you "add him" to the whitelist of the plot. Allow a user to build in a plot while the plot owner is online.

**Usage:** `/plot [[world;]X;Z] add <player | *>`

**Permissions:**

Primary:

* `plots.add` - Access to the command `/plot add`
* `plots.add.<amount>` - Specifying the amount of people the plot owner can add

Secondary:

* `plots.admin.command.add` - Administrative override
* `plots.add.everyone` - Access to add everyone

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Add.java)

#### TRUST

Whith this command you "add him" to the whitelist of the plot. It gives the added user more permissions as the normal ADD command: it allow a user to build in a plot every time and use WorldEdit while the plot owner is offline.

**Usage:** `/plot [[world;]X;Z] trust <player | *>`

**Aliases:** `[ t ]`

**Permissions:**

Primary:

* `plots.trust` - Access to the command `/plot trust`
* `plots.trust.<amount>` - Specifying the amount of people the plot owner can trust

Secondary:

* `plots.admin.command.trust` - Administrative override
* `plots.trust.everyone` - Access to trust everyone

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Trust.java)

#### REMOVE

Remove a player from a plot. This include the player whitelist (ADD, TRUST) and the blacklist (DENY) of the plot.

**Usage:** `/plot [[world;]X;Z] remove <player | *>`

**Aliases:** `[ r, untrust, ut, undeny, ud, unban ]`

**Permissions:**

Primary:

* `plots.remove` - Access to the command `/plot remove`

Secondary:

* `plots.admin.command.remove` Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Remove.java)

#### DENY

Deny a user from entering a plot. With this command you "add him" to the blacklist of the plot.

**Usage:** `/plot [[world;]X;Z] deny <player | *>`

**Aliases:** `[ d, ban ]`

**Permissions:**

Primary:

* `plots.deny` - Access to the command `/plot deny`
* `plots.deny.<amount>` - Specifying the amount of people the plot owner can deny

Secondary:

* `plots.admin.command.deny` - Administrative override
* `plots.admin.entry.denied` - Administrative override to bypass plot deny
* `plots.deny.everyone` - Access to deny everyone

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Deny.java)

#### GRANT

Manage plot grants.

**Usage:** `/plot grant <check | add> [player]`

**Permissions:**

* `plots.grant` - Access to the command `/plot grant`
* `plots.grant.add` - Access to the command `/plot grant add`
* `plots.grant.check` - Access to the command `/plot grant check`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Grant.java)

#### KICK

Kick a player from your plot.

**Usage:** `/plot [[world;]X;Z] kick <player | *>`

**Aliases:** `[ k ]`

**Permissions:**

Primary:

* `plots.kick` - Access to the command `/plot kick`

Secondary:

* `plots.admin.command.kick` - Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Kick.java)

#### MERGE

Merge the plot you are standing on with another plot.

**Usage:** `/plot [[world;]X;Z] merge <all | n | e | s | w> [removeroads]`

**Aliases:** `[ m ]`

**Permissions:**

Primary:

* `plots.merge` - Access to the command `/plot claim`

Secondary:

* `plots.merge.<amount>` - Limit the amount of plots a player can merge to a mega plot
* `plots.admin.command.merge` - Administrative override
* `plots.merge.other` - Access to merge the plot with other people
* `plots.merge.keeproad` - Access to use the keeproad argument

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Merge.java)

#### UNLINK

Unlink a mega-plot (merged plot)

**Usage:** `/plot [[world;]X;Z] unlink [createroads]`

**Aliases:** `[ u, unmerge ]`

**Permissions:**

Primary:

* `plots.unlink` - Access to the command `/plot unlink`

Secondary:

* `plots.admin.command.unlink` - Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Unlink.java)

#### SETHOME

Set the plot-home you’re standing on. The plothome is the position where the player will teleported if he use the `/plot home` or `/plot visit` command. With the argument `none` you reset the position.

**Usage:** `/plot [[world;]X;Z] set home [none]`

**Aliases:** `[ sh, seth, sethome ]`

**Permissions:**

* `plots.set.home` - Access to the command `/plot set home`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/SetHome.java)

#### ALIAS

Set the plot name

**Usage:**

* `/plot [[world;]X;Z] alias set <alias>`
* `/plot [[world;]X;Z] alias remove <alias>`

**Aliases:** `[ setalias, sa, name, rename, setname, seta, nameplot ]`

**Permissions:**

Primary:

* `plots.alias.set` - Access to the command `/plot alias set`
* `plots.alias.remove` - Access to the command `/plot alias remove`

Secondary:

* `plots.admin.alias.set` - Administrative override to set an alias
* `plots.admin.alias.remove` - Administrative override to remove an alias

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Alias.java)

#### SETDESCRIPTION

Set the plot description

**Usage:** `/plot [[world;]X;Z] desc <description>`

**Aliases:** `[ setdescription, setdesc, setd, description ]`

**Permissions:** `plots.set.desc` - Access to the command `/plot set description`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Desc.java)

#### MUSIC

Player music in a plot

**Usage:** `/plot [[world;]X;Z] music`

**Permissions:** `plots.music` - Access to the command `/plot music`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Music.java)

#### SETBIOME

List all possible biomes or change the plot biome. (You can change the biome with WorldEdit / FAWE too.) If you clear or delete the plot, you reset the biom setting too, so the default biome (changeable in the `worlds.yml`) will be used.

**Usage:** `/plot [[world;]X;Z] biome [biome]`

**Aliases:** `[ biome, sb, setb, b ]`

**Permissions:** `plots.set.biome` - Access to the command `/plot set biome`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Biome.java)

#### SETFLAG

Manage plot flags.

**Usage:**

Primary:

* `/plot [[world;]X;Z] flag`

Secondary:

* `/plot [[world;]X;Z] flag info <flag>`
* `/plot [[world;]X;Z] flag set <flag> <value>`
* `/plot [[world;]X;Z] flag add <flag> <values>`
* `/plot [[world;]X;Z] flag remove <flag> [values]`

**Aliases:** `[ f, flag ]`

**Permissions:**

Primary:

* `plots.flag` - Access to the command `/plot flag`

Secondary:

* `plots.set.flag` - Access to the command `/plot set flag`
* `plots.flag.remove` - Access to the command `/plot flag remove`
* `plots.flag.add` - Access to the command `/plot flag add`
* `plots.set.flag.other` - Access to set flag on other people’s plots
* `plots.set.flag.<arg>` - Access to the command `/plot set flag <arg>`
* `plots.flag.list` - Access to the command `/plot flag list`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/FlagCommand.java)

#### DONE

Mark a plot as done

**Usage:** `/plot [[world;]X;Z] done`

**Aliases:** `[ submit ]`

**Permissions:**

Primary:

* `plots.done` - Access to the command `/plot done`

Secondary:

* `plots.admin.command.done` - Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Done.java)

#### CONTINUE

Continue a plot that was previously marked as done

**Usage:** `/plot [[world;]X;Z] continue`

**Permissions:**

Primary:

* `plots.continue` - Access to the command `/plot continue`

Secondary:

* `plots.admin.command.continue` - Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Continue.java)

#### TOGGLE

Toggle per user settings

**Usage:** `/plot [[world;]X;Z] toggle <chat | chatspy | clear-confirmation | time | titles | worldedit>`

**Permissions:**

Primary:

* `plots.use` - Access to the command `/plot toggle`

Secondary:

* `plots.admin.command.chat` - Access to the command `/plot toggle chat-spy`
* `plots.worldedit.bypass` - Access to the command `/plot wea`
* `plots.toggle.chat` - Access to the command `/plot chat`
* `plots.admin.command.autoclear` - Access to the command `/plot toggle clear-confirmation`
* `plots.toggle.titles` - Access to the command `/plot toggle titles`
* `plots.toggle.time` - Access to the command `/plots toggle time`
* `plots.toggle.debug` - Access to the command `/plots toggle debug`
* `plots.admin.debug.other` - Administrative override to toggle the debugmode for other players

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Toggle.java)

#### SET

Set a plot value

**Usage:** `/plot [[world;]X;Z] set <biome | alias | home | floor | wall | all | air | main | middle | outline | border> <value...>`

**Aliases:** `[ s ]`

**Permissions:**

Primary:

* `plots.set` - Access to the command `/plot set`

Secondary:

* `plots.set." + <component>`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Set.java)

#### COPY

Copy a plot.

**Usage:** `/plot [[world;]X;Z] copy <X;Z>`

**Aliases:** `[ copypaste ]`

**Permissions:**

Primary:

* `plots.copy` - Access to the command `/plot copy`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Copy.java)

#### MOVE

Move a plot.

**Usage:** `/plot [[world;]X;Z] move <X;Z>`

**Permissions:**

Primary:

* `plots.move` - Access to the command `/plot move`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Move.java)

#### SWAP

Swap two plots.

**Usage:** `/plot [[world;]X;Z] swap <X;Z>`

**Aliases:** `[ switch ]`

**Permissions:**

Primary:

* `plots.swap` - Access to the command `/plot swap`

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Swap.java)

#### BACKUP

Manage plot backups

**Usage:** `/plot [[world;]X;Z] backup <save | list | load>`

**Permissions:**

Primary:

* `plots.backup` - Access to the command `/plot backup`

Secondary:

* `plots.backup.save` - Access to the command `/plot backup save`
* `plots.backup.load` - Access to the command `/plot backup load`
* `plots.backup.list` - Access to the command `/plot backup list`
* `plots.admin.backup.other` - Administrative override to manage backups at other plots

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Backup.java)

#### CLEAR

Clear the plot you stand on. It doesn’t reset any plot settigns or flag (with exception of the biome setting).

**Usage:** `/plot [[world;]X;Z] clear`

**Aliases:** `[ reset ]`

**Permissions:**

Primary:

* `plots.clear` - Access to the command `/plot clear`

Secondary:

* `plots.admin.command.clear` - Administrative override

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Clear.java)

#### DELETE

Delete the plot you stand on.

**Usage:** `/plot [[world;]X;Z] delete`

**Aliases:** `[ dispose, del ]`

**Permissions:**

Primary:

* `plots.delete` - Access to the command `/plot delete`

Secondary:

* `plots.admin.command.delete` - Administrative override to delete plots.

**Source Code:** [here](https://github.com/IntellectualSites/PlotSquared/tree/v6/Core/src/main/java/com/plotsquared/core/command/Delete.java)