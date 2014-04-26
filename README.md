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





Moin Rufin,

so ich habe wie versprochen jetzt den OpenSource Launch vorbereitet. Dazu habe ich auf GitHub ( DAS Opensource Portal :) )
die Organisation: CallistoVFX angelegt und das entsprechende Projekt:
https://github.com/CallistoVFX/RoyalRender_Blender_Submitter. Das ganze läuft unter der GPL 2 http://de.wikipedia.org/wiki/GNU_General_Public_License
Bevor ich jetzt wirklich infos reinlade Anbei die entsprechenden Dateien:
Wäre schön wenn du die infos ( grade zu royal Render ) ergänzt, und mein english überarbeitest, und schaust ob das alles so okay ist im Namen von Callisto.
Schick mir die überarbeiteten Dateien dann zurück dann mache ich den initialen Push.
Die Readme ist die Info die auf der Startseite angezeigt wird ( wo grade nur der Projektname steht ), ist mit Markdown formatiert:
http://de.wikipedia.org/wiki/Markdown
In der Issues_tmp habe ich die Infos für die Tickets geschrieben, die nacher im Issuer System des Projektes landen werden.
Meine Idee ist dann im RoyalRender + Blender Forum das Projekt zu beschreiben. Dazu würde ich den "About this Project"


2014-04-25 23:12 GMT+02:00 Rufin Wiesemann <r.wiesemann@callistovfx.com>:

Hi Friedrich,
hab noch ein Bisschen experimentiert. Bin jetzt bei folgendem Stand der Dinge:

2.7 an 2.7 Submit führt zu render_crash.txt. Gerendert wird gar nicht.

2.7 an 2.64 Submit wird gerendert bis auf letzten Frame der zugeteilten Sequenz und hängt dann. Heißt jeder Renderclient arbeitet pro Job nur einmal und hängt sich dann weg. Anschließend kommt die Fehlermeldung mit Error, region type missing. Ist übrigens Blender spezifisch bei Nutzung falscher blend file in falscher Blender Version. Sprich blend file mit neuerer Blender Version erstellt wirft diesen Fehler aus und hängt beim Rendering. Rückmeldung über RR-Control was den Bearbeitungsstand angeht funzt nicht.

2.64 an 2.64 mit 2.7 blend file puttet den gleichen Fehler aus und rendert auch bis auf den letzten Frame der zugeteilten Sequenz, selbst wenn der Blend file noch mal vorher in 2.6 gespeichert wird. Auch keine Rückmeldung über rr_control.

2.64 an 2.64 mit blend file der in 2.64 erstellt wurde. Gibt Rückmeldung über rrControl. Rendert alles speichert auch ins Netz, kann auch über rrViewer angeschaut werden, aber hängt sich ebenfalls beim speichern des letzten Frames der zugeteilten Sequenz weg.

Anbei ein zip mit allen relevanten Dateien und Anpassungen von mir. Gibt auch noch nen SDK von RR zum Submit_Plugin. Übrigens scheint es für alle wesentlichen 3D und 2D Programme auch noch mal ein plugin in form einer *.dll für den submitter_Sceneparser zu geben. Ich hab jetzt wie für execute erstmal einen *.cfg angelegt. Wesentlich was gebracht hat jedoch das rausschmeissen von aus dem normalen blender.cfg file. Danach wurden wenigstens (bis auf den letzten) alle zugeteilten frames gerendert. Denn Blender zu sagen dass es zwischen den zu rendernden Frames genau eine so große Lücke zu lassen, wie insgesamt frames von rr zugeteilt wurde, führte dazu dass er meist nur den ersten frame rendern konnte. Warum er jetzt beim abspeichern des letzten Frames generell abkackt, weiß ich immer noch nicht. Und warum 2.7 gar nicht will, auch nicht.

Gruß,
Rufin



Rufin Wiesemann








Callisto FX GmbH
Bundesallee 87/88 (Haus 7, Aufgang 5)
12161 Berlin   •  Germany
Web: www.callistovfx.com
Mail: Info@callistovfx..com
Fon: +49 (0)30 – 2062 4774
Fax: +49 (0)30 – 2064 1527
Mobil: +49 (0)179 - 2909 355
Eingetragen beim AG Berlin-Charlottenburg unter HRB 141053 B
Geschäftsführer: Rufin Wiesemann
UST-ID/VAT-ID: DE282423139






Diese E-Mail und Ihre Anhänge enthält vertrauliche und/ oder rechtlich geschützte Informationen. Wenn Sie nicht der richtige Adressat sind oder diese E-Mail irrtümlich erhalten haben, informieren Sie bitte sofort den Absender
und vernichten Sie diese E-Mail. Das unerlaubte Kopieren sowie die unbefugte Weitergabe dieser E-Mail und/oder ihrer Anhänge ist nicht gestattet.

This e-mail and it’s attachments may contain confidential and/or privileged information. If you are not the intended recipient (or have received this e-mail in error) please notify the sender immediately and delete this e-mail. Any
unauthorized copying, disclosure or distribution of the material in this e-mail and/or it’s attachments is strictly forbidden.







Diese E-Mail ist frei von Viren und Malware, denn der avast! Antivirus Schutz ist aktiv.



