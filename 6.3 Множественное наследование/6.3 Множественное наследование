import random

class Animal:
    live = True
    sound = None
    _DEGREE_OF_DANGER = 0

    def __init__(self, speed):
        self._cords = [0, 0, 0]
        self.speed = speed

    def move(self, dx, dy, dz):
        self.dx = dx*self.speed
        self.dy = dy*self.speed
        self.dz = dz*self.speed
        if self.dz >= 0:
            self._cords = [self.dx, self.dy, self.dz]
        elif self.dz < 0:
            print("It's too deep, i can't dive :(")

    def get_cords(self):
        print(f'X:{self.dx}, Y:{self.dy}, Z:{self.dz}')

    def attack(self):
        if self._DEGREE_OF_DANGER < 5:
            print("Sorry, i'm peaceful :)")
        elif self._DEGREE_OF_DANGER > 5:
            print("Be careful, i'm attacking you 0_0")

    def speak(self):
        print(self.sound)

class Bird(Animal):
    beak = True

    def lay_eggs(self):
        all_numbers = [1, 2, 3, 4]
        task = random.choice(all_numbers)
        print(f'Here are(is) {task} eggs for you')

class AquaticAnimal(Animal):
    _DEGREE_OF_DANGER = 3

    def dive_in(self, dz):
        self.dive_in_dz = dz
        self.ddz = self.dz - abs(self.dive_in_dz * self.speed) / 2
        self.move(int(self.dx/self.speed), int(self.dy/self.speed), int(self.ddz))

class PoisonousAnimal(Animal):
    _DEGREE_OF_DANGER = 8

class Duckbill(Bird, PoisonousAnimal, AquaticAnimal):
    sound = "Click-click-click"

db = Duckbill(10)

print(db.live)
print(db.beak)

db.speak()
db.attack()

db.move(1, 2, 3)
db.get_cords()
db.dive_in(6)
db.get_cords()

db.lay_eggs()