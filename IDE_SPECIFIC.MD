**Note: For**

VS Code
---
*VS Code is officially supported by FRC*

To use in Visual Studio Code, make sure you're using the version installed through the [WPILibInstaller](https://github.com/wpilibsuite/allwpilib/releases) or at least have the proper extensions installed. 

Head to `File > Open Folder`.
![](https://user-images.githubusercontent.com/9660418/50732000-cefb6980-1136-11e9-8296-249496dd2332.png) 

Select the project folder then the project should be opened.

![image](https://user-images.githubusercontent.com/9660418/50732149-45e63180-113a-11e9-9e25-19046b57b697.png)


Check out [this WPI ScreenSteps Live page](https://wpilib.screenstepslive.com/s/currentCS/m/java/l/1027063-building-and-deploying-to-a-roborio) on instructions on how to build and deploy

IntelliJ
---
*Note: The IntelliJ module is by default named `java` regardless of the directory name. It will work just fine. However if you wanted to change it, then delete all IntelliJ specific files (\*.iml, \*.ipr, \*.iws) and run the Gradle task `idea` to regenerate them with the proper module name.*

To use in IntelliJ, head to `File > Open...` or if you're on the Welcome Screen, hit `Open`

![image](https://user-images.githubusercontent.com/9660418/50732085-f5220900-1138-11e9-9988-7b07be0883dc.png)
or
![image](https://user-images.githubusercontent.com/9660418/50732101-4631fd00-1139-11e9-9bd8-f1abb84380cf.png)


Select the project folder then the project should open.

Make sure you import the Gradle project or even enable auto-import so that the Gradle config is read by IntelliJ's integration with it and utilized.

![image](https://user-images.githubusercontent.com/9660418/50732169-c86ef100-113a-11e9-8642-5d9f975b48c9.png)

Use the run configurations on the top right to run Gradle tasks.

![image](https://user-images.githubusercontent.com/9660418/50732180-02d88e00-113b-11e9-8a70-19a4a12178bd.png)

Eclipse
---
To use in Eclipse, head to `File > Open Projects from File System...`

![image](https://user-images.githubusercontent.com/9660418/50732199-6c589c80-113b-11e9-86ce-0b9d8fa1174e.png)

Select the project folder then the project should open after you hit `Finish`. You will have to close the welcome tab if you're on it to see the project.

![image](https://user-images.githubusercontent.com/9660418/50732208-a9bd2a00-113b-11e9-8fbb-c52db4e99208.png)

Right click on any part of the project in the Package Explorer and click `Configure Build Path...`

![image](https://user-images.githubusercontent.com/9660418/50732211-c48f9e80-113b-11e9-946d-d4998a5bb1a7.png)

Navigate to the `Libraries` tab, select `JRE System Library [JavaSE-11](unbound)`, and hit `Edit...`.

![image](https://user-images.githubusercontent.com/9660418/50732220-f4d73d00-113b-11e9-9834-1959f4c347f3.png)

Select the `Alternate JRE:` option and click on Installed JREs... 
![image](https://user-images.githubusercontent.com/9660418/50732227-1afcdd00-113c-11e9-82f0-a59e23de22a9.png)

It will list the JREs configured or autodetected with or by Eclipse. Click `Add...` if the supported JDK version (Java 1.11 in FRC 2019) for your target FRC year isn't already there. If it already is, make sure it's selected and skip the unnecessary steps below.

![image](https://user-images.githubusercontent.com/9660418/50732231-3667e800-113c-11e9-9414-4a2d5f592e8b.png)

After clicking `Add...`, select `Standard VM`.

![image](https://user-images.githubusercontent.com/9660418/50732236-6911e080-113c-11e9-9e65-71184126a9b5.png)

Select your JDK path. Don't use a JRE as a JDK installation is required to compile Java code. In 2019, if you used the [WPILibInstaller](https://github.com/wpilibsuite/allwpilib/releases) on windows, it installs JDK 11 to `C:/Users/Public/frc2019/jdk` or `%userprofile%/frc2019/jdk` depending on if you installed it for all users or just one. It doesn't matter what you name the JDK in Eclipse but it would be useful to include the JDK version in it for later reference.

![image](https://user-images.githubusercontent.com/9660418/50732254-fb19e900-113c-11e9-8de2-00e69d39cde0.png)

Finish that dialog. Make sure it's selected in the underlying dialog. Then hit `Apply and Close` or `Finish` on the rest of the dialogs.

![image](https://user-images.githubusercontent.com/9660418/50732265-23a1e300-113d-11e9-89de-f1d411b920c8.png)

In your project, you should see the JDK just added.

![image](https://user-images.githubusercontent.com/9660418/50732274-47fdbf80-113d-11e9-8fea-152d035b1bcf.png)

To run Gradle tasks, first make sure you have **at least one file selected in the project first** (as the Run Configurations in Eclipse depend on the project directory and can't detect it on its own). 

![image](https://user-images.githubusercontent.com/9660418/50732308-ef7af200-113d-11e9-99d0-fb8a36d21e77.png) *(note the blue selection highlight)*

Then click the arrow to the right of the green circle with a white arrow in it. Then hit `Run Configurations`. 

![image](https://user-images.githubusercontent.com/9660418/50732296-9f039480-113d-11e9-9c1d-29da1ced92d9.png)

Select any of the Gradle run configurations, I would recommend `Build` or one of the application launch configs to test it for the first time.

![image](https://user-images.githubusercontent.com/9660418/50732317-176a5580-113e-11e9-8479-fae4cf9f7b9e.png)

Press run at the bottom.

![image](https://user-images.githubusercontent.com/9660418/50732319-25b87180-113e-11e9-9ab8-e707d793a31c.png)

Some of the run configurations will show up in the dropdown for run configurations after you run them for the first time. So you want need to navigate to the `Run Configurations...` menu to run them anymore.

No IDE / Other IDE
---
As this project uses Gradle, you can use any IDE you want or even no IDE (plain old Notepad would work). However you will need some type of terminal to execute the gradle wrapper and run tasks (ex: `./gradlew.bat build` in Windows Command Prompt or PowerShell, `./gradlew build` on *NIX OSes).
