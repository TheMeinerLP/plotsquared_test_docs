# Event API

### 1. Introduction

PlotSquared uses the [Guava EventBus](https://github.com/google/guava/wiki/EventBusExplained) to register listeners and dispatch events.

### 2. Event List

Events can be found [here](https://intellectualsites.github.io/plotsquared-javadocs/core/com/plotsquared/core/events/package-summary.html).

### 3. Getting an instance

```java
import org.bukkit.Bukkit;
import org.bukkit.plugin.java.JavaPlugin;

public class MyPlotPlugin extends JavaPlugin {
    public static MyPlotPlugin THIS;

    @Override
    public void onEnable() {
        MyPlotPlugin.THIS = this;
        if (Bukkit.getPluginManager().getPlugin("PlotSquared") != null) {
        // Do something
       }
    }
}
```

### 4. Registering a Listener

Registering a listener is super easy. Add the `@Subscribe` (from the `com.google.common.eventbus` package) annotation to any methods that are listening to events, register the class with the EventBus through `PlotAPI#registerListener(Class)` and you’re done! One example:

```java
public class P2Listener {

  // if you like the dependency-injection-like approach:
  public P2Listener(PlotAPI api) {
    api.registerListener(this);
  }

  // less OOP, but if you want to make things easy:
  public P2Listener() {
    PlotAPI api = new PlotAPI();
    api.registerListener(this);
  }

  // A method handling a PlayerEnterPlotEvent
  @Subscribe
  public void onPlayerEnterPlot(PlayerEnterPlotEvent e) {
    //do stuff
  }
}
```