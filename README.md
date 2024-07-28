print  ("Developer - не только разработчик")


class House:
    def __init__(self, name, number_of_floors):
        self.name = name
        self.number_of_floors = number_of_floors

    def go_to(self, new_floor):
        if (new_floor > self.number_of_floors or new_floor < 1):
            print("Такого этажа не существует")
        else:
            for i in range (1, new_floor+1):
                print(f"Опять сломали лифт в {self.name}, ножками, этаж!  {i} из {new_floor}")
    def __len__(self):
        #print (type (self.number_of_floors))
        #input()
        return   self.number_of_floors

    def __str__(self):
        return 'Название: ' + self.name + ", кол-во этажей " + str(self.number_of_floors)

h1 = House('ЖК Горский', 18)
h2 = House('Домик в деревне', 2)

# __str__
print(h1)
print(h2)

# __len__
print(len(h1))
print(len(h2))

#
#print()
#h1.go_to(5)
#print()
#h2.go_to(10)
#h2.walls = "Briks"
#print(h2.walls )
#print(h1.walls )
