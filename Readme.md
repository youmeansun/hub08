## Wiring

```
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
You can modify the pins above in __init__ func.

```

## Using

```
>>> from hub08 import HUB08SPI
>>> matrix=HUB08SPI()
>>> matrix.loop()
>>> matrix.test_chinese()
>>> matrix.test_sinwave()
>>> matrix.test_fill()
>>> matrix.clear()
>>> matrix.drawRect(4,4,56,8,1)
```

