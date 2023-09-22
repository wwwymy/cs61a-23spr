wymy@Wairy lab08 % python3 ok -q wwpd-truck -u --local
=====================================================================
Assignment: Lab 8
OK, version v1.18.1
=====================================================================

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Unlocking tests

At each "? ", type what you would expect the output to be.
Type exit() to quit

---------------------------------------------------------------------
Car > Suite 1 > Case 1
(cases remaining: 1)

What would Python display? If you get stuck, try it out in the Python
interpreter!

>>> from car import *
>>> deneros_car = Car('Tesla', 'Model S')
>>> deneros_truck = MonsterTruck('Monster', 'Batmobile')
>>> deneros_car.size # Type Error if an error occurs and Nothing if nothing is displayed
? 'Tiny'
-- OK! --

>>> deneros_car.drive() # Type Error if an error occurs and Nothing if nothing is displayed
? 'Tesla Model S goes vroom!'
-- OK! --

>>> deneros_truck.size # Type Error if an error occurs and Nothing if nothing is displayed
? 'Monster'
-- OK! --

>>> deneros_truck.drive() # Type Error if an error occurs and Nothing if nothing is displayed
(line 1)? 'Vroom! This Monster Truck is huge!'
-- Not quite. Try again! --

(line 1)? 'Vroom! This Monster Truck is huge!'
-- Not quite. Try again! --

(line 1)? 
-- Not quite. Try again! --

(line 1)? Vroom! This Monster Truck is huge!
(line 2)? Monster Batmobile goes vroom!
-- Not quite. Try again! --

(line 1)? Vroom! This Monster Truck is huge!
(line 2)? 'Monster Batmobile goes vroom!'
-- OK! --

>>> MonsterTruck.drive(deneros_truck) # Type Error if an error occurs and Nothing if nothing is displayed
(line 1)? Vroom! This Monster Truck is huge!
(line 2)? 'Monster Batmobile goes vroom!'
-- OK! --

>>> Car.drive(deneros_truck) # Type Error if an error occurs and Nothing if nothing is displayed
? Vroom! This Monster Truck is huge!
-- Not quite. Try again! --

? 'Monster Batmobile goes vroom!'
-- OK! --

>>> deneros_truck.gas # Type Error if an error occurs and Nothing if nothing is displayed
? 0
-- OK! --

>>> MonsterTruck.rev(deneros_truck) # Type Error if an error occurs and Nothing if nothing is displayed
? Vroom! This Monster Truck is huge!
-- OK! --

>>> MonsterTruck.rev(deneros_car) # Type Error if an error occurs and Nothing if nothing is displayed
? Error
-- Not quite. Try again! --

? Vroom! This Monster Truck is huge!
-- OK! --

>>> Car.rev(deneros_truck) # Type Error if an error occurs and Nothing if nothing is displayed
? Error
-- OK! --

---------------------------------------------------------------------
OK! All cases for Car unlocked.

Cannot backup when running ok with --local.
wymy@Wairy lab08 % 

wymy@Wairy lab08 % python3 ok -q inheritance-abc -u --local
=====================================================================
Assignment: Lab 8
OK, version v1.18.1
=====================================================================

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Unlocking tests

At each "? ", type what you would expect the output to be.
Type exit() to quit

---------------------------------------------------------------------
Inheritance ABCs > Suite 1 > Case 1
(cases remaining: 1)

What would Python display? If you get stuck, try it out in the Python
interpreter!

>>> class A:
...   x, y = 0, 0
...   def __init__(self):
...         return
>>> class B(A):
...   def __init__(self):
...         return
>>> class C(A):
...   def __init__(self):
...         return
>>> print(A.x, B.x, C.x)
? 000
-- Not quite. Try again! --

? 0,0,0
-- Not quite. Try again! --

? 0 0 0
-- OK! --

>>> B.x = 2
>>> print(A.x, B.x, C.x)
? 0 2 0
-- OK! --

>>> A.x += 1
>>> print(A.x, B.x, C.x)
? 1 2 1
-- OK! --

>>> obj = C()
>>> obj.y = 1
>>> C.y == obj.y
? False
-- OK! --

>>> A.y = obj.y
>>> print(A.y, B.y, C.y, obj.y)
? 1 1 1 1
-- OK! --

---------------------------------------------------------------------
OK! All cases for Inheritance ABCs unlocked.