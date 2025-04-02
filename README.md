# orianted-programing
1)# Base class representing a Superhero
class Superhero:
    def __init__(self, name, power, alias):
        self.name = name  # Public attribute
        self.__power = power  # Private attribute (encapsulation)
        self.alias = alias  # Public attribute

    def __get_power(self):  # Private method for encapsulation
        return self.__power

    def introduce(self):
        print(f"Hi, I'm {self.name}, also known as {self.alias}.")

    def show_power(self):
        print(f"My power is {self.__get_power()}.")

# Inherited class representing a Flying Superhero
class FlyingHero(Superhero):
    def __init__(self, name, alias, speed):
        super().__init__(name, "Flight", alias)
        self.__speed = speed  # Private attribute for speed

    def show_power(self):
        # Polymorphism: Overriding the show_power method
        print(f"As {self.alias}, I can fly at a speed of {self.__speed} mph!")

    def fly(self):
        print(f"{self.alias} is soaring through the skies!")

# Inherited class representing a Strength-based Superhero
class StrengthHero(Superhero):
    def __init__(self, name, alias, strength_level):
        super().__init__(name, "Super Strength", alias)
        self.__strength_level = strength_level  # Private attribute for strength

    def show_power(self):
        # Polymorphism: Overriding the show_power method
        print(f"As {self.alias}, my strength level is {self.__strength_level}!")

    def lift(self):
        print(f"{self.alias} can lift incredibly heavy objects!")

# Creating instances of the Superhero and its subclasses
hero1 = Superhero("Bruce Wayne", "Stealth and Intelligence", "Batman")
hero1.introduce()
hero1.show_power()

flying_hero = FlyingHero("Clark Kent", "Superman", 900)
flying_hero.introduce()
flying_hero.show_power()
flying_hero.fly()

strength_hero = StrengthHero("Diana Prince", "Wonder Woman", 100)
strength_hero.introduce()
strength_hero.show_power()
strength_hero.lift()
2)# Base class representing a Vehicle
class Vehicle:
    def move(self):
        print("The vehicle is moving.")

# Subclass representing a Car
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

# Subclass representing a Plane
class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

# Base class representing an Animal
class Animal:
    def move(self):
        print("The animal is moving.")

# Subclass representing a Dog
class Dog(Animal):
    def move(self):
        print("Running 🐕")

# Subclass representing a Bird
class Bird(Animal):
    def move(self):
        print("Flying 🦅")

# Instantiate objects of different classes
car = Car()
plane = Plane()
dog = Dog()
bird = Bird()

# Call the move() method for each object
car.move()  # Output: Driving 🚗
plane.move()  # Output: Flying ✈️
dog.move()  # Output: Running 🐕
bird.move()  # Output: Flying 🦅
