# Easy CLI in one python file!
Installation:
-----------
download file cli.py and paste it to your project, in main file write 
```
from cli import CLI
console = CLI('~: ','Goodbye see you next time :)')
```
here '~:' is a start of each line
and  'Goodbye see you next time :)' is the goodbye message, sends when console is closing

Usage:
-----------
function addCommand(name, description, argsAmount, functionToExecute) - add new command to your CLI

function mainLoop() - start your CLI

command 'help' - is builtin and contains all added commands

command 'exit' - is builtin and stops your CLI but not all programm

Examples:
-----------
main.py
```
from cli import CLI
console = CLI('~: ','Goodbye see you next time)')

def test(arg1,arg2):
    print(f'test {arg1},{arg2}')

console.addCommand('test','just test',2, func=test)
console.mainLoop()
```
in work
```
PS C:\Users\Possiug\Desktop\Projects\Programs\Python\CLI> python main.py
~: help
------------------------CLI-----------------------
                  Made by Possiug!
--------------------------------------------------
        help - args amount: 0 - show all commands
        test - args amount: 2 - just test
~: test
incorrect args amount!
~: test 1 2
test 1,2
~:
```
