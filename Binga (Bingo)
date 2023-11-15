# _____________________#
# Ordinateur section
# _____________________#

# Les numéros
a_1 = random.randint(1, 9)
b_1 = random.randint(1, 9)
c_1 = random.randint(1, 9)
d_1 = random.randint(1, 9)
e_1 = random.randint(1, 9)
f_1 = random.randint(1, 9)

TableauOrd = [11]  # Pour éviter la condition de Gagné
TableauOrd.append(a_1)
TableauOrd.append(b_1)
TableauOrd.append(c_1)
TableauOrd.append(d_1)
TableauOrd.append(e_1)
TableauOrd.append(f_1)
TableauOrd.remove(11)  # Faite pas partie du Tableau finale

# _____________________#
# Joueur section
# _____________________#

# Les numéros
a_2 = random.randint(1, 9)
b_2 = random.randint(1, 9)
c_2 = random.randint(1, 9)
d_2 = random.randint(1, 9)
e_2 = random.randint(1, 9)
f_2 = random.randint(1, 9)

TableauJou = [11]  # Pour éviter la condition de Gagné
TableauJou.append(a_2)
TableauJou.append(b_2)
TableauJou.append(c_2)
TableauJou.append(d_2)
TableauJou.append(e_2)
TableauJou.append(f_2)
TableauJou.remove(11)  # Faite pas partie du Tableau finale

# _____________________#
# Interlocuteur section
# _____________________#
a_3 = 0  # Égal a zero pour maintenent. Pour éviter d'enlever un numéro d'un joueur immédiatement
TableauModele = []  # Le premier qui a une tableau qui a rien ou egal au TableauModele, gagne!


# _____________________#
# Les points
# _____________________#

def cliqueCalculer1():
    a_3 = random.randint(1, 9)  # Choisir une nouvelle chiffre
    lblReponse1['text'] = "Le prochain numéro est: {}".format(a_3)  # Montrez le chiffre

    # Si a_3 est égale a une des numéros du joueur ou ordinateur, il va l'enlever de leur Tableau complètement
    while a_3 in TableauOrd:
        TableauOrd.remove(a_3)
    lblReponse2['text'] = "{}".format(TableauOrd)

    while a_3 in TableauJou:
        TableauJou.remove(a_3)
        lblReponse3['text'] = "{}".format(TableauJou)

    # Message qui dit qui gagne:
    if len(TableauJou) + len(TableauOrd) == 0:  # Si il reste rien, les deux joueurs ont fini en même temps
            lblReponse4['text'] = "C'est une égaliter"
            lblMessage4['text'] = "Il n'y a pas de difference"

    elif TableauModele == TableauOrd:  # Si l'ordinateur gagne
        JT = len(TableauJou)  # Prendre en note le montent de numéros qui reste du joueur
        lblMessage4['text'] = 'Par: {} numéros'.format(JT)
        lblReponse4['text'] = "L'ordinateur a gagner"

    elif TableauModele == TableauJou:  # Si le joueur gagne
        CT = len(TableauOrd)  # Prendre en note le montent de numéros qui reste de l'ordinateur
        lblMessage4['text'] = 'Par: {} numéros'.format(CT)
        lblReponse4['text'] = "Tu as gagnés"

# -------------------------------------------------------------_#
# --------------------------------------------------------------#
# Le Fenetre
# --------------------------------------------------------------#
# -------------------------------------------------------------_#

# Fenetre
fenetre = tk.Tk()
fenetre.title("Binga")
fenetre["bg"] = "#046fb3"
fenetre.geometry("600x600")

# Titre 1
lblTitre = tk.Label(fenetre)
lblTitre['text'] = "Bienvenue au BINGA!"
lblTitre['font'] = "Arial 24"
lblTitre['bg'] = '#6ec7ff'
lblTitre["wraplength"] = 375
lblTitre.pack()

# Message1
lblmessage1 = tk.Label(fenetre)
lblmessage1['text'] = "Est-ce que tu est chanceuse?!"
lblmessage1['font'] = "Arial 10"
lblmessage1['bg'] = '#997af5'
lblmessage1.pack()

# Seperateur
lblSeperator1 = tk.Label(fenetre)
lblSeperator1["text"] = "-------------------------------------------------------------------"
lblSeperator1["bg"] = "#046fb3"
lblSeperator1.pack()

# --------------------------------------------------------------#
# Interlocuteur
# --------------------------------------------------------------#
# Titre2
lblInt = tk.Label(fenetre)
lblInt[
    'text'] = "L'interlocuteur"  # Le nom du personne qui crie les numeros est appeler l'interlocuteur dans Bingo
