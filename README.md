# Forge-API-Documentation
Minecraft is written in Java. One way to mod minecraft is to use Forge API to interact with Minecraft's native codes. To understand these API's, I compiled the latest Forge Mod on my computer and generated HTML documentation pages using javadoc

[Version 1.16.5-36.1.2](https://ziyuanzhao2000.github.io/Forge-API-Documentation/javadoc/)


By the way, you may be interested in generating these API documentation pages for yourself because Forge updates rather quickly over the years, and some keywords or methods in one version may be changed in the next. This is not too hard. First you need to know how to set up modding environment on your PC. Download Ecllipse or IntelliJ. I used IntelliJ. Then clone the version of Forge you need from Git. There will be build.gradle file in the unzipped folder. Use that to create a new project, and allow some time for the workspace to be set properly. Then execute commands: first ./gradlew genIntellijRuns within the IDE environment. This sets up run configuration and download additional assets. Think like this: Forge interacts with native Minecraft codes, but the copy we cloned from Git does not necessarily have the relevant codes, so we need to download additional stuff. Wait for upto 15 minutes for the download to complete. Then execute ./gradlew setup to setup the work space.

Okay. For the final step, run ./gradlew javadoc. This fires up a gradle script specifically made to handle the .java files in the deep folders. I've tried painstakingly to make the html by running javadoc from commandline, to no avail, so don't waste time like I did. Then wait for 5-10 minutes for the command to execute. You will see warnings and perhaps error messages. Eventually, if it tells you something is wrong, don't panic, you should actually have the javadoc generated. It's in the /projects/forge/build/docs/javadoc folder (that's darn deep!). Clicking into the index.html and you will see the thing! However, this should be used in complementation with Forge's documentation online, at: https://mcforge.readthedocs.io/en/1.15.x/ (for current versions), which has more explanations though less technical details.

Finally, credits to [Taylor](https://github.com/taylorgoolsby/forge-javadocs), [Neko](https://github.com/Nekoyue/ForgeJavaDocs-NG), and [diesieben07](https://forums.minecraftforge.net/topic/99311-trouble-with-initializing-a-new-item-for-registry/?tab=comments#comment-448794) for their helpful information so that I can figure this out.
