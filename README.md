# temperature-and-humidity.-DHT11


temperature and humidity. DHT11

sudo apt-get update
sudo apt-get install build-essential python-dev


git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT


sudo python setup.py install
sudo python3 setup.py install



cd examples


python AdafruitDHT.py 11 17







or another way

import Adafruit_DHT

sensor = Adafruit_DHT.DHT11
gpio = 17

# get a sensor reading (waiting 2 seconds between each retry).
humidity, temperature = Adafruit_DHT.read_retry(sensor, gpio)


if humidity is not None and temperature is not None:
    print('Temp={0:0.1f}*C  Humidity={1:0.1f}%'.format(temperature, humidity))
else:
    print('Failed to get reading. Try again!')









or another 




import sys
import Adafruit_DHT
import time

while True:

    humidity, temperature = Adafruit_DHT.read_retry(11, 4)

    print 'Temp: {0:0.1f} C  Humidity: {1:0.1f} %'.format(temperature, humidity)
    time.sleep(1)
