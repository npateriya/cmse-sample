
# CMSE Sample Code Generation Prep Guide in CodeExchnage IDE

When using the Cisco Metrics Search Engine (CMSE) the code generation feature may be used with VS Code or another IDE.  CMSE provides sample code that leverages common and value-added Python libraries to reduce overall code complexity.  The following steps will help you set up a Python environment for use with CMSE.

1) Prepare a Python 3.10 or higher environment
If you have no Python environment or need assistance, the following documentation is helpful:
* https://wiki.python.org/moin/BeginnersGuide
* https://wiki.python.org/moin/BeginnersGuide/Download

2) A virtual environment (venv) is highly suggested to keep separation of this project environment from the python libraries of your core operating system

```
$ mkdir CMSE
$ cd CMSE
$ python3 -m venv .venv
$ source .venv/bin/activate
(.venv) CMSE $
```

3) pip install the common libraries CMSE uses.
Note: These may change over time, so view the python code 'import' statements to ensure your virtual environment has them installed.  Check with 'pip list'

```
(.venv) CMSE $ pip install meraki requests ncclient lxml pysnmp netmiko
```

4) Use VS Code and open your project directory to the CMSE folder created above, whether local to your computer or remote to another system.

5) Use the menu options View > Command Palette, then 'Python: Command Interpreter' to navigate to the virtual environment instance of python3, usually in your CMSE directory, then .venv/bin/python, which may already be the recommended option.

6) (Optional) Save the workspace with menu option File > Save Workspace As...
then give it a name like CMSE

You are now prepared for the CMSE code generator function.
After doing a CMSE search and selecting a desired metric, click the 'Show code snippets' gadget when provided.

Use the copy icon to inject the Python code to your PC clipboard.
Return to the VS Code utility and create a new file with menu option File > New Text File (or CTRL-N), then paste the Python code from the clipboard with menu option Edit > Paste (or CTRL-V).
Update the Python script with your preferred device management hostname/IP and credentials, or use the DevNet Sandbox Always-On devices referenced at
https://devnetsandbox.cisco.com/RM/Topology (change Type filter to Always-On)
