# API Documentation

**🏠 Return to the index**

### 2. Maven & Gradle Examples <a href="#_maven_gradle_examples" id="_maven_gradle_examples"></a>

* Javadocs: [https://intellectualsites.github.io/plotsquared-javadocs/](https://intellectualsites.github.io/plotsquared-javadocs/)
* Major upgrade diff: [https://intellectualsites.github.io/plotsquared-api-diff/](https://intellectualsites.github.io/plotsquared-api-diff/)

!!! tip " Gradle is the recommended when working with the PlotSquared API. Ensure the [toolchain](https://docs.gradle.org/current/userguide/toolchains.html) points to Java 17 or higher."

#### 2.1. Gradle - PlotSquared Core

If you need to access the Bukkit module of PlotSquared, copy the example below.

```kt
repositories {
    mavenCentral()
    maven { url = uri("https://repo.papermc.io/repository/maven-public/") }
}

dependencies {
    implementation(platform("com.intellectualsites.bom:bom-1.18.x:1.27"))
    compileOnly("com.plotsquared:PlotSquared-Core")
}
```

#### 2.2. Gradle - PlotSquared Core and Bukkit

```kt
repositories {
    mavenCentral()
    maven { url = uri("https://repo.papermc.io/repository/maven-public/") }
}

dependencies {
    implementation(platform("com.intellectualsites.bom:bom-1.18.x:1.27"))
    compileOnly("com.plotsquared:PlotSquared-Core")
    compileOnly("com.plotsquared:PlotSquared-Bukkit") { isTransitive = false }
}
```

#### 2.3. Maven - PlotSquared Core

```xml
<repositories>
    <repository>
        <id>papermc</id>
        <url>https://repo.papermc.io/repository/maven-public/</url>
    </repository>
</repositories>
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>com.intellectualsites.bom</groupId>
            <artifactId>bom-1.18.x</artifactId>
            <version>1.27</version>
            <scope>import</scope>
            <type>pom</type>
        </dependency>
    </dependencies>
</dependencyManagement>
<dependencies>
    <dependency>
        <groupId>com.plotsquared</groupId>
        <artifactId>PlotSquared-Core</artifactId>
        <scope>provided</scope>
    </dependency>
</dependencies>
```

#### 2.4. Maven - PlotSquared Core and Bukkit

```xml
<repositories>
    <repository>
        <id>papermc</id>
        <url>https://repo.papermc.io/repository/maven-public/</url>
    </repository>
</repositories>
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>com.intellectualsites.bom</groupId>
            <artifactId>bom-1.18.x</artifactId>
            <version>1.27</version>
            <scope>import</scope>
            <type>pom</type>
        </dependency>
    </dependencies>
</dependencyManagement>
<dependencies>
    <dependency>
        <groupId>com.plotsquared</groupId>
        <artifactId>PlotSquared-Core</artifactId>
        <scope>provided</scope>
    </dependency>

    <dependency>
        <groupId>com.plotsquared</groupId>
        <artifactId>PlotSquared-Bukkit</artifactId>
        <scope>provided</scope>
        <exclusions>
            <exclusion>
                <artifactId>PlotSquared-Core</artifactId>
                <groupId>*</groupId>
            </exclusion>
        </exclusions>
    </dependency>
</dependencies>
```

### 4. Terminology <a href="#_terminology" id="_terminology"></a>

#### 4.1. Plot area <a href="#_plot_area" id="_plot_area"></a>

A plot area is any area that PlotSquared will manage/handle. If this is an infinite plot world, the entire world is considered to be a plot area. If you use plot clusters, then only part of the world will be a plot area, and anything outside this area will not be handled by PlotSquared.

#### 4.2. Clusters <a href="#_clusters" id="_clusters"></a>

Clusters can be created within existing plot areas, or they can be created in a previously non-plot world, which will in turn create it’s own plot area.

#### 4.3. Road <a href="#_road" id="_road"></a>

A road is what separates each plot, and includes the wall around each plot. Attempting to get a plot at this location will return null.

#### 4.4. Plot <a href="#_plot" id="_plot"></a>

A plot can be claimed or unclaimed. Getting a plot at a location where one isn’t claimed will return a new unowned plot object.