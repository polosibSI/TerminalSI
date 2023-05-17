Pince robot
![pince3](/pince3.jpg)
![main_robot](/main_robot.jpg)
![pince2](/pince2.jpg)

code clignotement :
```python
while True:
    pin0.write_digital(0)
    sleep(1000)
    pin0.write_digital(1)
    sleep(1000)
```
```python
while True:
    niveau = pin1.read_analog()
    pin0.write_analog(niveau)
    sleep(20)
```