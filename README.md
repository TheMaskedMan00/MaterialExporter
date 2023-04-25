# MaterialExporter

A plugin for Koikatsu and Koikatsu Sunshine to export materials at runtime.

I doubt anyone would find this useful exept me and a handful of other people who export characters from the game.

In the releases there should be a 'ShaderProperties.xml', Please create a new folder called 'MaterialExporter' in your 'UserData' folder and place the file inside.

The exported materials are checked via hash to check for duplicates, since there are a lot of duplicate materials in game and we dont need them.

Once the files are exported you can import them into your unity project and switch their shader to the correct one (can't do it automaticlly since A. it will mess up the hash check and B. You have to decompile the shaders yourself if you plan to use them so the GUID will be different)

Everything that the exporter can export is listed below:
Texture Offsets and Scale
Floats
Vectors/Colors
My own selection of Global Variables.

Note that custom shaders wont work since we cannot get a list of a shader's properties at runtime, If you run into a shader that cannot export please create an issue and upload the card/mod/shader and I will try to add compatibility for it.

# Usage
In the releases there should be a 'ShaderProperties.xml', Please create a new folder called 'MaterialExporter' in your 'UserData' folder and place the file inside.

In the character editor, simply press Left Shift and M.
The materials will be exported to 'UserData/MaterialExporter/Materials/(CharacterName)/'

You can configure the hotkey and export directory in the plugin settings.
