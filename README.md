# UE4 Demo Scene

This directory contains assets and blueprints to run the Demo Scenes in Unreal

## Current status
master branch: ![badge](https://gitlab.com/senseglove/ue4-senseglove-demo-scene/badges/master/pipeline.svg "status")

## Getting the sources
This repository uses submodules. You need the --recursive option to fetch the submodules automatically:

`$ git clone --recurse-submodules https://gitlab.com/senseglove/ue4-senseglove-demo-scene`

Alternatively:

`$ git clone https://gitlab.com/senseglove/ue4-senseglove-demo-scene`

`$ cd ue4-senseglove-demo-scene`

`$ git submodule update --init --recursive`

## Updating the submodule plugin
After getting the sources, you'll have the latest plugin by default.
In case the plugin gets updated after that, you can run:

`$ git submodule update --remote`

This will be enough if you are just using the plugin submodule and not developing on it. More information on git's submodules can be found here: https://git-scm.com/book/en/v2/Git-Tools-Submodules

## Prerequisites 
- Unreal Engine V4.10 and upwards
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

`git checkout myNewDemo`

- Preferably, do not remote push your local branches. If you think your assets and scripts and worthwile, merge it into master and push. Make sure you don't include any unneccessary binaries. 

- Try to work with directories in the Content folder, i.e MyNewGameBlueprints/Someblueprint.uasset. This way maps, blueprints and assets for different examples stay organized.

- Don't change the config files for initial Maps etc. You can make Maps and Configurations. Just include it in a folder in the Content directory. The initial scene should be the demo

- If the master branch gets updated remotely, try to rebase. This should be relatively easy, as long as you keep your directories seperated.

Of course, you can also fork this repo, but make sure you set an upstream link to keep updated!

### Developing with the Unreal Editor / Blueprints
Open the Unreal Project file and it will automatically compile the project and plugin. 

### Developing with Visual Studio / C++
Right click on the Unreal project file and click on `Generate Visual Studio project files`. This will setup your local references correctly. Open the newly generate .sln file. You can debug and build as usual in Visual Studio. 

### Hot reloading with Editor and Visual Studio
Open the editor first and then click on File > Visual Studio. 


