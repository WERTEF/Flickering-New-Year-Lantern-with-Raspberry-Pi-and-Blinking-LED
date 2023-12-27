# Flickering-New-Year-Lantern-with-Raspberry-Pi-and-Blinking-LED
Example code for creating a flickering New Year lantern with Raspberry Pi and a blinking LED.
import RPi.GPIO as GPIO
import time

led_pin = 17

GPIO.setmode(GPIO.BCM)
GPIO.setup(led_pin, GPIO.OUT)

try:
    while True:
        GPIO.output(led_pin, GPIO.HIGH)
        time.sleep(0.5)
        GPIO.output(led_pin, GPIO.LOW)
        time.sleep(0.5)
except KeyboardInterrupt:
    GPIO.cleanup()
