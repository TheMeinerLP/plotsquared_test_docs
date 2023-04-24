# Plot component presets

### Introduction

PlotSquared v5.12.0 introduced a new component preset system. The new system allows server owners to make component presets that players can then apply to their plots via a GUI. The GUI menu overrides player specific permissions. Thus, you can use the GUI to let players use components that they’re not normally permitted to use.

### Components

The components available - and the values you can use - are the same as those in the `/plot set <component>` command.

Available components:

* floor
* wall
* all
* air
* main
* middle
* outline
* border

### Configuration

The system is toggled in the `settings.yml` file under `enabled-components`. It is enabled by default.

Presets are configured in the file `plugins/PlotSquared/settings/components.yml`:

```yaml
presets:
  - component: floor
    cost: 0.0
    pattern: '##wool'
    name: <rainbow:2>Disco Floor</rainbow>
    icon: yellow_wool
    description:
      - <gold>Spice up your plot floor</gold>
    permission: ''
```

This is a powerful system as it allows you to use the power of BlockBuckets to define block-patterns.

### Cost

If a non-zero cost is defined and both [Vault](https://www.spigotmc.org/resources/vault.34315/) and an economy plugin is present, the GUI will charge using the in-game currency.

### Icons

### Permission

The player won’t be able to see presets that they are not permitted to use. If the permission is set to `''` (an empty string) then all players will be able to use that preset.

### /plot components

The command for opening the GUI is `/plot components` and has the permission node `plots.components`.

Using this command will bring up the GUI menu, but only if the player is in a plot that they own.

![component\_small.png](https://i.imgur.com/brFlzw6.png)