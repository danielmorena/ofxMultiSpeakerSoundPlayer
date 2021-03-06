ofxMultiSpeakerSoundPlayer
==========================

An implementation of ofSoundPlayer using FMod to handle each single speaker connected to a surround sound card.  
For example, with this addon, is possible to send one sound file to the frontal speakers, another sound file to the side speakers etc.  
It provides the following method:

    void playTo(int speaker);

where `speaker` is a value between 0 and 3, with the following meaning:

* **0** send to rear speakers (R+L)
* **1** send to side speakers (R+L)
* **2** send to frontal speakers (R+L)
* **3** send to central speaker

It is designed for a 7.1 surround setup, but can be changed editing the value of `speakerMode` variable from `FMOD_SPEAKERMODE_7POINT1` to one of the `FMOD_SPEAKERMODE` values.  
Another value to configure, is the device index (`deviceNumber`) referring to the used sound card, that can be found with the `FMOD_System_GetDriverInfo` method.

Tested with openFrameworks 0.8.1 on Linux Debian 64bit.
