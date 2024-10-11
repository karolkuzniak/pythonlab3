# pythonlab3
tkinter
Z1 – tkinter 
Popraw kod z Dodatku 1 tak, aby interfejs programu był jak najbardziej zbliżony do tego pokazanego na rysunkach poniżej. Z listy można wybrać język programowania: Python, Kotlin, JavaScript. Okno zawiera tytuł Ciekawa aplikacja okienkowa. 
Poprawny wynik działania powinien być następujący: 
  
 
 
 
  
 
  
 
Dodatek 1 – tkinter 
# -*- coding: utf-8 -*- 
 
# modfied by Jakub example from 
https://www.tutorialspoint.com/python/tk_menu.htm 
 
import tkinter 
  def donothing(): 
    filewin = tkinter.Toplevel(window) 
    button = tkinter.Button(filewin, text="Kliknij mnie")     button.pack() 
  window = tkinter.Tk() 
 
  
menubar = tkinter.Menu(window) filemenu = tkinter.Menu(menubar, tearoff=0) filemenu.add_command(label="Nowy", command=donothing) filemenu.add_command(label="Otwórz", command=donothing) filemenu.add_command(label="Zapisz", command=donothing) filemenu.add_command(label="Zapisz jako ...", command=donothing) filemenu.add_command(label="Zamknij", command=donothing) 
 
filemenu.add_separator() 
 
filemenu.add_command(label="Wyjście", command=window.quit) menubar.add_cascade(label="Plik", menu=filemenu) editmenu = tkinter.Menu(menubar, tearoff=0) 
editmenu.add_command(label="Cofnij", command=donothing) 
 
editmenu.add_separator() 
 editmenu.add_command(label="Wytnij", command=donothing) editmenu.add_command(label="Kopiuj", command=donothing) editmenu.add_command(label="Wklej", command=donothing) editmenu.add_command(label="Usuń", command=donothing) 
editmenu.add_command(label="Zaznacz wszystko", command=donothing) 
 menubar.add_cascade(label="Edycja", menu=editmenu) helpmenu = tkinter.Menu(menubar, tearoff=0) helpmenu.add_command(label="Indeks", command=donothing) helpmenu.add_command(label="O programie", command=donothing) menubar.add_cascade(label="Pomoc", menu=helpmenu) 
 
window.config(menu=menubar) 
  
window.mainloop() 
