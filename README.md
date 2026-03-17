
# atak-5.6-plugin-template

This is a clean, "blank slate" template for developing private ATAK plugins. It is based on the ATAK 5.6.0 SDK and follows modern plugin development patterns.

Repository: https://github.com/aegorsuch/atak-5.6-plugin-template

## Getting Started

- **ATAK SDK:** This template assumes you are working within an ATAK SDK environment.
- **Android Studio:** Latest stable version recommended.
- **JDK 17:** Required for ATAK 5.x development.

### 2. How to Use This Template
- **GitHub:** Click the **"Use this template"** button to create a new repository based on this code.
- **Manual:** Copy this directory to your `plugins/` folder in the ATAK SDK.

### 3. New Plugin Initialization Checklist
Follow these steps immediately after creating your new repository to personalize it:

- [ ] **Rename Package:** Right-click `com.atakmap.android.helloworld` in Android Studio -> **Refactor** -> **Rename** to your new package name (e.g., `com.atakmap.android.mytool`).
- [ ] **Update build.gradle:** In `app/build.gradle`, update the `namespace` to match your new package name.
- [ ] **Update Manifest:** In `app/src/main/AndroidManifest.xml`, update all activity and service paths.
- [ ] **Update plugin.xml:** In `app/src/main/assets/plugin.xml`, update the `impl` attribute to point to your new `Lifecycle` class.
- [ ] **Change App Name:** Update `app_name` and `hello_world` strings in `app/src/main/res/values/strings.xml`.
- [ ] **Update README:** Replace this template's README with your plugin's specific documentation.

## Key Concepts

### Context Management
ATAK plugins deal with two types of `Context`:
- **Plugin Context:** Used to resolve resources (layouts, strings, drawables) from your plugin APK.
- **MapView Context:** Used for UI elements like `AlertDialog`, `Toast`, and graphics access.

### Lifecycle & Tools
- `HelloWorldLifecycle`: Manages the plugin's entry point and initialization.
- `HelloWorldTool`: Defines the plugin's presence in the ATAK toolbar/menu.

## Build and Deploy
Run the following to build the APK:
```bash
./gradlew assembleCivDebug
```
The resulting APK will be located in `app/build/outputs/apk/civ/debug/`.


---
*Note: This template is provided as-is for the ATAK development community.*