lblInt['font'] = "italic 15"
lblInt['bg'] = '#000000'
lblInt['fg'] = '#eeff03'
lblInt.pack()

# Reponse de l'inter
lblReponse1 = tk.Label(fenetre)
lblReponse1["text"] = "".format(a_3)
lblReponse1["font"] = "Arial 15"
lblReponse1['bg'] = '#FFFFFF'
lblReponse1.pack()

# Seperateur
lblSeperator1 = tk.Label(fenetre)
lblSeperator1["text"] = "-------------------------------------------------------------------"
lblSeperator1["bg"] = "#046fb3"
lblSeperator1.pack()

# --------------------------------------------------------------#
# Ordinateur
# --------------------------------------------------------------#

# Titre3
lblOrd = tk.Label(fenetre)
lblOrd['text'] = "L'ordinateur"
lblOrd['font'] = "italic 15"
lblOrd['bg'] = '#000000'
lblOrd['fg'] = '#bd1e2e'
lblOrd.pack()

# Message2
lblmessage2 = tk.Label(fenetre)
lblmessage2['text'] = "Les numéros de L'ordinateur"
lblmessage2['font'] = "Arial 10"
lblmessage2['bg'] = '#bd1e2e'
lblmessage2.pack()

# Reponse de l'ordinateur
lblReponse2 = tk.Label(fenetre)
lblReponse2["text"] = "{}".format(TableauOrd)
lblReponse2["font"] = "Arial 11"
lblReponse2['bg'] = '#FFFFFF'
lblReponse2.pack()

# Seperateur
lblSeperator2 = tk.Label(fenetre)
lblSeperator2["text"] = "-------------------------------------------------------------------"
lblSeperator2["bg"] = "#046fb3"
lblSeperator2.pack()

# --------------------------------------------------------------#
# Joueur
# --------------------------------------------------------------#
# Titre4
lblJou = tk.Label(fenetre)
lblJou['text'] = "Joueur"
lblJou['font'] = "italic 15"
lblJou["bg"] = "#000000"
lblJou['fg'] = '#35945d'
lblJou.pack()

# Message3
lblmessage3 = tk.Label(fenetre)
lblmessage3['text'] = "Les numéros du Joueur"
lblmessage3['font'] = "Arial 10"
lblmessage3['bg'] = '#35945d'
lblmessage3.pack()

# Reponse du Joueur
lblReponse3 = tk.Label(fenetre)
lblReponse3["text"] = "{}".format(TableauJou)
lblReponse3["font"] = "Arial 11"
lblReponse3['bg'] = '#FFFFFF'
lblReponse3.pack()

# Seperateur
lblSeperator3 = tk.Label(fenetre)
lblSeperator3["text"] = "-------------------------------------------------------------------"
lblSeperator3["bg"] = "#046fb3"
lblSeperator3.pack()

# Bouton de Calculation1
btnCalculer1 = tk.Button(fenetre)
btnCalculer1["text"] = " Numéro Générateur"
btnCalculer1["font"] = "Arial 11"
btnCalculer1["command"] = cliqueCalculer1
btnCalculer1.pack()

# Reponse de qui gagne
lblReponse4 = tk.Label(fenetre)
lblReponse4["text"] = " "
lblReponse4["font"] = "Arial 10"
lblReponse4['bg'] = '#FFFFFF'
lblReponse4.pack()

# Reponse de difference
lblMessage4 = tk.Label(fenetre)
lblMessage4["text"] = " "
lblMessage4["font"] = "Arial 10"
lblMessage4['bg'] = '#FFFFFF'
lblMessage4.pack()

# Seperateur
lblSeperator4 = tk.Label(fenetre)
lblSeperator4["text"] = "-------------------------------------------------------------------"
lblSeperator4["bg"] = "#046fb3"
lblSeperator4.pack()
# --------------------------------------------------------------#
# Regles
# --------------------------------------------------------------#
#Regle1
lblRegle1 = tk.Label(fenetre)
lblRegle1["text"] = "Chaque joueur aura des numéros donné qui sont au hasard!"
lblRegle1["bg"] = "#ffc800"
lblRegle1.pack()

#Regle2
lblRegle2 = tk.Label(fenetre)
lblRegle2["text"] = "Pour Gagné tu aura besoin avoir tous tes numéro dite par l’interlocuteur!"
lblRegle2["bg"] = "#ffc800"
lblRegle2.pack()

#Regle3
lblRegle3 = tk.Label(fenetre)
lblRegle3["text"] = "Pour être donné un numéro pèse sur le générateur!"
lblRegle3["bg"] = "#ffc800"
lblRegle3.pack()

fenetre.mainloop()
