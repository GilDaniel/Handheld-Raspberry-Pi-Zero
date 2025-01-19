# Handheld-Raspberry-Pi-Zero

I've made this project for a long, long time, so I am sharing all the circuitry and configuration files for anyone who want to make something similar. It don't have a pretty case (Because I don't have access to a 3d printer) but the circuitry and the overall project works just fine and I am enjoying a lot the games.

Youtube video: https://www.youtube.com/watch?v=VMPekJrzFAk&t=5s

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/main.jpeg)

The circuitry consists basicly on two 18650 2000mah batteries connected in paralel, which are managed by a tp4560 charge/protection circuit. The battery's 4.2v are stepped to 5v with a MT3608 module, wich powers all the 5v eletronics.
The D-pad and push-buttons have one terminal connected to the ground and the other to the Raspberry's GPIO. With that, the adafruit retrogame script regconizes the push-button presses as keyboard presses.
For the audio, I've used a low pass filter that smooths-out the Raspberry's PWM audio (It's necessary to change the config.txt file for getting this PWM audio on the GPIO 19). Then, the audio signal goes to the headphone jack or to the PAM8403 audio amplifier, depending on the audio selection switch.
The LCD screen that comes in a cheap car parking mirror was taken apart and modified to work with 5 volts, by bypassing it's internal 12v to 5v linear voltage regulator. After that, I connected it's RCA video input to the respective TV pins of the Raspberry-PI.

Here is the full schemathic

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/Schematic_Rasp_portable_2021-04-30-1.jpg)

OBS: A overclock is made on the config.txt file, for disabling it, erase the commands below #overclock
