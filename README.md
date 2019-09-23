# Running multiple Unity Editor instances within the same "Project"

When it comes to **multiplayer** game development, we might want to have several instances of Unity running at the same time, without us literally duplicating every single piece of data.

This is especially true when our repositories are huge.

So I created this little Unity tool for Windows to help everybody in doing just this. This solves the famous problem of "Looks like this project is already open" that appears in Unity.

Just put the Editor folder into your project and open the tool in *Window → The Gamedev Guru → Project Instance Creator*

For more explanation, go to the original The Gamedev Guru blog post at [https://thegamedev.guru/multiple-unity-editor-instances-within-a-single-project/](https://thegamedev.guru/multiple-unity-editor-instances-within-a-single-project/)

# Manual steps

1. Create a directory where you want to create a new unity instance project, e.g. _MyGame-Slave-3_

2. Open a command line and enter the new directory you just created

3. Create the junctions you need based on the path to the ORIGINAL_PROJECT_DIRECTORY


To create a junction for the Assets folder:

_mklink /J Assets ORIGINAL_PROJECT_DIRECTORY/Assets_

Example:

*c:\MyProject-Slave-1> mklink /J Assets c:\MyProject\Assets*

# The end

Questions? Create an issue or drop me an e-mail

*P.S. If you need this for Linux/Mac, you'll need to adapt the commands accordingly.*