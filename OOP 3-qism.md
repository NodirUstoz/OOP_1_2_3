# Python OOP darsligi — 3-qism

## OOP dan 50 ta amaliy masala

---

## Kirish

Quyidagi masalalar OOP ni mustahkamlash uchun tuzilgan. Ular oddiydan murakkabga qarab ketadi. Masalalar quyidagi mavzularni qamrab oladi:

* class va object
* attribute va method
* `self`, `__init__`
* instance va class attribute
* inheritance
* polymorphism
* encapsulation
* abstraction
* `property`
* `super()`
* composition
* magic methods
* abstract class
* dataclass

---

# 1-bo'lim. Class va Object

## 1-masala. Talaba klassi

**Vazifa:** `Student` klassi yarating. `name` atributi bo'lsin. Object yaratib ismni chiqaring.

**Yechim:**

```python
class Student:
    def __init__(self, name):
        self.name = name


s = Student("Ali")
print(s.name)
```

---

## 2-masala. Kitob klassi

**Vazifa:** `Book` klassi yarating. `title` va `author` atributlari bo'lsin.

---

## 3-masala. Mashina klassi

**Vazifa:** `Car` klassi yarating. `brand` va `color` atributlari bo'lsin.

---

## 4-masala. Telefon klassi

**Vazifa:** `Phone` klassi yarating. `model` atributi bo'lsin.

---

## 5-masala. O'qituvchi klassi

**Vazifa:** `Teacher` klassi yarating. `name` va `subject` atributlari bo'lsin.

---

# 2-bo'lim. Methodlar

## 6-masala. Talaba o'zini tanishtirsin

**Vazifa:** `introduce()` methodi yozing.

**Yechim:**

```python
class Student:
    def __init__(self, name):
        self.name = name

    def introduce(self):
        print(f"Mening ismim {self.name}")


s = Student("Ali")
s.introduce()
```

---

## 7-masala. Mashina yurishi

**Vazifa:** `drive()` methodi yozing.

---

## 8-masala. Kitob haqida ma'lumot

**Vazifa:** `info()` methodi yozing.

---

## 9-masala. Telefon qo'ng'iroq qilsin

**Vazifa:** `call()` methodi yozing.

---

## 10-masala. O'qituvchi dars o'tsin

**Vazifa:** `teach()` methodi yozing.

---

# 3-bo'lim. `self` va `__init__`

## 11-masala. Mahsulot narxi

**Vazifa:** `Product` klassida `name` va `price` atributlari bo'lsin.

**Yechim:**

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price


p = Product("Olma", 12000)
print(p.name, p.price)
```

---

## 12-masala. 2 ta obyekt yaratish

**Vazifa:** Bir klassdan 2 ta obyekt yarating va farqli ma'lumot bering.

---

## 13-masala. Bemor klassi

**Vazifa:** `Patient` klassida `fullname` va `phone` atributlari bo'lsin.

---

## 14-masala. Kurs klassi

**Vazifa:** `Course` klassida `title` va `duration` atributlari bo'lsin.

---

## 15-masala. Kompyuter klassi

**Vazifa:** `Computer` klassida `brand`, `ram` atributlari bo'lsin.

---

# 4-bo'lim. Instance va Class Attribute

## 16-masala. Maktab nomi

**Vazifa:** `Student` klassida `school` class attribute bo'lsin.

**Yechim:**

```python
class Student:
    school = "45-maktab"

    def __init__(self, name):
        self.name = name


s1 = Student("Ali")
s2 = Student("Vali")

print(s1.school)
print(s2.school)
```

---

## 17-masala. G'ildiraklar soni

**Vazifa:** `Car` klassida `wheels = 4` bo'lsin.

---

## 18-masala. Universitet umumiy atributi

**Vazifa:** `university` class attribute yarating.

---

## 19-masala. Farqni ko'rsatish

**Vazifa:** instance va class attribute farqini amalda ko'rsating.

---

## 20-masala. Klinika nomi

**Vazifa:** `Doctor` klassida `clinic_name` class attribute bo'lsin.

---

# 5-bo'lim. Inheritance

## 21-masala. Ota klassdan method olish

**Vazifa:** `Animal` klassi va `Dog` voris klassini yozing.

**Yechim:**

```python
class Animal:
    def eat(self):
        print("Ovqat yeyapti")


class Dog(Animal):
    def bark(self):
        print("Vov-vov")


d = Dog()
d.eat()
d.bark()
```

---

## 22-masala. Person va Student

**Vazifa:** `Student`, `Person` dan meros olsin.

---

## 23-masala. Employee va Doctor

**Vazifa:** `Doctor`, `Employee` dan meros olsin.

---

## 24-masala. User va Admin

**Vazifa:** `Admin`, `User` dan meros olsin.

---

## 25-masala. Vehicle va Bus

**Vazifa:** `Bus`, `Vehicle` dan meros olsin.

---

# 6-bo'lim. Polymorphism

## 26-masala. Hayvonlar ovozi

**Vazifa:** `sound()` methodi turli klasslarda turlicha ishlasin.

**Yechim:**

```python
class Dog:
    def sound(self):
        print("Vov-vov")


