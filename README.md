# RumblerNetwork
In-development multiplayer networking solution for Godot Engine

## Usage
Download the latest release from the right (RumblerNetworkWin64.zip), and place the contents of the 'Editor' folder into your Godot project.

Add references to the four assemblies in the 'addons' folder into your C# project. You can do this by adding the following in to your .csproj file:
```
	<ItemGroup>
		<Reference Include="Rumbler.General">
			<HintPath>addons\General.dll</HintPath>
		</Reference>
		<Reference Include="Rumbler.General.Networking">
			<HintPath>addons\GeneralNetworking.dll</HintPath>
		</Reference>
		<Reference Include="Rumbler.GodotGeneral">
			<HintPath>addons\GodotGeneral.dll</HintPath>
		</Reference>
		<Reference Include="Rumbler.Network">
			<HintPath>addons\RumblerNetwork.dll</HintPath>
		</Reference>
	</ItemGroup>
```

Edit the contents of the 'RelevantAssemblies.rumbler' file and replace 'NameOfYourAssembly' with the name of your C# Assembly (or asssemblies on multiple lines, if you have multiple)

Add an Autoload (Project Settings -> Globals -> Autoload) for res://Scripts/AutoLoadStartup.cs

## Exporting
When exporting your project, place 'Release/0Harmony.dll' and 'Release/nanosockets.dll' into the root of your exported project folder.

Place the contents of the 'Release/Data/' folder into the 'data_X_windows_x86_64' folder in your exported project folder. Note: **You must do this every time you export your project** (This is only necessary because Godot automatically replaces the assemblies within data_X_windows_x86_64 folder every time you export)

Copy 'RelevantAssemblies.rumbler' and 'MasterServerInfo.rumbler' from your project folder into the root of your exported project folder.

## Libraries
Using https://github.com/nxrighthere/NanoSockets and https://github.com/pardeike/Harmony
