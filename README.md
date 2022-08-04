# Study-Pal-Application
Developed an mobile application in Python in which students can meet up on a common forum and prepare for exams with other students that are studying the same subject.


import kivy
from kivy.app import App
from kivy.uix.gridlayout import GridLayout 
from kivy.uix.label import Label
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button


class StudyBuddyApp(GridLayout):
  def __init__(self,**kwargs):
    super(StudyBuddyApp,self).__init__()
    self.cols = 4
    

    self.add_widget(Label(text= "School"))
    self.sc_name = TextInput
    self.add_widget(self.sc_name)
    
    self.add_widget(Label(text= "Student Name"))
    self.s_name = TextInput
    self.add_widget(self.s_name)

    self.add_widget(Label(text= "Course Name"))
    self.c_name = TextInput
    self.add_widget(self.c_name)

    self.add_widget(Label(text= "Professor"))
    self.p_name_name = TextInput
    self.add_widget(self.p_name)

    self.press = Button(text = "Lets find your Pal!")
    self.press.bind(on_press = self.click_me)
    self.add_widget(self.press)
