# Dialogue-Sample-Player

What is DialogueSamplePlayer:
-----------------------------

This is a player desinged to play samples for a dialogue of three persons.
Therfore the buttons are ordered in an table with three columns. Each of the 
columns represents one person. For each person the player chooses one output 
channel.

The Dialogue Sample Player markes the played samples with bluish green color.
To reset the color of all buttons press 'Reset' or if you just want to reset one
button hold the right mouse key and left click the button you want.

Further the player sends OSC commands when a player starts playing and when the 
user clicked the stop, ring, hangup or reset button.

Prerequisites:
------------
1. Install Python (version 3.6 or later): https://www.python.org/downloads/
2. Run setup.bat (installs sounddevice, soundfile, PyQT5, python-osc)

Quick start (for Windows):
------------
1. Start 'DialogueRun.bat'
2. Choose an ASIO soundcard
3. Choose output channels (Player1-3)
- OSC if needed:
4. Set 'Network address' 
	- ('Test IP' button sends a ping and shows if IP address is OK)
5. Set 'OSC port'
- If all is okay:
6. Click 'OK'
- The main window shows up:
7. Click the buttons with the messages you want and build a dialogue
8. Click 'Quit' to close the DialogueSamplePlayer.

Usage without ASIO soundcard:
------------
* Download and install ASIO4ALL http://www.asio4all.org/ and restart PC.
* Set the channels to either 2 or 1. Don't mix.

Local usage without OSC
------------
Enter 127.0.0.1 as network address.


Special buttons:
----------------

'Stop'		- Stops the current playback and sends OSC message 'Stop'

'Ring'		- Send an OSC message to trigger en external ringing sound

'Hangup'	- Stops the current playback and sends OSC message 'Hangup'

'Reset'		- Reset the color of all buttons and sends OSC message 'Reset'

If you want to reset only one button hold the right mouse key and left click 
the button you want.


OSC commands out: 
-----------------

    Player start: 
        Adress: 'A','B','C'
        Data:   <length of sample in milliseconds>
    Stop clicked:
        Adress: 'Stop'
        Data:   0
    Ring clicked:
        Adress: 'Ring'
        Data:   0
    Hangup clicked:
        Adress: 'Hangup'
        Data:   0
    Reset clicked:
        Adress: 'Reset'
        Data:   0


TODO:
----- 
	- Playing parallel



