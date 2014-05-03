RoyalRender Blender Submitter
=============================

Submission Script for Blender to Royal Render Rendermanager

### About this Project
Blender is getting more and more stakes in professional environments. The target of this Project is to connect Blender with
a standard rendermanager in a professional environment. Since RoyalRender is a solid choice and does not only offer support for quite 
a lot of software solutions out of the box, but also offers the possibility to configure custom solutions, we chose RoyalRender for a 
first thorough testing of the commandline rendering capabilities of Blender.     
 

### Version

This an early Alpha Version with a lot of Problems.

In the current Version you can submit scenes to Blender to Royal Render. Rendering is started, but not properly finished. Our Documentations has some Placeholders in it.
See issue list for more Information.
Any Help is highly appriciated.


### How it works

The Blender Python script blender_rr_submitter.py read the current Blender Scene Rendersetting like : StartFrame, EndFrame
output Path and so on and create a RoyalRender conform formated XML file. Then the rr_submitter.sh from RoyalRender is started with
this XML as first set of paramters. The RoyalRender Submitter gets all needed information from this XML.

RoyalRender needs two configuration files: one in the Installation Path 3D19__Blender.cfg which defines the command that
is started for Blender. In the current config Blender render is started via Commandline.  File is placed in
FILL_PATH_HERE

Second one is Blender.cfg wich contains the Path to the Blender application.
 File is Placed in RR_ROOT/install_paths/Blender.cfg

find more at the RoyalRender help page: http://www.royalrender.de/help/


### Installation

You need the RR_ROOT environment variable set on the submitter machine. Which usually already happend automatically on RoyalRender's Worksstation
client install.
Then put the blender_rr_submitter.py in your Blender/scripts/startup folder. which is usually at "../blender foundation/Blender/2.*/scripts/startup"
Copy the 3D19_Blender.cfg file to the RoyalRender Root share into the folder "render_apps/_config/"
After installing blender on the render clients, you add the new renderer through the config dialogue of the clientwatch's configure/render applications
dialogue. The automatic search and add function will only work if you also add a blender.cfg file unter "render_apps/_install_paths" stating the path
local path to the blender install. But adding manually works just fine.


### Callisto FX

Callisto FX is mainly a Visual Effects Studio for Television, Film and Commercial work in Berlin Germany.  
We have a small render farm and and a motivated potent team of alrounders. Delivering high quality vfx as well as industrial or architectual visualization
or low poly modelling and game character animation. 
Feel free to investigate under www.callistovfx.com

### Contribution
Everybody can contribute. Just follow the git-hub guidelines, and fork the poject, and open a pull-request against
the master. We are using git-flow for branch convention. So open the pull-Request against the develop branch pls.
Documentation changes against the documentation branch.

 If you want to file a bug - use the Git-Hub Issue system.

### Special Thanks

The idea of the Submitter is based on the work of:

Patrik Gleich and Felix Bucella
http://portal.hs-weingarten.de/c/document_library/get_file?uuid=471d8fbf-0fe7-43f6-8fb5-087933209bc3&groupId=26000



