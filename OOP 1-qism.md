# Python OOP bo‘yicha ultra mukammal to‘liq darslik

## O‘quvchilar, talabalar va yangi boshlovchilar uchun chuqur, batafsil va tartibli qo‘llanma

---

## Mundarija

1. [Kirish](#kirish)
2. [OOP nima](#oop-nima)
3. [Nima uchun OOP kerak](#nima-uchun-oop-kerak)
4. [Dasturlashda OOP ning o‘rni](#dasturlashda-oop-ning-orni)
5. [Class tushunchasi](#class-tushunchasi)
6. [Object tushunchasi](#object-tushunchasi)
7. [Class va object farqi](#class-va-object-farqi)
8. [Attribute tushunchasi](#attribute-tushunchasi)
9. [Method tushunchasi](#method-tushunchasi)
10. [`self` tushunchasi](#self-tushunchasi)
11. [`__init__` konstruktori](#__init__-konstruktori)
12. [Obyekt yaratish va ishlatish](#obyekt-yaratish-va-ishlatish)
13. [Instance attribute va class attribute](#instance-attribute-va-class-attribute)
14. [Method turlari](#method-turlari)
15. [OOP ning 4 ta asosiy tamoyili](#oop-ning-4-ta-asosiy-tamoyili)
16. [Inkapsulyatsiya](#inkapsulyatsiya)
17. [Abstraksiya](#abstraksiya)
18. [Meros olish](#meros-olish)
19. [Polimorfizm](#polimorfizm)
20. [Method overriding](#method-overriding)
21. [Method overloading haqida](#method-overloading-haqida)
22. [`super()` funksiyasi](#super-funksiyasi)
23. [Protected va private atributlar](#protected-va-private-atributlar)
24. [Getter, setter va `property`](#getter-setter-va-property)
25. [Magic methods](#magic-methods)
26. [Composition, aggregation, association](#composition-aggregation-association)
27. [Abstract class](#abstract-class)
28. [Interface g‘oyasi](#interface-goyasi)
29. [Dataclass](#dataclass)
30. [OOP da yaxshi kod yozish qoidalari](#oop-da-yaxshi-kod-yozish-qoidalari)
31. [Real modellashtirish misollari](#real-modellashtirish-misollari)
32. [Klinika tizimi misolida OOP](#klinika-tizimi-misolida-oop)
33. [Bank tizimi misolida OOP](#bank-tizimi-misolida-oop)
34. [Online do‘kon misolida OOP](#online-dokon-misolida-oop)
35. [O‘quvchilar eng ko‘p qiladigan xatolar](#oquvchilar-eng-kop-qiladigan-xatolar)
36. [OOP ni o‘rganish strategiyasi](#oop-ni-organish-strategiyasi)
37. [Juda qisqa konspekt](#juda-qisqa-konspekt)
38. [Xulosa](#xulosa)

---

# Kirish

Dasturlashni endi o‘rganayotgan odam boshida quyidagi mavzularni o‘rganadi:

* o‘zgaruvchilar
* sonlar
* matnlar
* shart operatorlari
* sikllar
* funksiyalar
* list, tuple, set, dictionary

Bu mavzular juda muhim. Lekin vaqt o‘tishi bilan dasturlar kattalashadi. Kichik dasturda hamma narsa oddiy ko‘rinadi, ammo katta loyihada vaziyat boshqacha bo‘ladi.

Masalan, sizda quyidagi tizim bo‘lishi mumkin:

* foydalanuvchilar
* rollar
* kurslar
* mahsulotlar
* buyurtmalar
* klinikalar
* shifokorlar
* bemorlar
* qabul yozuvlari
* to‘lovlar

Endi bularning hammasini oddiy funksiyalar bilan boshqarish qiyinlashadi. Kodlar tarqalib ketadi, ma’lumotlar chalkashadi, qaysi joy qaysi narsaga tegishli ekanini tushunish qiyin bo‘ladi. Ana shunda **OOP** kerak bo‘ladi.

**OOP** dasturdagi narsalarni real hayotdagi obyektlarga o‘xshatib tuzishga yordam beradi.

---

# OOP nima

**OOP** — bu **Object Oriented Programming**, ya’ni **Obyektga yo‘naltirilgan dasturlash**.

Bu dasturlash usulida dastur:

* klasslar
* obyektlar
* atributlar
* metodlar

asosida quriladi.

Sodda qilib aytganda:

> OOP — ma’lumot va xatti-harakatni bir joyga yig‘ish usuli.

Masalan, `Car` degan klassni olaylik.

Mashinaning:

* markasi
* rangi
* narxi
* tezligi

bo‘lishi mumkin. Bular ma’lumot.

Mashina:

* yuradi
* to‘xtaydi
* signal beradi

Bular xatti-harakat.

OOP da shu ikkalasi bitta tuzilma ichida saqlanadi.

---

# Nima uchun OOP kerak

## 1. Kodni tartibli qiladi

Agar bitta obyektga tegishli ma’lumot va metodlar bitta klass ichida bo‘lsa, kod juda tushunarli bo‘ladi.

Masalan, `Student` klassida:

* ism
* yosh
* kurs

atribut bo‘ladi.

Va shu klass ichida:

* tanishtir()
* o‘qish()
* baho_ko‘rsatish()

kabi metodlar bo‘ladi.

---

## 2. Katta loyihalarda qulay

Katta tizimlarda OOP juda foydali:

* CRM
* ERP
* bank tizimi
* klinika tizimi
* maktab tizimi
* online do‘kon

Bunday loyihalarda ma’lumotlar juda ko‘p bo‘ladi. OOP ularni tartibli saqlashga yordam beradi.

---

## 3. Qayta foydalanish imkonini beradi

Bir klassni bir marta yozib, undan ko‘p marta foydalanish mumkin.

Masalan, `User` klassidan:

* Admin
* Teacher
* Student
* Doctor

kabi klasslar hosil qilish mumkin.

---

## 4. Haqiqiy hayotni modellashtirish oson bo‘ladi

Real hayotdagi obyektlarni dasturda ifodalash qulaylashadi.

Masalan:

* bemor
* shifokor
* appointment
* mahsulot
* savat
* buyurtma

---

## 5. Xatolarni kamaytiradi

Ma’lumotni himoyalash, noto‘g‘ri qiymat kiritishni kamaytirish va mantiqni aniq bo‘lishiga yordam beradi.

---

# Dasturlashda OOP ning o‘rni

OOP hamma muammoning yagona yechimi emas. Lekin juda katta foydali paradigma.

Ba’zi joylarda oddiy funksional yondashuv yetadi. Masalan:

* kichik kalkulyator
* sodda konvertor
* juda kichik skript

Lekin quyidagi joylarda OOP juda qulay:

* foydalanuvchilar bilan ishlash
* rolli tizimlar
* murakkab modellar
* katta backend
* GUI dasturlar
* o‘yinlar

Demak, OOP ni bilish professional dasturchi bo‘lish uchun juda muhim.

---

# Class tushunchasi

**Class** — bu obyekt yaratish uchun shablon.

Sodda qilib:

> Class — qolip.

Masalan, `Talaba` degan klass yozsak, bu hali aniq bitta odam emas. Bu umumiy model.

```python
class Talaba:
    pass
```

Bu yerda `Talaba` — klass.

Class real hayotdagi obyektning sxemasi bo‘ladi.

### Misol bilan tushunish

Agar siz non qolipi ko‘rgan bo‘lsangiz:

* qolip — class
* shu qolipda pishgan non — object

Yoki:

* uy chizmasi — class
* shu chizma asosida qurilgan uy — object

---

# Object tushunchasi

**Object** — klass asosida yaratilgan aniq nusxa.

```python
class Talaba:
    pass

t1 = Talaba()
t2 = Talaba()
```

Bu yerda:

* `t1` — object
* `t2` — object

Ikkalasi bir xil klassdan yaratilgan, lekin ular ikki xil obyekt.

### Muhim nuqta

Bir klassdan juda ko‘p obyekt yaratish mumkin.

Masalan:

```python
class Car:
    pass

car1 = Car()
car2 = Car()
car3 = Car()
```

Hammasi `Car` klassidan, lekin alohida obyektlar.

---

# Class va object farqi

Bu mavzu juda muhim. Ko‘pchilik yangi boshlovchilar chalkashtiradi.

## Class

* shablon
* qolip
* umumiy model

## Object

* aniq nusxa
* ishlatiladigan real instansiya

### Misol

`Student` — class
`Ali`, `Vali`, `Madina` — object

Yoki:

`Car` — class
`oq Malibu`, `qora Cobalt`, `kulrang Nexia` — object

---

# Attribute tushunchasi

**Attribute** — obyektning xususiyati.

Masalan, talabaning:

* ismi
* yoshi
* kursi
* bahosi

atribut bo‘lishi mumkin.

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Bu yerda:

* `self.name`
* `self.age`

atributlar.

### Atribut nimani anglatadi

Atribut obyekt haqida ma’lumot saqlaydi.

Masalan:

* `Car` uchun `color`
* `Phone` uchun `brand`
* `Patient` uchun `phone_number`

---

# Method tushunchasi

**Method** — klass ichida yozilgan funksiya.

```python
class Student:
    def say_hello(self):
        print("Salom")
```

Bu yerda `say_hello()` — method.

### Funksiya va method farqi

## Funksiya

Klassdan tashqarida yoziladi.

## Method

Klass ichida yoziladi.

### Misol

Talaba:

* tanishtiradi
* o‘qiydi
* yuguradi

Shular method bo‘lishi mumkin.

---

# `self` tushunchasi

`self` — aynan shu obyektning o‘zini bildiradi.

Bu OOP dagi eng asosiy tushunchalardan biri.

```python
class Student:
    def __init__(self, name):
        self.name = name
```

Bu yerda `self.name` degani:

> aynan shu obyektning `name` atributi

### Misol

```python
class Student:
    def __init__(self, name):
        self.name = name

    def introduce(self):
        print(f"Mening ismim {self.name}")

s1 = Student("Ali")
s2 = Student("Vali")

s1.introduce()
s2.introduce()
```

Bu yerda:

* `s1` o‘zining `name` ini ishlatadi
* `s2` o‘zining `name` ini ishlatadi

### Nega `self` kerak

Bitta klassdan ko‘p obyekt yaratiladi. `self` qaysi obyekt bilan ishlayotganingizni bildiradi.

---

# `__init__` konstruktori

`__init__` — obyekt yaratilgan paytda avtomatik ishlaydigan maxsus metod.

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

```python
s = Student("Ali", 18)
```

Bu paytda `__init__` avtomatik ishlaydi.

### Vazifasi

* boshlang‘ich qiymat berish
* obyektni tayyorlash
* kerakli atributlarni o‘rnatish

### Nega konstruktor deyiladi

Chunki u obyektning dastlabki holatini “quradi”.

---

# Obyekt yaratish va ishlatish

Quyidagi misolni ko‘ramiz:

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def info(self):
        print(f"Brand: {self.brand}, Color: {self.color}")

car1 = Car("Chevrolet", "oq")
car2 = Car("Kia", "qora")

car1.info()
car2.info()
```

Bu yerda:

* `Car` — class
* `car1`, `car2` — object
* `brand`, `color` — attribute
* `info()` — method

Bu juda klassik OOP misoli.

---

# Instance attribute va class attribute

Bu mavzu juda muhim.

## Instance attribute

Har bir obyektga alohida tegishli atribut.

```python
class Student:
    def __init__(self, name):
        self.name = name
```

Bu yerda `name` har bir student uchun alohida.

---

## Class attribute

Barcha obyektlar uchun umumiy atribut.

```python
class Student:
    school = "45-maktab"

    def __init__(self, name):
        self.name = name
```

Bu yerda `school` — class attribute.

### Misol

```python
s1 = Student("Ali")
s2 = Student("Vali")

print(s1.school)
print(s2.school)
```

Ikkalasi uchun ham bitta qiymat chiqadi.

---

## Farqi

### Instance attribute

Har bir obyekt uchun alohida bo‘ladi.

### Class attribute

Barcha obyektlar uchun umumiy bo‘ladi.

---

# Method turlari

Python OOP da uchta asosiy method turi bor:

1. instance method
2. class method
3. static method

---

## 1. Instance method

Bu oddiy metod.

```python
class Student:
    def hello(self):
        print("Salom")
```

Bu obyekt orqali ishlaydi.

```python
s = Student()
s.hello()
```

Bu yerda `self` bor.

---

## 2. Class method

Bu metod klass bilan ishlaydi.

```python
class Student:
    school = "Najot"

    @classmethod
    def show_school(cls):
        print(cls.school)
```

```python
Student.show_school()
```

Bu yerda `cls` — klassning o‘zi.

### Qachon kerak

* class attribute bilan ishlaganda
* alternative constructor yozganda

---

## 3. Static method

Bu metod `self` ham, `cls` ham ishlatmaydi.

```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b
```

```python
print(Math.add(3, 5))
```

### Qachon kerak

* klass bilan mantiqan bog‘liq
* lekin obyekt yoki klass holatiga bog‘liq emas

---

# OOP ning 4 ta asosiy tamoyili

OOP ning yuragi bo‘lgan 4 tamoyil:

1. **Inkapsulyatsiya**
2. **Abstraksiya**
3. **Meros olish**
4. **Polimorfizm**

Bu 4 tamoyilni juda chuqur tushunish kerak.

---

# Inkapsulyatsiya

## Ta’rif

**Inkapsulyatsiya** — ma’lumot va uni boshqaruvchi metodlarni bitta klass ichiga jamlash hamda ichki ma’lumotni himoyalash.

Sodda qilib:

> Ma’lumotni nazoratsiz o‘zgartirishdan saqlash.

---

## Hayotiy misol

Bank kartasidagi balansni olaylik.

Siz:

* balansni ko‘rishingiz mumkin
* pul qo‘shishingiz mumkin
* pul yechishingiz mumkin

Lekin:

* istagancha qo‘lda balansni minus million qilolmaysiz

Sababi bu jarayon nazorat qilinadi.

Bu — inkapsulyatsiya.

---

## Kod misol

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount

    def show_balance(self):
        return self.__balance
```

```python
acc = BankAccount("Ali", 1000)
acc.deposit(500)
acc.withdraw(200)
print(acc.show_balance())
```

---

## Nega `__balance` ishlatildi

Ikki pastki chiziq bilan yozilgan atribut tashqaridan to‘g‘ridan-to‘g‘ri ishlatishni cheklaydi.

Bu:

* himoya beradi
* noto‘g‘ri o‘zgarishni kamaytiradi
* klass ichidagi qoidalarga bo‘ysundirishga yordam beradi

---

## Inkapsulyatsiyaning foydalari

* ma’lumot himoyalanadi
* xatolar kamayadi
* nazorat kuchayadi
* kod ishonchli bo‘ladi

---

## Juda sodda eslab qolish

> Inkapsulyatsiya = himoyalash + tartib

---

# Abstraksiya

## Ta’rif

**Abstraksiya** — murakkab ichki jarayonlarni yashirib, foydalanuvchiga faqat kerakli qismini ko‘rsatish.

Sodda qilib:

> Murakkab narsani sodda ko‘rsatish.

---

## Hayotiy misol

Mashina haydayotgan odam:

* rulni buradi
* gazni bosadi
* tormoz qiladi

Lekin u:

* piston qanday ishlashini
* yoqilg‘i qanday yonishini
* dvigatel ichida nima bo‘layotganini

bilib turishi shart emas.

Bu — abstraksiya.

---

## Kod misol

```python
class Car:
    def start(self):
        print("Mashina ishga tushdi")

    def stop(self):
        print("Mashina to‘xtadi")
```

Foydalanuvchi faqat:

* `start()`
* `stop()`

ni ko‘radi.

Ichidagi texnik murakkablik yashirilgan.

---

## Inkapsulyatsiya va abstraksiya farqi

Bu juda muhim.

### Inkapsulyatsiya

Ma’lumotni himoyalaydi.

### Abstraksiya

Murakkablikni yashiradi.

### Juda sodda farq

* inkapsulyatsiya: “nimani cheklaymiz?”
* abstraksiya: “nimani soddalashtiramiz?”

---

# Meros olish

## Ta’rif

**Meros olish** — bir klass boshqa klassdan atribut va metodlarni olishi.

Sodda qilib:

> Yangi klass tayyor imkoniyatni oladi.

---

## Hayotiy misol

`Animal` degan umumiy klass bo‘lsin:

* yeydi
* uxlaydi

`Dog` klassi ham hayvon, `Cat` klassi ham hayvon.

Shuning uchun ular `Animal` dan meros olishi mumkin.

---

## Kod misol

```python
class Animal:
    def eat(self):
        print("Ovqat yeyapti")

    def sleep(self):
        print("Uxlayapti")


class Dog(Animal):
    def bark(self):
        print("Vov-vov")
```

```python
dog = Dog()
dog.eat()
dog.sleep()
dog.bark()
```

Bu yerda `Dog`, `Animal` dan:

* `eat()`
* `sleep()`

ni oldi.

Va o‘zi:

* `bark()`

ni qo‘shdi.

---

## Ota va voris klass

* `Animal` — ota klass
* `Dog` — voris klass

Yoki:

* parent class
* child class

---

## Meros olishning foydasi

* takroriy kod kamayadi
* umumiy mantiq bitta joyda bo‘ladi
* kengaytirish oson bo‘ladi

---

## Qachon inheritance ishlatish kerak

Agar munosabat:

> “A bu B ning turi”

bo‘lsa.

Masalan:

* Dog is an Animal
* Teacher is a User

Agar:

> “A da B bor”

bo‘lsa, composition yaxshiroq.

Masalan:

* Car has an Engine
* Order has Products

---

# Polimorfizm

## Ta’rif

**Polimorfizm** — bir xil metodning turli klasslarda turlicha ishlashi.

Sodda qilib:

> Nomi bir xil, natijasi har xil.

---

## Hayotiy misol

Ovoz chiqarish:

* it — vovullaydi
* mushuk — miyovlaydi
* sigir — mo‘raydi

Hammasida harakat:

* `sound()`

Lekin natija turli.

---

## Kod misol

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
```

```python
animals = [Dog(), Cat(), Cow()]
for animal in animals:
    animal.sound()
```

Bu polimorfizm.

---

## Nega muhim

Chunki funksiyalar obyekt turiga qattiq bog‘lanmasdan ishlay oladi.

```python
def make_sound(animal):
    animal.sound()
```

Bu funksiya `Dog`, `Cat`, `Cow` bilan ishlayveradi.

---

# Method overriding

Agar voris klass ota klass metodini qayta yozsa, bu **overriding** deyiladi.

```python
class Animal:
    def sound(self):
        print("Hayvon ovoz chiqarmoqda")


class Dog(Animal):
    def sound(self):
        print("It vovulladi")
```

Bu yerda `Dog`, `sound()` metodini qayta yozdi.

Bu polimorfizmning muhim ko‘rinishi.

---

# Method overloading haqida

Python’da Java yoki C++ dagidek klassik method overloading yo‘q.

Masalan, bunday yozsangiz:

```python
class Test:
    def add(self, a):
        return a

    def add(self, a, b):
        return a + b
```

ikkinchi metod birinchisini bosib ketadi.

Shuning uchun Python’da odatda quyidagilar ishlatiladi:

* default parametr
* `*args`
* `**kwargs`

### Misol

```python
class Test:
    def add(self, a, b=0):
        return a + b
```

Yoki:

```python
class Test:
    def add(self, *args):
        return sum(args)
```

---

# `super()` funksiyasi

`super()` — ota klass metodiga murojaat qilish uchun ishlatiladi.

```python
class Animal:
    def __init__(self, name):
        self.name = name


class Dog(Animal):
    def __init__(self, name, color):
        super().__init__(name)
        self.color = color
```

Bu yerda:

* `name` ota klassdan olinadi
* `color` voris klassga qo‘shiladi

### Nega kerak

Tayyor kodni qayta yozmaslik uchun.

---

# Protected va private atributlar

Python’da qat’iy access modifier yo‘q, lekin usullar bor.

## Public

```python
self.name
```

Hamma joydan ishlatish mumkin.

## Protected

```python
self._name
```

Bu:

> “ichki foydalanish uchun” degan signal.

## Private

```python
self.__name
```

Bu kuchliroq yashirishni bildiradi.

---

# Getter, setter va `property`

Ba’zida atributni to‘g‘ridan-to‘g‘ri emas, maxsus nazorat bilan ishlatish kerak bo‘ladi.

## Oddiy getter va setter

```python
class Student:
    def __init__(self, age):
        self.__age = age

    def get_age(self):
        return self.__age

    def set_age(self, age):
        if age > 0:
            self.__age = age
```

---

## `property` bilan qulay usul

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
```

```python
s = Student(18)
print(s.age)
s.age = 20
print(s.age)
```

Bu tashqaridan atributga o‘xshaydi, lekin ichkarida nazorat ishlaydi.

---

# Magic methods

Python’da maxsus metodlar bor. Ular obyekt xatti-harakatini o‘zgartiradi.

Masalan:

* `__init__`
* `__str__`
* `__repr__`
* `__len__`
* `__add__`

---

## `__str__`

Obyektni chiroyli ko‘rsatish uchun.

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

## `__len__`

`len()` bilan ishlashi uchun.

```python
class Box:
    def __init__(self, items):
        self.items = items

    def __len__(self):
        return len(self.items)

b = Box([1, 2, 3])
print(len(b))
```

---

## `__add__`

`+` operatori uchun.

```python
class Number:
    def __init__(self, value):
        self.value = value

    def __add__(self, other):
        return Number(self.value + other.value)

    def __str__(self):
        return str(self.value)

a = Number(5)
b = Number(7)
print(a + b)
```

---

# Composition, aggregation, association

OOP dagi hamma bog‘lanish inheritance emas.

Bu juda muhim.

---

# Composition

Bir obyekt boshqa obyektni o‘z ichida yaratadi va unga kuchli bog‘langan bo‘ladi.

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
```

Bu composition.

### Ma’nosi

`Car` ichida `Engine` bor.

Bu:

> has-a

bog‘lanish.

---

# Aggregation

Bir obyekt boshqa obyekt bilan ishlaydi, lekin u mustaqil ham yashay oladi.

```python
class Teacher:
    def __init__(self, name):
        self.name = name


class Department:
    def __init__(self, teacher):
        self.teacher = teacher
```

Bu yerda `Teacher` alohida ham mavjud bo‘la oladi.

---

# Association

Bu obyektlar orasidagi umumiy bog‘lanish.

Masalan:

* student course ga yoziladi
* doctor patientni ko‘radi
* user order qiladi

Bu inheritance bo‘lishi shart emas.

---

# Abstract class

Ba’zan klass shunchaki umumiy shablon bo‘ladi. Undan obyekt yaratish emas, voris klasslar uchun majburiy struktura berish kerak bo‘ladi.

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def sound(self):
        pass
```

Bu yerda `Animal` — abstract class.

```python
class Dog(Animal):
    def sound(self):
        print("Vov-vov")
```

Agar `Dog` `sound()` metodini yozmasa, xato bo‘ladi.

---

# Interface g‘oyasi

Python’da alohida `interface` kalit so‘zi yo‘q. Lekin interface g‘oyasi bor.

Ma’nosi:

> Ma’lum klasslar ma’lum metodlarni albatta amalga oshirishi kerak.

Masalan:

* barcha to‘lov klasslari `pay()` metodiga ega bo‘lsin
* barcha fayl saqlash klasslari `save()` metodiga ega bo‘lsin

Bu yondashuv katta loyihalarda juda foydali.

---

# Dataclass

Agar klass asosan ma’lumot saqlash uchun bo‘lsa, `dataclass` juda qulay.

```python
from dataclasses import dataclass

@dataclass
class Student:
    name: str
    age: int
    grade: float
```

```python
s = Student("Ali", 18, 4.8)
print(s)
```

### Foydasi

* `__init__` avtomatik yoziladi
* `__repr__` avtomatik hosil bo‘ladi
* kod qisqaradi

---

# OOP da yaxshi kod yozish qoidalari

## 1. Har narsani class qilmang

Ba’zi joyda oddiy funksiya yetadi.

## 2. Har narsaga inheritance ishlatmang

Ko‘p joyda composition yaxshiroq.

## 3. Klassning vazifasi aniq bo‘lsin

Bitta klass juda ko‘p ish qilmasin.

## 4. Ma’lumotni himoya qiling

Kerak bo‘lsa private/protected ishlating.

## 5. Tashqi interfeys sodda bo‘lsin

Ichki murakkablikni yashirib, ishlatishni qulay qiling.

## 6. Nomlash toza bo‘lsin

* klass nomi odatda `PascalCase`
* method va variable odatda `snake_case`

---

# Real modellashtirish misollari

OOP ni tushunish uchun real obyektlarni model qilish juda foydali.

Masalan:

* maktab tizimi
* klinika tizimi
* bank tizimi
* online shop
* kutubxona
* telegram bot tizimi

---

# Klinika tizimi misolida OOP

Quyidagi klasslar bo‘lishi mumkin:

* `User`
* `Doctor`
* `Employee`
* `Patient`
* `Appointment`
* `Clinic`

### Mantiq

* `Doctor` `User` dan meros olishi mumkin
* `Appointment` ichida `Doctor` va `Patient` bo‘ladi
* `Patient` ma’lumotlari alohida model bo‘ladi
* `Clinic` ichida ko‘plab doctorlar bo‘lishi mumkin

### Misol

```python
class User:
    def __init__(self, full_name, phone):
        self.full_name = full_name
        self.phone = phone


class Doctor(User):
    def __init__(self, full_name, phone, specialty):
        super().__init__(full_name, phone)
        self.specialty = specialty


class Patient(User):
    def __init__(self, full_name, phone):
        super().__init__(full_name, phone)


class Appointment:
    def __init__(self, doctor, patient, date):
        self.doctor = doctor
        self.patient = patient
        self.date = date
```

Bu juda toza modellashtirish.

---

# Bank tizimi misolida OOP

Klasslar:

* `User`
* `Account`
* `Card`
* `Transaction`

### Misol

```python
class Account:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount

    def show_balance(self):
        return self.__balance
```

Bu inkapsulyatsiya uchun juda yaxshi misol.

---

# Online do‘kon misolida OOP

Klasslar:

* `User`
* `Product`
* `Cart`
* `Order`
* `Payment`

### Misol

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price


class Cart:
    def __init__(self):
        self.products = []

    def add_product(self, product):
        self.products.append(product)

    def total_price(self):
        return sum(product.price for product in self.products)
```

Bu composition ga ham misol.

---

# O‘quvchilar eng ko‘p qiladigan xatolar

## 1. `self` ni unutish

Noto‘g‘ri:

```python
class A:
    def hello():
        print("Salom")
```

To‘g‘ri:

```python
class A:
    def hello(self):
        print("Salom")
```

---

## 2. Class va object ni chalkashtirish

`Student` — class
`student1` — object

---

## 3. Instance va class attribute ni aralashtirish

`self.name` va `Student.school` boshqa-boshqa narsalar.

---

## 4. Har joyda inheritance ishlatish

Ko‘p joyda composition yaxshiroq.

---

## 5. OOP ni faqat class yozish deb o‘ylash

OOP bu:

* model qilish
* mas’uliyat taqsimlash
* bog‘lanishni to‘g‘ri tanlash
* dizayn

demakdir.

---

## 6. Juda katta klass yozish

Bitta klass:

* user
* payment
* sms
* analytics
* auth

hammasini qilsa, bu noto‘g‘ri.

---

# OOP ni o‘rganish strategiyasi

## 1-bosqich

* class
* object
* attribute
* method
* `self`
* `__init__`

## 2-bosqich

* instance attribute
* class attribute
* instance/class/static method

## 3-bosqich

* inkapsulyatsiya
* abstraksiya
* inheritance
* polymorphism

## 4-bosqich

* overriding
* `super()`
* private/protected
* property

## 5-bosqich

* magic methods
* composition
* abstract class
* dataclass

## 6-bosqich

* real loyiha modellashtirish
* mini CRM
* online shop
* school system
* clinic system

---

# Juda qisqa konspekt

## Class

Obyekt uchun shablon.

## Object

Class asosida yaratilgan nusxa.

## Attribute

Obyekt xususiyati.

## Method

Klass ichidagi funksiya.

## `self`

Shu obyektning o‘zi.

## `__init__`

Obyekt yaratilganda ishlaydigan konstruktor.

## Inkapsulyatsiya

Ma’lumotni himoyalash.

## Abstraksiya

Murakkablikni yashirish.

## Meros olish

Boshqa klassdan xususiyat va metod olish.

## Polimorfizm

Bir xil metodning turli ko‘rinishda ishlashi.

## Overriding

Metodni qayta yozish.

## `super()`

Ota klass metodiga murojaat qilish.

## Composition

Bir obyekt ichida boshqa obyekt.

## Abstract class

Majburiy umumiy shablon.

## Dataclass

Ma’lumot saqlash uchun qulay klass.

---

# Xulosa

OOP — bu faqat `class` va `object` emas. Bu dastur tuzish usuli, fikrlash modeli va arxitektura asosidir.

OOP ni yaxshi tushungan dasturchi:

* katta loyihani yaxshiroq tashkil qiladi
* kodni toza yozadi
* qayta foydalaniladigan yechimlar yaratadi
* real hayotdagi tizimlarni aniq modellashtiradi

Eng muhim narsa shuki, OOP ni faqat yodlab bo‘lmaydi. Uni:

* misol yozib
* klasslar tuzib
* kichik loyihalar qilib
* real modellar ustida ishlash orqali

yaxshi o‘rganish mumkin.

---

# Eng qisqa eslab qolish formulasi

> **Class** — shablon
> **Object** — nusxa
> **Attribute** — xususiyat
> **Method** — amal
> **Inkapsulyatsiya** — himoya
> **Abstraksiya** — soddalashtirish
> **Meros olish** — davom ettirish
> **Polimorfizm** — turlicha ishlash
