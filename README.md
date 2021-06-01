# Handheld-Raspberry-Pi-Zero

So, I have made this project for a long time, and I'd like to share all the circuits and configuration files for helping someone who want to make something similar.It is not pretty,( Becouse I don't have access to a 3d printer) but the circuitry works just fine and I am enjoying a lot the games.

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/main.jpeg)

The circuitry is pretty straightfoward, it's basicly two 18650 batterys connected in paralel, which are protected by a tp4560 charge/protection circuit. Then the 4.2v of the battery are stepped up to 5v with a MT3608 module that power all the 5v eletronics.
The d-pad and buttons have one terminal connected to the ground and the other to one of the Raspberry's GPIO. That, with the adafruit retrogame script, are regconized as a keyboard presses.
I use for the audio, a low pass filter that smooth-out the raspberry's PWM audio (It's necessary to change the config.txt file for getting the audio on the GPIO 19),so the audio signal goes to the headphone jack and a PAM8403, that amplifies the audio for the speaker.
I've modified a rear view car parking mirror, for work with 5 volts, and connect it's RCA video to the respective TV pins of the raspberry.

Here is the full schemathic

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/Schematic_Rasp_portable_2021-04-30-1.jpg)


PS: I speak portuguese, so, sorry for my english.
