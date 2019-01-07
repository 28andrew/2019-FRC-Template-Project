Template FRC Java Project
---

A Gradle-based Java project that may be used in VS Code, IntelliJ, and Eclipse. It utilizes the [GradleRIO](https://github.com/wpilibsuite/GradleRIO) plugin which is the method of building for the FRC 2019 season (and likely beyond). This template is based on the project template provided by WPI extension in VS Code but with many changes to support more IDEs consistently.

*Currently should work for the 2019 FRC Season!*

Usage
---
To use, clone this repository then rename the folder to the name of your project (ex: DeepSpaceRobot). Then in `build.gradle`, `Main.java`, `Robot.java`, the package folder (`src/main/java/frc/####/robot`), `.wpilib/wpilib_preferences.json`, replace any instances of `4277` with your FRC team's number. **[Next, follow the IDE-specific instructions to setup your IDE (or for instructions for a lack of an IDE)](IDE_SPECIFIC.MD)** and for IDE-specific usage. If you plan to support IntelliJ, read the note under it. Multiple different IDEs may use the same project. 

JSON files for the KauaiLabs NavX Library and CTRE Phoenix Framework are included in `vendordeps`. You may want to update the JSON files by running the installer as listed below. Then copy and paste the .json files from `C:/Users/Public/frc2019/vendordeps` or `%userprofile%/frc2019/vendordeps` or in the directory for your specific OS to the project's `vendordeps` folder.

If you need CTRE, make sure you run the [Phoenix Framework Installer](http://www.ctr-electronics.com/hro.html#product_tabs_technical_resources) and use the Tuner program on your RoboRIO.
If you need NavX, make sure you run the [NavX-MXP Installer](https://www.kauailabs.com/public_files/navx-mxp/navx-mxp.zip)

Java source code belongs in `src/main/java`. Read `src/main/deploy/example.txt` on how to deploy other files to the RoboRIO and how to reference them in code.
