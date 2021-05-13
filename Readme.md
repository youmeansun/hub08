# Chinese HUB08 74HC595 Led Matrix (64x16) lib for ESP8266 Micropython

## About

I have many HUB08(red) LED Matrix in my small dark room. With a RMB8 led conntroller from Taobao, it's easy to texting on it from phones, but it can't work as a stopwatch what I want to use on my physics pendulum lesssons. 328P boards sell in an unacceptable price in 2021, above RMB20, but ESP8266 always under RMB10. So, Search libraries on Git, None at all. So, I have to write a one myself.

## Wiring

```null
Hardware spi uses MOSI=GPIO13, MISO=GPIO12, SCK=GPIO14, so CLK and R1 are unchangeable.
_________________________________
CLK...... GPIO-14 
R1........GPIO-12
_________________________________
A.........GPIO-16
B.........GPIO-15
C.........GPIO-02
D.........GPIO-00
LAT.......GPIO-05
OE........GPIO-04
You can modify the pins in lower part in __init__ func.

```

## Using

```null
>>> from hub08 import HUB08SPI
>>> matrix=HUB08SPI()
>>> matrix.loop()
>>> matrix.test_chinese()
>>> matrix.test_sinwave()
>>> matrix.test_fill()
>>> matrix.clear()
>>> matrix.drawRect(4,4,56,8,1)
```

