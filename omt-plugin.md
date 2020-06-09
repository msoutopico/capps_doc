# Graphical user interface
The plugin adds three items under the *Project* menu, which allow for three actions:

* **Import OMT package**: Unpack an OMT file and deploy the project it contains
* **Export OMT package**: Pack the current project as an OMT file
* **Export OMT and delete project**: Pack and delete the current project

## Packing a project

When packing the project, by default OmegaT will propose the parent folder (the one that contains the project folder) as the location where the OMT package will be saved, but the user can change this location before packing. Another convenient location might be inside the project itself. 

Every time a user packs a project, a few entries will be written to the `omt-packer.log`, thus keeping track of all the packing actions (which can be useful for the purposes of technical support), including information about the time, the user ID and the files.

## Packing and deleting a project

If the user wants to keep a packed version of the project but wants to get rid of the project itself, this item combines the two actions in one.

## Unpacking the project

When unpacking a project (when importing an OMT package), OmegaT will uncompress the contents of the OMT package, creating a project folder and opening that project in OmegaT. 

If the plugin detects another project in the folder where it tries to unpack (e.g. because the package is being imported from inside the project folder), then it assumes it is the same project and will overwrite it. 

If a `project_save.tmx` file is found in the existing project being overwritten and the package also contains a `project_save.tmx` file, then it asks the user whether that file should be overwritten or not. If the user chooses to overwrite it, a timestamped backup is created. All other files are overwritten in either case. 
