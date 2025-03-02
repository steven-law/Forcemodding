# Forcemodding
a collection of instructions to mod the akai force (probably also mpc range)
a modded AKAI product is needed

install vs code on a pc, you want to write code
install c/c++ extension
install remote ssh


install raspberry OS on a raspberry 3/4 IMPORTANT!! USE RASPBERRY OS from 28.1.2022 because of GLIB 2.32 !!!

connect from your PC to the pi in vscode via Remote SSH  
some things will get installed on the pi  
install alsa with sudo apt install libasound2-dev (via PUTTY, Terminal, or WinSCP)  
install binwalk for extracting img files
get kikgen´s imager file for comprtessing
to enable execution from sd card make:   
mount remount /media/662522 -o rw,remount,exec   
   
   
create a folder on the pi with mkdir YourSequencerName  
copy the rt*.h /.cpp files from one of an existing sequencer projects into your new folder  
copy the compile.sh file into your folder  
edit the compile file to your sequencerName   
copy the main.cpp file into your folder  

create code in main.cpp  
for midi cc´s the MPC MIDI CC Layout is as follows:  
Page 1:  
13 14 15 16  
 9 10 11 12  
 5  6  7  8  
 1  2  3  4  
  
compile with running the compile file with sh compile.sh  
  
connect to your force via WinSCP  
create a new folder in /media/662522/AddOns/YourProject  
copy the new created project file to this folder  
take the file from a different sequencer on the force and copy those to your folder  
  
change the files to your sequncer project, save.  
Your apps are now available over amit´s nodeserver (internet browser: <yourforceIP>  
and can be started and stopped easily over there.  
  

