# Schematic generation

In order to have a plot world generate with schematics do the following:

1. Create a plot schematic with `/plot schematic save`
2. Move the created schematic from `/plugins/PlotSquared/schematics/` to `/plugins/PlotSquared/schematics/GEN_ROAD_SCHEMATIC/<world name>/` and rename it to `plot.schematic`/`plot.schem` (depending on the file extension of the schematic file you’re moving)
3. In `settings.yml`, add/update the following:

```yaml
# Schematic Settings
schematics:
  # Whether schematic based generation should paste schematic on top of plots, or from Y=1
  paste-on-top: false
```

The world will now generate using the schematic.