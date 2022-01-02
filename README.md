# Handheld-Raspberry-Pi-Zero

I've made this project for a long, long time, and I'd like to share all the circuitry and config files for anyone who want to make something similar. It don't have an pretty case,(Becouse I don't have access to a 3d printer) but the circuitry works just fine and I am enjoying a lot the games.

Youtube video: https://www.youtube.com/watch?v=VMPekJrzFAk&t=5s

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/main.jpeg)

The circuitry is pretty straightfoward, it's basicly two 18650 2000mah batteries connected in paralel, which are protected by a tp4560 charge/protection circuit. The battery's 4.2v are stepped up to 5v with a MT3608 module, that power all the 5v eletronics.
The D-pad and push-buttons have one terminal connected to the ground and the other one to the Raspberry's GPIO. whith that, the adafruit retrogame script regconizes the push-button presses as keyboard presses.
I've used for the audio, an low pass filter that smooths-out the Raspberry's PWM audio (It's necessary to change the config.txt file for getting this PWM audio on the GPIO 19),so the audio signal goes to the headphone jack and the PAM8403 audio amplifier.
I've modified a rear view car parking mirror, to work with 5 volts, and then I connected it's RCA video to the respective TV pins of the Raspberry-PI.

Here is the full schemathic

![alt text](https://github.com/GilDaniel/Handheld-Raspberry-Pi-Zero/blob/main/Schematic_Rasp_portable_2021-04-30-1.jpg)

OBS: A overclock is made on the config.txt file, for disabling it, erase the commands below #overclock
