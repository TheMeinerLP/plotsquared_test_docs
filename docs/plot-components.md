# Plot components

#### /plot set biome

This is an alias for `/plot setbiome` and has the permission node `plots.set.biome`. From v5.11.0 this has full command completion.

#### /plot set alias

This is an alias for `/plot setalias` and has the permission node `plots.alias`. This changes the name of the plot as displayed in lists, and allows you to do `/plot visit <alias>`

#### /plot set home

This is an alias for `/plot sethome` and has the permission node `plots.set.home`.

If no argument is given, the plot home location will be set to your current location. To remove the custom home location use `/plot sethome unset/reset/remove/none`.

#### /plot set \<component>

This allows you to update various parts of the plot. The components that exist are:

* `main`: Blocks in the area under the plot floor
* `floor`: Blocks in the plot floor
* `air`: Blocks in the area above the plot floor
* `all`: All blocks in a plot
* `wall`: Blocks inside of plot wall
* `border`: Blocks in the plot border
* `outline`: Blocks in the area surrounding the plot
* `middle`: The block(s) in the middle of the plot

Each component has a separate permission node, namely `plots.set.<component>`, and they share the syntax `/plot set <component> <pattern>`.

This is a powerful system as it allows you to use the power of BlockBuckets to define block-patterns.