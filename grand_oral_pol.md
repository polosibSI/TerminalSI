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

```python
ef set_servo_angle(pin, angle):
    duty = 26 + (angle * 102) / 180
    pin.write_analog(duty)

angle = 90
set_servo_angle(pin2, angle)

while True:
    if button_a.was_pressed() and angle >= 10:
        angle -= 10
        set_servo_angle(pin2, angle)
    if button_b.was_pressed() and angle <= 170:
        angle += 10
        set_servo_angle(pin2, angle)
```