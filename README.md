#Module qui va etre utiliser au cours de ce jeu
import random

choix = ["python", "programmation", "algorithme", "Numerique", "sciences", "informatique"]
solution = random.choice(choix)

tentatives = 7
#creation d'une variable qui va servir d'affichage 
affichage = ""
lettres_trouvees = ""

for l in solution:
  affichage = affichage + "_ "

print(">> Hello so let's get started <<")

while tentatives > 0:
  print("\nMot à deviner : ", affichage)
  proposition = input("proposez une lettre : ")
  
    if proposition in solution:
      lettres_trouvees = lettres_trouvees + proposition
      print("-> very well ! carry on")
      
    else:
      tentatives = tentatives - 1
      print("-> Nope\n")
      if tentatives==0:
        print(" ============ ")
      if tentatives<=1:
        print(" ||/       |  ")
      if tentatives<=2:
        print(" ||        0  ")
      if tentatives<=3:
        print(" ||       /|\ ")
      if tentatives<=4:
        print(" ||       /|\  ")
      if tentatives<=5:
        print("/||           ")
      if tentatives<=6:
        print("==============\n")

      

 
  
  
  

