class Pet:

   def __init__(self, name, species):
       self.name = name
       self.species = species
       self.hungry = True
       self.tired = True
       self.happy = False

   def feed(self):
       if self.hungry:
        print(f"{self.name} has been fed.")
        self.hungry = False
        print(f"{self.name} is not hungry.")

   def sleep(self):
       if self.tired:
        print(f"{self.name} has gone to sleep.")
        self.tired = False
        print(f"{self.name} is not tired.")


   def play(self):
       if self.happy:
        print(f"{self.name} is already playing.")
        print(f"{self.name} is playing now.")
        self.happy = True

   def end_of_day(self):
       print(f"species - {self.species}")
       print(f"hungry _ {round(self.hungry)}")
       print(f"happy _ {self.happy}")

   def life(self,day):
       for day in range (1,365):
           day_str = f"Day{day}of{self.name}"
           day = "Day" + str(day+1) + "of" + self.name + "life"
           print(f"{day:=^50}")
           live_cude = random.randint(1,3)
           if live_cude ==1:
              self.to_Pet()
           elif live_cude ==2:
              self.to_sleep()
           elif live_cude ==3:
               self.to_play()
           elif live_cude ==4:
               self.to_feed()
               print(f"{self.name}died on day{day}")
               self.end_of_day()

cat =Pet(name="Cat")

for day in range(365):
    if cat.life == False:
        break
    cat.life(day)


