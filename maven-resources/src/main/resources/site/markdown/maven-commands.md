## Maven Commands

### Default
#### Run Test
```bash
mvn clean test
```

#### Generate Project's Site and Publish

-	**site:deploy** goal only deploying the generated site, so need to execute **site** goal beforehand to generate the site.
-	**surefire-report-plugin** will call the **test** goal, so doesn't need to explicitly execute **test** goal to generate jacoco/surefire report.

```bash
mvn clean site site:deploy
```

#### Package Project
```bash
mvn clean package verify
```

#### Deploy to Package Repository
```bash
mvn deploy
```
---

### Versions Maven Plugin
#### Checking for new versions of plugins
To get information about newer versions of plugins that you are using in your build, just invoke the **display-plugin-updates** goal.
```bash
mvn versions:display-plugin-updates
```

#### Checking for new versions of dependencies
To get information about newer versions of dependencies that you are using in your build, just invoke the **display-dependency-updates** goal.
```bash
mvn versions:display-dependency-updates
```

#### Checking for new versions of properties
To get information about newer versions of dependencies that you are using in your build, just invoke the **display-property-updates** goal.
```bash
mvn versions:display-property-updates
```

#### Updating the parent version
To update the parent version of your POM to the latest available, just invoke the **update-parent** goal.
```bash
mvn versions:update-parent
```

#### Updating versions specified by properties
This goal helps when you use properties to define versions. Please see the **update-properties** example.
```bash
mvn versions:update-properties
```

#### Setting the project version
To set the project version to a specific version, just invoke the set goal.
```bash
mvn versions:set -DnewVersion=1.0.1-SNAPSHOT
```

#### Reverting modifications to the pom.xml files
To restore your pom.xml files to their initial state, before you started modifying it with the versions-maven-plugin, invoke the **revert** goal.
Note that it is best practice to use a Source Code Management system and not rely on the **pom.xml.versionsBackup** files created by the versions-maven-plugin.
```bash
mvn versions:revert
```

#### Accepting modifications to the pom.xml files
To accept the modifications made to your pom.xml files by the versions-maven-plugin invoke the **commit** goal. This will have the effect of removing any **pom.xml.versionsBackup** files. 
Note that it is best practice to use a Source Code Management system and not rely on the **pom.xml.versionsBackup** files created by the versions-maven-plugin.
```bash
mvn versions:commit
```

For more information about these, visit https://www.mojohaus.org/versions-maven-plugin/usage.html.