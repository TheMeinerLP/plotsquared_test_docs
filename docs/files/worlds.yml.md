# worlds.yml

```yaml
configuration_version: v5
worlds:
  # The name of the world
  plotworld:
    plot:
      # The road height above from Y 0
      height: 62
      # The road length around a plot
      size: 42
      # Uses the block bucket format:
      # ex: stone,grass_block
      filling: stone
      # Uses the block bucket format:
      # ex: stone,grass_block
      floor: grass_block
      # Wheather the plot should have a bedrock layer at the bottom
      bedrock: true
      # The plot biome
      biome: FOREST
      # Whether or not plots should be merged
      auto_merge: false
      # Whether or not signs should be created at the corner of a plot
      create_signs: true
      # The material to use for the plot signs.
      sign_material: OAK_WALL_SIGN
    # Configure the wall
    wall:
      # Uses the block bucket format:
      # ex: stone,grass_block
      block: stone_slab
      # Uses the block bucket format:
      # ex: stone,grass_block
      block_claimed: sandstone_slab
      # Uses the block bucket format:
      # ex: stone,grass_block
      filling: stone
      height: 62
      # Wheather or not blocks should be placed on top of the border
      place_top_block: true
    # Configure the road
    road:
      # Road width along a side of a plot
      width: 7
      # Road height from Y 0
      height: 62
      # Uses the block bucket format:
      # ex: stone,grass_block
      block: quartz_block
      # Apply flags for the road within the following pattern:
      # flags:
      #          pvp: true
      #                gamemode: survival
      # Do NOT add them inside the brackets
      flags: {}
    misc_spawn_unowned: false
    # Configure the home
    home:
      # side, center/middle or x,z (relative to the plot) or x,y,z
      default: side
      # side, center/middle or x,z (relative to the plot) or x,y,z
      nonmembers: side
    schematic:
      # Whether or not the user can choose between a schematic when they claim a plot
      specify_on_claim: false
      # Wheather or not the schematic should be pasted on claim
      on_claim: false
      # Define the schematic within the following format:
      # file:
      #                example.schem
      file: 'null'
      schematics: []
    # Command costs
    economy:
      # Can use ANTLR's lexer tokens for dynamic prices
      # See https://worldedit.enginehub.org/en/latest/usage/other/expressions/
      # for a list of supported arguments. The plot variable is referenced as plots
      prices:
        merge: 100
        sell: 100
        claim: 100
      # Wheather or not the setting should be active
      use: false
    # Default plot chat mode (toggled with `/plot toggle chat`)
    chat:
      enabled: false
      # Whather or not plotchat will be on always
      forced: false
    # Limit the number of people that can be added to a plot
    limits:
      max-members: 128
    world:
      # Build height going from Y
      max_height: 256
      min_height: 1
      # Used for the gamemode flag
      gamemode: creative
      # World border expands dynamically
      border: false
    # false = disabled
    event:
      spawn:
        # Wheather or not spawn eggs are enabled
        egg: false
        # Wheather or not breeding is enabled
        breeding: false
        # Wheather or not custom events are enabled
        custom: true
    # Wheather or not natural mob spawning is enabled
    natural_mob_spawning: false
    # Wheather or not spawners are spawning mobs
    mob_spawner_spawning: false
     # Controls the world type / terrain / generator used
    generator:
     type: 0
     terrain: 0
     plugin: PlotSquared
    # Global plot flags, see: https://intellectualsites.github.io/plotsquared-documentation/plot-flags
    flags: {}
```