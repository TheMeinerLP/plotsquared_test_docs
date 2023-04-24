# Plot Backups

PlotSquared v5.11.0 introduced a new plot backup system. This allows you to create backups of your plots, which can be restored at a later point.

!!! warning "The system does (currently) not work for merged plots."

By default, the system will also create backups of the plot when certain potentially destructive actions are performed. These currently include:

* Clearing the plot
* Setting a plot component (floor, filling, etc)

The backup system currently only stores blocks inside the plot, and will not include things such as flags, settings, etc. The backup system uses plot schematics behind the scenes.