class Cat:
    def sound(self):
        print("Miyov")


class Cow:
    def sound(self):
        print("Mo'-mo'")


for animal in [Dog(), Cat(), Cow()]:
    animal.sound()
```

---

## 27-masala. To'lov usullari

**Vazifa:** `pay()` methodi turlicha ishlasin.

---

## 28-masala. Uchish misoli

**Vazifa:** `fly()` methodini turli klasslarda yozing.

---

## 29-masala. Login xabarlari

**Vazifa:** `show_role()` methodi turlicha ishlasin.

---

## 30-masala. Transport harakati

**Vazifa:** `move()` methodi har xil ishlasin.

---

# 7-bo'lim. Encapsulation

## 31-masala. Private balans

**Vazifa:** `BankAccount` klassida `__balance` private atribut bo'lsin.

**Yechim:**

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def show_balance(self):
        return self.__balance


acc = BankAccount(1000)
print(acc.show_balance())
```

---

## 32-masala. Pul qo'shish

**Vazifa:** `deposit()` methodi yozing.

---

## 33-masala. Pul yechish

**Vazifa:** `withdraw()` methodi yozing.

---

## 34-masala. Baho nazorati

**Vazifa:** `Student` klassida baho private bo'lsin va setter bilan tekshirilsin.

---

## 35-masala. Hamyon

**Vazifa:** `Wallet` klassi yarating, pul private bo'lsin.

---

# 8-bo'lim. `property`

## 36-masala. Yoshni property bilan boshqarish

**Vazifa:** `Student` klassida `age` ni `@property` bilan boshqaring.

**Yechim:**

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
s.age = 20
print(s.age)
```

---

## 37-masala. Narxni nazorat qilish

**Vazifa:** `Product` klassida `price` ni `@property` bilan boshqaring.

---

## 38-masala. Maoshni boshqarish

**Vazifa:** `Employee` klassida `salary` ni `@property` bilan boshqaring.

---

## 39-masala. Baho property bilan

**Vazifa:** `Student` klassida `grade` ni `@property` bilan boshqaring.

---

## 40-masala. Ombordagi son

**Vazifa:** `StoreItem` klassida `quantity` ni `@property` bilan boshqaring.

---

# 9-bo'lim. Overriding va `super()`

## 41-masala. Ovoz chiqarishni qayta yozish

**Vazifa:** `Animal` klassidagi `sound()` methodini `Dog` klassida qayta yozing (override).

**Yechim:**

```python
class Animal:
    def sound(self):
        print("Hayvon ovoz chiqardi")


class Dog(Animal):
    def sound(self):
        print("It vovulladi")


d = Dog()
d.sound()
```

---

## 42-masala. Person va Student

**Vazifa:** `Student` klassida `super().__init__()` ishlatib `Person` dan meros oling.

---

## 43-masala. User va Admin info

**Vazifa:** `Admin` klassida `super().info()` ishlatib ota klass methodini chaqiring.

---

## 44-masala. Employee va Teacher

**Vazifa:** `Teacher` klassida `super().__init__()` ishlatib `Employee` dan meros oling.

---

## 45-masala. Vehicle va Car

**Vazifa:** `Car` klassida `Vehicle` ning `move()` methodini qayta yozing (override).

---

# 10-bo'lim. Composition

## 46-masala. Mashina va motor

**Vazifa:** `Car` klassi ichida `Engine` klassidan obyekt yarating (composition).

**Yechim:**

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


c = Car()
c.start()
```

---

## 47-masala. Kompyuter va protsessor

**Vazifa:** `Computer` klassi ichida `CPU` klassidan obyekt yarating (composition).

---

## 48-masala. Uy va xona

**Vazifa:** `House` klassi ichida `Room` klassidan obyektlar yarating (composition).

---

# 11-bo'lim. Magic methods

## 49-masala. `__str__`

**Vazifa:** `Student` klassida `__str__` magic methodini yozing.

**Yechim:**

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

## 50-masala. `__len__`

**Vazifa:** `Box` klassida `__len__` magic methodini yozing.

---

# Yakuniy tavsiyalar

Bu 50 ta masalani o'rganish uchun quyidagi tartibda ishlang:

1. Har bir kodni o'zingiz qayta yozing.
2. `print()` larni o'zgartirib natijani kuzating.
3. Atribut nomlarini almashtirib ko'ring.
4. Methodlarga qo'shimcha mantiq qo'shing.
5. Har 5 ta masaladan keyin o'zingiz 1 ta yangi masala tuzing.

---

# Eng foydali mashq usuli

Masalan, `Student` klassini oldingiz. Endi uni kengaytiring:

* `name`
* `age`
* `grade`
* `introduce()`
* `study()`
* `__str__()`
* `property`
* inheritance orqali `ExcellentStudent`

Shunday qilib bitta sodda klassdan katta model yasab borasiz. OOP aynan shunday o'rganiladi.

---

# Xulosa

Bu 50 ta masala OOP bo'yicha kuchli amaliy baza beradi. Ular orqali siz:

* class va object
* method va attribute
* inheritance
* polymorphism
* encapsulation
* property
* composition
* magic method

kabi mavzularni mustahkamlaysiz.
