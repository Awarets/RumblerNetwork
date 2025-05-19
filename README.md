# RumblerNetwork
In-development multiplayer networking solution for Godot Engine

## Usage
Download the latest release from the right (RumblerNetworkWin64.zip), and place the contents of the 'Editor' folder into your Godot project.

Edit the contents of the 'RelevantAssemblies.rumbler' file and replace 'NameOfYourAssembly' with the name of your C# Assembly (or asssemblies on multiple lines, if you have multiple)

Add an Autoload (Project Settings -> Globals -> Autoload) for res://Scripts/AutoLoadStartup.cs

## Exporting
When exporting your project, place '0Harmony.dll' and 'nanosockets.dll' into the root of your exported project folder.

Place the contents of the 'Data' folder into the 'data_X_windows_x86_64' folder in your exported project folder. Note: **You must do this every time you export your project** (This is only necessary because Godot automatically replaces the assemblies within data_X_windows_Y folder every time you export)

Copy 'RelevantAssemblies.rumbler' and 'MasterServerInfo.rumbler' from your project folder into the root of your exported project folder.

## Libraries
Using https://github.com/nxrighthere/NanoSockets and https://github.com/pardeike/Harmony
