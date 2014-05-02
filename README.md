Blender Submitter for Royal Render 

RoyalRender Blender Submitter
=============================

Submission Script for Blender to Royal Render Rendermanager

### About this Project
Blender is getting more and more stakes in professional environments. The target of this Project is to connect Blender with
 the standard Rendermanager in a professional environment.
 ADD SOME MORE HERE

### Version

This an early Alpha Version with a lot of Problems.

In the current Version you can submit scenes to Blender to Royal Render. Rendering is started, but not properly finished.
See issue list for more Information.
Any Help is highly appriciated.

### How it works

The Blender Python script blender_rr_submitter.py read the current Blender Scene Rendersetting like : StartFrame, EndFrame
output Path and so on and create an Royal Render formated XML. Then the rr_submitter.sh from Royal Render is started with
this XML as first Paramter. The RoyalRender Submitter get all needed information from this XML.

Royal Render need two configuration files: one in the Installation Path 3D19__Blender.cfg which defines the command that
is started for Blender. In the current config Blender render is started via Commandline.  File is placed in
FILL_PATH_HERE

Second one is Blender.cfg wich contains the Path to the Blender application.
 File is Placed in FILL_PATH_HERE

ADD DOKU LINKS TO ROYAL RENDER

### Installation

You need the RR_ROOT environment Variabel setuped on the Submitter Mashine.
The put the blender_rr_submitter.py in your Blender/scripts/startup folder.

### CallistoVFX

CallistoVFX is an ADD INFORMATION HERE

### Contribution
Everybody can contribute. Just follow the git-hub guidelines, and fork the Project, and open a pull-request against
the master. We are using git-flow for branch convention. So open the pull-Request against the develop branch pls.
Documentation changes against the documentation branch.

 If you want to file a bug - use the Git-Hub Issue system.

### Special Thanks

The idea of the Submitter is based on the work of:

Patrik Gleich and Felix Bucella
http://portal.hs-weingarten.de/c/document_library/get_file?uuid=471d8fbf-0fe7-43f6-8fb5-087933209bc3&groupId=26000





