
# Installing Python

We went to the Python page for the initial download: (https://www.python.org/downloads/)
After selecting the most recent version (3.9.2) for Mac OSX, I downloaded it to my computer.

Then, we found a beginning tutorial for getting Python set up on VS Code (https://code.visualstudio.com/docs/python/python-tutorial). This involved:

Installing Python using Homebrew by opening the Mac Terminal and typing: 

  `brew install python3`
  
Once installation was complete, we verified by typing: 

  `python3 --version`

this returned the most recent version 3.9.2

Then we started a VS Code project: 

  ```mkdir hello
  cd hello
  code .```

Inside the project we selected a Python interpreter by opening the Command Pallette and typing: Python: Select Interpreter. Then we created a folder titled "hello" with a file titled "hello.py" and then in the file we entered the following code: 

  ```msg = "Hello World"
  print(msg)```

To run the msg we cliked the Run Python File in Terminal play button which is a green arrow located in the top right hand corner of the code editor, next to the button that allows the user to split the screen. This runs the msg in the integrated terminal (print is synonomous with console.log in Python).

Following the successful run of the Hello World message, the tutorial then directed us to use the debugger, by placing the cursor on "print" and selecting F9, or using the mouse to left click on the dot next to the line number, setting up a break point. Then pressing F5 initializes the debugger (the same can be done by going to the VS Code toolbar at the top of the screen and selecting the "Run" menu and then selecting "Start Debugger". To initialize the debugger, you need to select Python File when VS Code prompts you to select a debug configuration. A debugging toolbar appears at the top of the screen to facilitate in the debugging process.

We also explored working with variables in the Debug Console in the integrated terminal:

  ```msg
  msg.capitalize()
  msg.split()```

The final portion of the tutorial involves installing and using packages. We're prompted to open a new file called "standardplot.py" and pasting in the following code:

  ```import matplotlib.pyplot as plt
  import numpy as np

  x = np.linspace(0, 20, 100)  # Create a list of evenly-spaced numbers over the range
  plt.plot(x, np.sin(x))       # Plot the sine of each x point
  plt.show()                   # Display the plot```

Running this code through the debugger results in a message: "ModuleNotFoundError: No module named 'matplotlib'" because we have not previously installed the matplotlib package. The tutorial then directs you to set up a project-specific virtual environment in the terminal and then install the package with the following lines of code in the terminal:

  ```python3 -m venv .venv
  source .venv/bin/activate```

Then:

  `python3 -m pip install matplotlib`

Finally, rerunning the program results in a pop up waveline graph.

After this we found https://www.w3schools.com/python/ a helpful starting point for a quick overview of Python fundamentals. If we had more time we would have worked through some modules at https://www.codecademy.com/courses/learn-python-3/