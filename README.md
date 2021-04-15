# TouchDesigner-SP-Template
A free download of my single drum template for MIDI mapping in TouchDesigner using a Sensory Percussion sensor, 
including a Sensory set file with a single drum MIDI starter template and a blank kit building template. 

Visit the assets folder and download direct from GitHub! Must have TouchDesigner already installed in order to open 
and use template. Visit deritivative.ca for a free download.

MIDI Mapping directions:

1. In TouchDesigner, open <b>Dialogs > MIDI Device Mapper</b>

2. In Sensory Percussion, open preferences and make sure <b>Active MIDI Outputs > IAC Driver Bus 1</b> is selected.

3. In TouchDesigner's <b>Device Mapper</b>, select <b>Create New Mapping</b>. 

4. Under <b>In Device</b> in the device mappings console, select <b>IAC Driver Bus 1.</b>

5. Select the <b>Device</b> console (next to the device mappings console) and click the <b>Add Device</b> button.

6. Select the newly created <b>User Device Map</b> and rename it. I use "SPMesh".

7. Test your drum to make sure the MIDI information is being read by TouchDesigner.

8. Locate your <b>Note On</b> messages. TouchDesigner uses hexidecimal code for MIDI messages.  Visit http://www.midibox.org/dokuwiki/doku.php?id=midi_specification 
for a more detailed description of hexidecimal MIDI messages. 

9. Note the message associated with the <b>Note On</b> event. If you are using channel 1 in Sensory, it will start with <b>90</b>. The second value will be your 
MIDI note number. In the SP Template, I use note <b>C 1/number 24</b>.

10. Replace the values in slider <b>s1</b> with "<b>90 24 --</b>". This indicates "note on, channel 1, (90) C1 (24)". "<b>--</b>" are where your input values will 
be stored.

11. As per the SP Template, replace the values in slider <b>s2</b> with "<b>90 25 --</b>" and <b>s3</b> with "<b>90 26 --</b>".

12. If you use a sensor on channel 2, your hex code MIDI note on messages will be start with "<b>91</b>". Channel 3, "<b>92</b>". Channel 4, "<b>93</b>". 

13. If you use different MIDI notes from Sensory, check their corresponding note numbers. For reference, C4 is 60.

14. Return to the <b>Device Mapper</b> console. Under <b>MIDI Map</b> select <b>SPMesh</b>. 
<body>
<pre>
 ___  ___  ________  ___      ___ _______           ________ ___  ___  ________      
|\  \|\  \|\   __  \|\  \    /  /|\  ___ \         |\  _____\\  \|\  \|\   ___  \    
\ \  \\\  \ \  \|\  \ \  \  /  / | \   __/|        \ \  \__/\ \  \\\  \ \  \\ \  \   
 \ \   __  \ \   __  \ \  \/  / / \ \  \_|/__       \ \   __\\ \  \\\  \ \  \\ \  \  
  \ \  \ \  \ \  \ \  \ \    / /   \ \  \_|\ \       \ \  \_| \ \  \\\  \ \  \\ \  \ 
   \ \__\ \__\ \__\ \__\ \__/ /     \ \_______\       \ \__\   \ \_______\ \__\\ \__\
    \|__|\|__|\|__|\|__|\|__|/       \|_______|        \|__|    \|_______|\|__| \|__|
    </pre>
  </body>
