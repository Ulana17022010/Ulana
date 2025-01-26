class Student:

    def __init__(self, name):
        self.name = name
        self.gladness = 50
        self.progress = 0
        self.alive = True
        self.money = 0

    def to_study(self):
        print("Time to study")
        self.progress += 0.12
        self.gladness -= 3
        exec .money -= 0.6

    def to_chill(self):
      if self.money >= 10:
        print("Time to rest")
        self.gladness += 5
        self.progress -= 0.1

    def to_sleep(self):
         print("Time to sleep")
         self.gladness += 3
         self.progress -= 0.05
         self.money -= 0.02

    def to_work(self):
        print("Time to work")
        self.money += 20
        self.progress += 0.05
        self.gladness += 2

    def is_alive(self):
        if self.progress < -0.5:
            print("Cast out...")
            self.alive = False
        elif self.gladness <= 0:
            print("Depression...")
            self.alive = False
        elif self.progress > 5:
            print("Passed externally...")
            self.alive = False

    def end_of_day(self):
        print(f"Gladness = {self.gladness}")
        print(f"Progress = {round(self.progress)}")
        print(f"Money = {self.money}")


    def end_of_day(self):
        print(f"Gladness - {self.gladness}")
        print(f"Progress - {round(self.progress, 2)}")

    def life(self, day):
     for day in range (1,365):
       day_str = f"Dy{day}of{self.name}"
       day = "Day " + str(day+1) + " of " + self.name + " life"
       print(f"{day:=^50}")
       live_cube = random.randint(1,3)
       if live_cube ==1:
          self.to_student()
       elif live_cube == 2:
          self.to_sleep()
       elif live_cube == 3:
          self.to_chill()
       elif live_cube == 4:
          self.end_of_work()
          self.is_alive()
          print(f"{self.name}died on day{day}")
       self.end_of_day()


nick = Student(name="Nick")

for day in range(365):
    if nick.alive == False:
        break
    nick.life(day)
