### izveidot number guessing speel ar Pyton  programmēšanas valodu

### Saturs

### 1.Spēles apraksts
Interisants,spēle, kas atīsta loģiku.
### 2.Spēles loģika

Dators nejauši ģenerē vienu skaitli no 1 līdz 100. Tālāk piedāvā spēlētājiem uzminēt to skaitli utt

Spēles loģika ir labi aprakstīta šajā kodā:
```py
import random
repeat= True
while repeat:
    number = random.randint(1, 100)
    #print(number) 
    guess = 0
    tries = 0

    while guess != number:
        if guess < number:
            print("Pamēģini lielāku skaitli.")
        else:
            print("Pamēģini mazāku skaitli.")

        guess = int(input("Uzmini skaitli:"))
        tries+=1
    else:
        if tries<3:
           print(f"WOW!uzminēji tikai pēc {tries} reizēm!")
        elif tries < 6:
            print(f"Nav slikti.tu uzminēji pēc {tries} reizēm!")
        else:
            print("Hmm...vajadzētu patrenēties,uzminēji")       
    response = input("Vai gribi turpināt? y/n:") 
    if response == "y":
        repeat =True
    elif response == "n":
        repeat = False
        print("Paldies par spēli! Bye,bye!")
```

