#REPL.IT
#https://repl.it/join/vnxndavf-azanir

import PySimpleGUI as sg
import time
# Задание 3:
#     Заведите 3 списка: today, tomorrow, other (вы можете назвать переменные по-другому).
#     Измените блок кода, который выполняет команду add:
#     Дополнительно запросите у пользователя дату выполнения задачи.
#     В зависимости от введенной даты добавьте задачу в один из списков по следующим правилам:
#         Если пользователь ввел "Сегодня", добавьте задачу в список today.
#         Если пользователь ввел "Завтра", добавьте задачу в список tomorrow.
#         Если пользователь ввел любое другое значение, добавьте задачу в список other.


#список команд для юзера
HELP = '''Справка по командам:
help - вывести список команд
add - добавить задачу
print - вывести все задачи
exit - завершить программу
'''
#списки задач
today = []
tomorrow = []
other = []

#флаг выхода из бесконечного while
stop = False

# Define the window's contents
layout = [  [sg.Text("Введите команду")],     
            [sg.Input()],
            [sg.Output(size=(43, 10))],
            [sg.Submit(), sg.Cancel()]
]

# Create the window
window = sg.Window('Homework 2', layout,)  

def add_task():
  print('Введите задачу: ')
  event, values = window.read()
  task = values[0]
  print('<------------------>')
  sg.Popup('Задача добавлена')
  return(task)

while True:  
  event, values = window.read()

  if event in (None, 'Exit', 'Cancel'):
    print('Спасибо за использование! До свидания!')
    break        
  #print(event, values) #debug
  elif values[0].lower() == 'exit':
    print('Спасибо за использование! До свидания!')
    break
  #вывод помощи
  elif values[0].lower() == 'help':
    print(HELP)
  #lj,fdktybt задачи
  elif values[0] == 'add':
    while True:
      print('Введите дату: ')
      event, values = window.read()
      dat = values[0].lower()
      if dat == 'сегодня':
        today.append(add_task())
        break
      elif dat == 'завтра':
        tomorrow.append(add_task())
        break
      else:
        other.append(add_task())
        break

  #вывод справки print
  elif values[0].lower() == 'print':
    print('Сегодня')
    for i in today:
      print(i)
    
    print('Завтра')
    for i in tomorrow:
      print(i)
    
    print('Когда-то')
    for i in other:
      print(i)
  
  else:
    print('Неизвестная команда. Введите help, чтобы увидеть список команд')
# Finish up by removing from the screen
time.sleep(1)
window.close()
