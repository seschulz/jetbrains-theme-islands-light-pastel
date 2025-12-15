# Building the Pastel Theme

## Prerequisites

- JDK 17 or higher
- Gradle 8.5 or higher (or use the wrapper if included)
- IntelliJ IDEA 2025.2 or higher (for testing)

## Build Instructions

### Using Gradle

1. Open a terminal in the project root directory
2. Run the build command:
   ```bash
   ./gradlew build
   ```
   or on Windows:
   ```cmd
   gradlew.bat build
   ```

3. The built plugin will be located at:
   ```
   build/distributions/jetbrains-theme-islands-light-pastel-1.0.0.zip
   ```

### Using IntelliJ IDEA

1. Open the project in IntelliJ IDEA
2. Wait for Gradle to sync (if using build.gradle)
3. Go to **Build > Build Project**
4. The plugin will be compiled and ready for testing

### Gradle Wrapper Setup (if not included)

If you need to set up the Gradle wrapper:

```bash
gradle wrapper --gradle-version 8.5
```

This will create:
- `gradlew` (Unix/macOS)
- `gradlew.bat` (Windows)
- `gradle/wrapper/` directory

## Testing the Theme

### During Development

1. Run the plugin in a sandboxed IDE:
   ```bash
   ./gradlew runIde
   ```

2. A new IntelliJ IDEA window will open with your theme installed
3. Go to Settings > Appearance & Behavior > Appearance
4. Select "Islands Light Pastel" from the theme dropdown

### Installing Locally

1. Build the plugin (see above)
2. In your main IntelliJ IDEA instance:
   - Go to Settings > Plugins
   - Click the gear icon ⚙️
   - Select "Install Plugin from Disk..."
   - Navigate to `build/distributions/pastel-theme-1.0.0.zip`
   - Click OK and restart the IDE

## Available Gradle Tasks

- `./gradlew build` - Build the plugin
- `./gradlew buildPlugin` - Build the plugin distribution
- `./gradlew runIde` - Run IntelliJ IDEA with the plugin
- `./gradlew test` - Run tests (if any)
- `./gradlew clean` - Clean build artifacts
