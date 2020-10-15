# UE4 Demo Scene

This directory contains assets and blueprints to run the Demo Scenes in Unreal

## Getting the sources
This repository uses submodules. You need the --recursive option to fetch the submodules automatically:

`$ git clone --recurse-submodules https://gitlab.com/Adjuvo/SenseGlove-Unreal-Demo`

Alternatively:

`$ git clone https://gitlab.com/Adjuvo/SenseGlove-Unreal-Demo`

`$ cd SenseGlove-Unreal-Demo`

`$ git submodule update --init --recursive`

## Updating the submodule plugin
After getting the sources, you'll have the latest plugin by default.
In case the plugin gets updated after that, you can run:

`$ git submodule update --remote`

This will be enough if you are just using the plugin submodule and not developing on it. More information on git's submodules can be found here: https://git-scm.com/book/en/v2/Git-Tools-Submodules

## Prerequisites 
- Unreal Engine V4.25 and upwards
- SenseComm v0.6 and upwards

## Running
Open the Unreal Project file (not the .sln file), it will recompile the source and plugin directory.
In the master branch there are two folders in the Content directory:
1. HandMeshes/ -- compatible .fbx imports 
2. Examples/ -- examples on about grabbing and tracing

## Developing on this repo
Some hints for developing:

- Make sure you are in the master branch `git checkout master`. You can branch from there, for example:
`git branch myNewDemo`

Of course, you can also fork this repo, but make sure you set an upstream link to keep updated!
Pull requests are welcomed.

### Developing with the Unreal Editor / Blueprints
Open the Unreal Project file and it will automatically compile the project and plugin. 

### Developing with Visual Studio / C++
Right click on the Unreal project file and click on `Generate Visual Studio project files`. This will setup your local references correctly. Open the newly generate .sln file. You can debug and build as usual in Visual Studio. 

### Hot reloading with Editor and Visual Studio
Open the editor first and then click on File > Visual Studio. 


