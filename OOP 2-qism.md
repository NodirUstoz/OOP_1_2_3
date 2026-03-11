# Python OOP darsligi — 2-qism

## Har bir mavzu bo‘yicha kuchli Python misollar, savollar va mashqlar

---

## Mundarija

1. [Kirish](#kirish)
2. [Class va Object bo‘yicha misollar](#class-va-object-boyicha-misollar)
3. [Attribute va Method bo‘yicha misollar](#attribute-va-method-boyicha-misollar)
4. [`self` va `__init__` bo‘yicha misollar](#self-va-__init__-boyicha-misollar)
5. [Instance va Class Attribute bo‘yicha misollar](#instance-va-class-attribute-boyicha-misollar)
6. [Instance method, classmethod, staticmethod](#instance-method-classmethod-staticmethod)
7. [Inkapsulyatsiya bo‘yicha misollar](#inkapsulyatsiya-boyicha-misollar)
8. [Abstraksiya bo‘yicha misollar](#abstraksiya-boyicha-misollar)
9. [Meros olish bo‘yicha misollar](#meros-olish-boyicha-misollar)
10. [Polimorfizm bo‘yicha misollar](#polimorfizm-boyicha-misollar)
11. [Overriding va `super()`](#overriding-va-super)
12. [Getter, Setter va `property`](#getter-setter-va-property)
13. [Magic methods bo‘yicha misollar](#magic-methods-boyicha-misollar)
14. [Composition bo‘yicha misollar](#composition-boyicha-misollar)
15. [Abstract class bo‘yicha misollar](#abstract-class-boyicha-misollar)
16. [Dataclass bo‘yicha misollar](#dataclass-boyicha-misollar)
17. [Eng muhim nazariy savollar](#eng-muhim-nazariy-savollar)
18. [Mustahkamlash uchun mashqlar](#mustahkamlash-uchun-mashqlar)
19. [Mini loyiha g‘oyalari](#mini-loyiha-goyalari)
20. [Xulosa](#xulosa)

---

# Kirish

Oldingi qismda biz OOP ning nazariyasini ko‘rdik. Endi esa shu bilimlarni amalda mustahkamlaymiz.

Bu qismda siz:

* har bir mavzu bo‘yicha kod ko‘rasiz
* kodning ichki mantiqini tushunasiz
* nazariy savollar orqali bilimni tekshirasiz
* mashqlar orqali mustaqil ishlaysiz

Bu qism juda muhim, chunki OOP faqat o‘qib emas, **yozib ko‘rib** o‘rganiladi.

---

# Class va Object bo‘yicha misollar

## Misol 1. Eng sodda klass

```python
class Student:
    pass


s1 = Student()
s2 = Student()

print(s1)
print(s2)
```

## Tushuntirish

Bu yerda:

* `Student` — class
* `s1`, `s2` — object

Hozircha klass ichida hech narsa yo‘q, lekin obyekt yaratish mumkin.

---

## Misol 2. Telefon klassi

```python
class Phone:
    pass


phone1 = Phone()
phone2 = Phone()
```

Bu yerda ham `Phone` — class, `phone1` va `phone2` — object.

---

## Muhim xulosa

Class — qolip.
Object — o‘sha qolipdan yaratilgan nusxa.

---

## Savollar

1. Class nima?
2. Object nima?
3. Bitta classdan nechta object yaratish mumkin?
4. `Student` bilan `s1 = Student()` orasidagi farq nima?

---

## Mashqlar

1. `Car` nomli bo‘sh class yarating.
2. Shu classdan 3 ta object yarating.
3. `Book` nomli bo‘sh class yarating.
4. `Teacher` nomli bo‘sh classdan 2 ta object yarating.

---

# Attribute va Method bo‘yicha misollar

## Misol 1. Talaba atributlari

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age


s1 = Student("Ali", 18)

print(s1.name)
print(s1.age)
```

## Tushuntirish

Bu yerda:

* `name`
* `age`

atributlar.

Ular obyekt haqida ma’lumot saqlaydi.

---

## Misol 2. Method qo‘shish

```python
class Student:
    def __init__(self, name):
        self.name = name

    def introduce(self):
        print(f"Mening ismim {self.name}")


s1 = Student("Ali")
s1.introduce()
```

## Tushuntirish

Bu yerda `introduce()` — method.
U klass ichida yozilgan funksiya.

---

## Misol 3. Mashina haqida ma’lumot

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def info(self):
        print(f"Brand: {self.brand}, Color: {self.color}")


car1 = Car("Chevrolet", "oq")
car1.info()
```

---

## Savollar

1. Atribut nima?
2. Method nima?
3. Atribut bilan method orasidagi farq nima?
4. `self.name` nima ma’noni bildiradi?

---

## Mashqlar

1. `Book` klassi yarating. Unda `title` va `author` atributlari bo‘lsin.
2. `info()` methodi yarating va kitob nomi bilan muallifni chiqarsin.
3. `Animal` klassi yarating. `name` atributi va `speak()` methodi bo‘lsin.
4. `Laptop` klassi yarating va `brand`, `ram` atributlarini qo‘shing.

---

# `self` va `__init__` bo‘yicha misollar

## Misol 1. `self` bilan ishlash

```python
class Student:
    def __init__(self, name):
        self.name = name

    def say_name(self):
        print(self.name)


s1 = Student("Ali")
s2 = Student("Vali")

s1.say_name()
s2.say_name()
```

## Tushuntirish

Bu yerda:

* `s1` uchun `self.name = "Ali"`
* `s2` uchun `self.name = "Vali"`

Har bir object o‘z qiymatiga ega.

---

## Misol 2. `__init__` avtomatik ishlashi

```python
class User:
    def __init__(self, username):
        print("Obyekt yaratildi")
        self.username = username


u1 = User("ali_01")
```

## Tushuntirish

`u1 = User("ali_01")` yozilganda `__init__` avtomatik chaqiriladi.

---

## Misol 3. Bir nechta atribut

```python
class Product:
    def __init__(self, name, price, quantity):
        self.name = name
        self.price = price
        self.quantity = quantity

    def info(self):
        print(self.name, self.price, self.quantity)


p1 = Product("Olma", 12000, 5)
p1.info()
```

---

## Savollar

1. `self` nima?
2. `__init__` qachon ishlaydi?
3. Nega `self` kerak?
4. `__init__` bo‘lmasa ham object yaratish mumkinmi?

---

## Mashqlar

1. `Teacher` klassi yarating. `name`, `subject` atributlari bo‘lsin.
2. `Patient` klassi yarating. `fullname`, `phone` atributlari bo‘lsin.
3. `Course` klassi yarating. `title`, `duration` atributlari bo‘lsin.
4. Har bir klassga bittadan method yozing.

---

# Instance va Class Attribute bo‘yicha misollar

## Misol 1. Instance attribute

```python
class Student:
    def __init__(self, name):
        self.name = name


s1 = Student("Ali")
s2 = Student("Vali")

print(s1.name)
print(s2.name)
```

Bu yerda `name` har bir object uchun alohida.

---

## Misol 2. Class attribute

```python
class Student:
    school = "Najot Ta'lim"

    def __init__(self, name):
        self.name = name


s1 = Student("Ali")
s2 = Student("Vali")

print(s1.school)
print(s2.school)
```

Bu yerda `school` ikkalasi uchun umumiy.

---

## Misol 3. Farqni ko‘rish

```python
class Student:
    school = "45-maktab"

    def __init__(self, name):
        self.name = name


s1 = Student("Ali")
s2 = Student("Vali")

s1.name = "Hasan"
Student.school = "12-maktab"

print(s1.name)
print(s2.name)
print(s1.school)
print(s2.school)
```

## Tushuntirish

* `name` faqat bitta objectga tegishli
* `school` esa classga tegishli

---

## Savollar

1. Instance attribute nima?
2. Class attribute nima?
3. Qachon class attribute ishlatamiz?
4. `self.name` bilan `Student.school` farqi nima?

---

## Mashqlar

1. `Car` klassida `wheels = 4` class attribute bo‘lsin.
2. `brand`, `color` instance attribute bo‘lsin.
3. `Teacher` klassida `school_name` class attribute bo‘lsin.
4. 2 ta object yaratib, farqini ko‘rsating.

---

# Instance method, classmethod, staticmethod

## Misol 1. Instance method

```python
class Student:
    def __init__(self, name):
        self.name = name

    def hello(self):
        print(f"Salom, men {self.name}")


s = Student("Ali")
s.hello()
```

---

## Misol 2. Class method

```python
class Student:
    school = "Najot"

    @classmethod
    def show_school(cls):
        print(cls.school)


Student.show_school()
```

---

## Misol 3. Static method

```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b


print(Math.add(5, 7))
```

---

## Misol 4. Alternative constructor

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    @classmethod
    def from_string(cls, text):
        name, age = text.split("-")
        return cls(name, int(age))


s = Student.from_string("Ali-18")
print(s.name)
print(s.age)
```

---

## Savollar

1. Instance method qaysi ma’lumot bilan ishlaydi?
2. Classmethod da `cls` nimani bildiradi?
3. Staticmethod qachon kerak bo‘ladi?
4. Alternative constructor nima?

---

## Mashqlar

1. `School` klassida class attribute yarating.
2. `show_school()` nomli classmethod yozing.
3. `is_even()` nomli staticmethod yozing.
4. `from_text()` nomli classmethod yozing.

---

# Inkapsulyatsiya bo‘yicha misollar

## Misol 1. Oddiy private atribut

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance

    def show_balance(self):
        return self.__balance


acc = BankAccount("Ali", 1000)
print(acc.show_balance())
```

---

## Misol 2. Nazorat bilan pul qo‘shish

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def show_balance(self):
        return self.__balance


acc = BankAccount("Ali", 1000)
acc.deposit(500)
print(acc.show_balance())
```

---

## Misol 3. Noto‘g‘ri qiymatdan himoya

```python
class Student:
    def __init__(self, name, grade):
        self.name = name
        self.__grade = grade

    def set_grade(self, grade):
        if 0 <= grade <= 100:
            self.__grade = grade

    def get_grade(self):
        return self.__grade
```

Bu yerda baho nazorat bilan o‘zgartiriladi.

---

## Savollar

1. Inkapsulyatsiya nima?
2. Nega private atribut ishlatiladi?
3. Inkapsulyatsiyaning foydasi nima?
4. `__balance` nima uchun kerak?

---

## Mashqlar

1. `Wallet` klassi yarating va `__money` private atribut qiling.
2. `add_money()` methodi yozing.
3. `spend_money()` methodi yozing.
4. `show_money()` methodi yozing.

---

# Abstraksiya bo‘yicha misollar

## Misol 1. Soddalashtirilgan interfeys

```python
class Car:
    def start(self):
        print("Mashina ishga tushdi")

    def stop(self):
        print("Mashina to‘xtadi")


car = Car()
car.start()
car.stop()
```

Bu yerda foydalanuvchi ichki murakkablikni ko‘rmaydi.

---

## Misol 2. Kompyuterni yoqish

```python
class Computer:
    def turn_on(self):
        print("Kompyuter yoqildi")

    def turn_off(self):
        print("Kompyuter o‘chdi")
```

Ichkaridagi barcha murakkab jarayon yashirilgan.

---

## Misol 3. Kofe mashinasi

```python
class CoffeeMachine:
    def make_coffee(self):
        print("Qahva tayyor bo‘ldi")


machine = CoffeeMachine()
machine.make_coffee()
```

Bu ham abstraksiya.

---

## Savollar

1. Abstraksiya nima?
2. Inkapsulyatsiya va abstraksiya farqi nima?
3. Nega abstraksiya kerak?
4. Qachon foydalanuvchiga faqat tashqi interfeys ko‘rsatamiz?

---

## Mashqlar

1. `TV` klassi yarating. `on()` va `off()` methodlari bo‘lsin.
2. `WashingMachine` klassi yarating. `start_wash()` methodi bo‘lsin.
3. `ATM` klassi yarating. `withdraw_cash()` methodi bo‘lsin.
4. Har birida abstraksiyani tushuntirib yozing.

---

# Meros olish bo‘yicha misollar

## Misol 1. Oddiy inheritance

```python
class Animal:
    def eat(self):
        print("Ovqat yeyapti")


class Dog(Animal):
    def bark(self):
        print("Vov-vov")


dog = Dog()
dog.eat()
dog.bark()
```

---

## Misol 2. User va Admin

```python
class User:
    def login(self):
        print("Tizimga kirdi")


class Admin(User):
    def delete_user(self):
        print("Foydalanuvchini o‘chirdi")


admin = Admin()
admin.login()
admin.delete_user()
```

---

## Misol 3. Employee va Doctor

```python
class Employee:
    def __init__(self, name):
        self.name = name

    def work(self):
        print(f"{self.name} ishlayapti")


class Doctor(Employee):
    def treat(self):
        print(f"{self.name} bemorni davolayapti")


d = Doctor("Hasan")
d.work()
d.treat()
```

---

## Savollar

1. Meros olish nima?
2. Ota klass va voris klass nima?
3. Meros olishning foydasi nima?
4. Qachon inheritance ishlatiladi?

---

## Mashqlar

1. `Person` klassi yarating.
2. `Student(Person)` klassi yarating.
3. `Teacher(Person)` klassi yarating.
4. `Person` da umumiy method yozing.
5. Voris klasslarda qo‘shimcha method yozing.

---

# Polimorfizm bo‘yicha misollar

## Misol 1. Bir xil method, turli natija

```python
class Dog:
    def sound(self):
        print("Vov-vov")


class Cat:
    def sound(self):
        print("Miyov")


class Cow:
    def sound(self):
        print("Mo‘-mo‘")


animals = [Dog(), Cat(), Cow()]
for animal in animals:
    animal.sound()
```

---

## Misol 2. Funksiya orqali ishlatish

```python
class Duck:
    def fly(self):
        print("O‘rdak uchdi")


class Plane:
    def fly(self):
        print("Samolyot uchdi")


def start_flying(obj):
    obj.fly()


start_flying(Duck())
start_flying(Plane())
```

---

## Misol 3. Payment misoli

```python
class CardPayment:
    def pay(self):
        print("Karta orqali to‘landi")


class CashPayment:
    def pay(self):
        print("Naqd pul bilan to‘landi")


def complete_payment(payment):
    payment.pay()


complete_payment(CardPayment())
complete_payment(CashPayment())
```

---

## Savollar

1. Polimorfizm nima?
2. Nega polimorfizm qulay?
3. Method nomi bir xil bo‘lsa ham, natija turlicha bo‘lishi mumkinmi?
4. `pay()` misolida polimorfizm qayerda?

---

## Mashqlar

1. `Bird`, `Plane`, `Rocket` klasslari yarating, `fly()` methodi bo‘lsin.
2. `Dog`, `Lion`, `Fox` klasslarida `sound()` methodi bo‘lsin.
3. `ClickPayment`, `PaymePayment`, `CashPayment` klasslari yarating.
4. Barchasini bitta funksiya orqali ishlating.

---

# Overriding va `super()`

## Misol 1. Overriding

```python
class Animal:
    def sound(self):
        print("Hayvon ovoz chiqardi")


class Dog(Animal):
    def sound(self):
        print("It vovulladi")


a = Animal()
d = Dog()

a.sound()
d.sound()
```

---

## Misol 2. `super()` bilan konstruktor

```python
class Person:
    def __init__(self, name):
        self.name = name


class Student(Person):
    def __init__(self, name, grade):
        super().__init__(name)
        self.grade = grade


s = Student("Ali", 5)
print(s.name)
print(s.grade)
```

---

## Misol 3. `super()` bilan method chaqirish

```python
class Person:
    def info(self):
        print("Bu odam haqida umumiy ma’lumot")


class Student(Person):
    def info(self):
        super().info()
        print("Bu esa talaba haqida qo‘shimcha ma’lumot")


s = Student()
s.info()
```

---

## Savollar

1. Overriding nima?
2. `super()` nima uchun kerak?
3. `super().__init__()` qachon ishlatiladi?
4. Voris klass ota klass methodini qayta yozishi mumkinmi?

---

## Mashqlar

1. `Animal` va `Cat` klasslari yozing, `sound()` ni overriding qiling.
2. `User` va `Admin` klasslari yozing, `info()` methodini overriding qiling.
3. `Person` va `Teacher` klasslari yozing, `super()` ishlating.
4. Ota klassning methodini chaqirib, so‘ng qo‘shimcha matn chiqaring.

---

# Getter, Setter va `property`

## Misol 1. Oddiy getter/setter

```python
class Student:
    def __init__(self, age):
        self.__age = age

    def get_age(self):
        return self.__age

    def set_age(self, age):
        if age > 0:
            self.__age = age


s = Student(18)
print(s.get_age())
s.set_age(20)
print(s.get_age())
```

---

## Misol 2. `property` bilan

```python
class Student:
    def __init__(self, age):
        self.__age = age

    @property
    def age(self):
        return self.__age

    @age.setter
    def age(self, value):
        if value > 0:
            self.__age = value


s = Student(18)
print(s.age)
s.age = 21
print(s.age)
```

---

## Misol 3. Narxni nazorat qilish

```python
class Product:
    def __init__(self, price):
        self.__price = price

    @property
    def price(self):
        return self.__price

    @price.setter
    def price(self, value):
        if value >= 0:
            self.__price = value
```

---

## Savollar

1. Getter nima?
2. Setter nima?
3. `property` nimaga kerak?
4. Qachon oddiy atribut o‘rniga `property` ishlatamiz?

---

## Mashqlar

1. `BankCard` klassi yarating. `balance` ni `property` bilan boshqaring.
2. `Product` klassi yarating. `price` manfiy bo‘lmasin.
3. `Student` klassi yarating. `grade` 0 dan 100 gacha bo‘lsin.
4. `Employee` klassida `salary` ni `property` bilan boshqaring.

---

# Magic methods bo‘yicha misollar

## Misol 1. `__str__`

```python
class Student:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return f"Student: {self.name}"


s = Student("Ali")
print(s)
```

---

## Misol 2. `__len__`

```python
class Box:
    def __init__(self, items):
        self.items = items

    def __len__(self):
        return len(self.items)


b = Box([1, 2, 3, 4])
print(len(b))
```

---

## Misol 3. `__add__`

```python
class Number:
    def __init__(self, value):
        self.value = value

    def __add__(self, other):
        return Number(self.value + other.value)

    def __str__(self):
        return str(self.value)


a = Number(10)
b = Number(20)
print(a + b)
```

---

## Savollar

1. Magic method nima?
2. `__str__` nimaga kerak?
3. `__len__` qachon ishlatiladi?
4. `__add__` bilan nimani boshqarish mumkin?

---

## Mashqlar

1. `Book` klassida `__str__` yozing.
2. `Basket` klassida `__len__` yozing.
3. `Money` klassida `__add__` yozing.
4. `Student` klassida `__repr__` yozib ko‘ring.

---

# Composition bo‘yicha misollar

## Misol 1. Car va Engine

```python
class Engine:
    def start(self):
        print("Motor ishga tushdi")


class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        self.engine.start()
        print("Mashina yurdi")


car = Car()
car.start()
```

---

## Misol 2. Computer va CPU

```python
class CPU:
    def process(self):
        print("Hisoblash bajarildi")


class Computer:
    def __init__(self):
        self.cpu = CPU()

    def work(self):
        self.cpu.process()
        print("Kompyuter ishladi")
```

---

## Misol 3. House va Room

```python
class Room:
    def __init__(self, name):
        self.name = name


class House:
    def __init__(self):
        self.room1 = Room("Yotoqxona")
        self.room2 = Room("Mehmonxona")
```

---

## Savollar

1. Composition nima?
2. Inheritance va composition farqi nima?
3. `Car has an Engine` qaysi bog‘lanish?
4. Nega composition ko‘p joyda foydali?

---

## Mashqlar

1. `Phone` va `Battery` klasslari yarating.
2. `School` va `Classroom` klasslari yarating.
3. `Shop` va `Product` klasslari yarating.
4. Har birida composition ishlating.

---

# Abstract class bo‘yicha misollar

## Misol 1. Oddiy abstract class

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def sound(self):
        pass
```

---

## Misol 2. Voris klasslar

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def sound(self):
        pass


class Dog(Animal):
    def sound(self):
        print("Vov-vov")


class Cat(Animal):
    def sound(self):
        print("Miyov")
```

---

## Misol 3. Payment tizimi

```python
from abc import ABC, abstractmethod

class Payment(ABC):
    @abstractmethod
    def pay(self):
        pass


class CardPayment(Payment):
    def pay(self):
        print("Karta orqali to‘landi")


class CashPayment(Payment):
    def pay(self):
        print("Naqd to‘lov qilindi")
```

---

## Savollar

1. Abstract class nima?
2. `@abstractmethod` nimani bildiradi?
3. Qachon abstract class ishlatiladi?
4. Nega barcha voris klasslarda bir xil method bo‘lishi foydali?

---

## Mashqlar

1. `Transport` abstract class yarating.
2. `Car`, `Bike`, `Bus` klasslari yozing.
3. `move()` methodini majburiy qiling.
4. `Notification` abstract class yarating va voris klasslar yozing.

---

# Dataclass bo‘yicha misollar

## Misol 1. Eng sodda dataclass

```python
from dataclasses import dataclass

@dataclass
class Student:
    name: str
    age: int


s = Student("Ali", 18)
print(s)
```

---

## Misol 2. Product dataclass

```python
from dataclasses import dataclass

@dataclass
class Product:
    name: str
    price: float
    quantity: int
```

---

## Misol 3. Baho modeli

```python
from dataclasses import dataclass

@dataclass
class Grade:
    subject: str
    score: int
```

---

## Savollar

1. Dataclass nima?
2. Qachon dataclass qulay?
3. Oddiy class bilan dataclass farqi nima?
4. Dataclass ko‘proq nimaga mos?

---

## Mashqlar

1. `Book` dataclass yarating.
2. `User` dataclass yarating.
3. `Clinic` dataclass yarating.
4. `Appointment` dataclass yarating.

---

# Eng muhim nazariy savollar

1. OOP nima?
2. Class va object orasidagi farq nima?
3. Atribut nima?
4. Method nima?
5. `self` nima uchun kerak?
6. `__init__` ning vazifasi nima?
7. Instance attribute nima?
8. Class attribute nima?
9. Instance method, classmethod, staticmethod farqi nima?
10. Inkapsulyatsiya nima?
11. Abstraksiya nima?
12. Inkapsulyatsiya bilan abstraksiya farqi nima?
13. Meros olish nima?
14. Ota klass va voris klass nima?
15. Polimorfizm nima?
16. Overriding nima?
17. `super()` nimaga kerak?
18. Getter va setter nima?
19. `property` nimaga kerak?
20. Magic method nima?
21. Composition nima?
22. Inheritance va composition farqi nima?
23. Abstract class nima?
24. Dataclass nima?
25. OOP qaysi loyihalarda ayniqsa foydali?

---

# Mustahkamlash uchun mashqlar

## 1-daraja

1. `Student` klassi yarating.
2. `name`, `age` atributlari bo‘lsin.
3. `introduce()` methodi bo‘lsin.
4. 3 ta object yarating.

## 2-daraja

1. `Car` klassi yarating.
2. `brand`, `color`, `year` atributlari bo‘lsin.
3. `info()` methodi bo‘lsin.
4. `drive()` methodi bo‘lsin.

## 3-daraja

1. `Person` klassi yarating.
2. `Student(Person)` va `Teacher(Person)` klasslari yarating.
3. Umumiy va qo‘shimcha methodlar yozing.

## 4-daraja

1. `BankAccount` klassi yarating.
2. `__balance` private atribut bo‘lsin.
3. `deposit()`, `withdraw()`, `show_balance()` methodlari bo‘lsin.

## 5-daraja

1. `Animal` abstract class yarating.
2. `Dog`, `Cat`, `Cow` voris klasslarini yarating.
3. `sound()` methodini majburiy qiling.

## 6-daraja

1. `Product` klassi yarating.
2. `Cart` klassi yarating.
3. `Cart` ichida mahsulotlar saqlansin.
4. `total_price()` methodi bo‘lsin.

## 7-daraja

1. `Payment` abstract class yarating.
2. `CardPayment`, `CashPayment`, `PaymePayment` klasslari yarating.
3. `pay()` methodini polimorfizm orqali ishlating.

---

# Mini loyiha g‘oyalari

## 1. Kutubxona tizimi

Klasslar:

* `Book`
* `Reader`
* `Library`

## 2. Maktab tizimi

Klasslar:

* `Student`
* `Teacher`
* `Course`
* `Grade`

## 3. Klinika tizimi

Klasslar:

* `Doctor`
* `Patient`
* `Appointment`

## 4. Bank tizimi

Klasslar:

* `User`
* `Account`
* `Card`
* `Transaction`

## 5. Online do‘kon

Klasslar:

* `Product`
* `Cart`
* `Order`
* `Payment`

---

# Xulosa

Bu qismda siz OOP ning deyarli barcha asosiy mavzularini:

* kod misollari
* savollar
* mashqlar

orqali mustahkamladingiz.

Endi eng to‘g‘ri yo‘l shu:

avval har bir bo‘limdagi kodlarni o‘zingiz yozib chiqing, keyin mashqlarni mustaqil bajaring, undan keyin mini loyiha qiling.

Shunda OOP siz uchun nazariya emas, amaliy ko‘nikmaga aylanadi.