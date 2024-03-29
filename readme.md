# This script creates a line-to-line aligned tmx file

It accepts either two sentence-segmented txt files, with one sentence per line in
each file, or one txt file with two tab-delimited elements per line. 
Based on that, the script creates a tmx file in the same location as the original file(s).

In case of a single tab-delimited file it must have the following format: 
'Original-text Tab-char Translation' per each line.

You must also pass as the first argument the desired language codes as follows:
-c en-US#ar-SA; -c EN#RU, etc.

The default language codes are en-US and ru-RU

## How to install on Windows (no admin rights required)

Step 1. Get Python 3 from Microsoft Store

Step 2. Get PowerShell from Microsoft Store

Step 3. Create a new folder in your file system on Windows

Step 4. Right-click on that folder and select Open in Terminal

Step 5. Write the following in the command line of the open Terminal window:
```
> python3 -m venv .venv
> .\.venv\Scripts\Activate.ps1
> python3 -m pip install txt2tmx
```

## How to use

If you've just finished the installation, type in in the command line (for
a single source file):
```
> python3 -m txt2tmx -c en#ar C:\full-path\your-file.txt
```

Or, in case of two source files:
```
> python3 -m txt2tmx -c en#ar C:\full-path\file_1.txt C:\full-path\file_2.txt 
```

If you already closed PowerShell, use Windows Explorer to find the folder that you created in Step 3 (or simply repeat Steps 3 to 5 if you can't find it). Open that folder in PowerShell Terminal. Then type in the following commands in the PowerShell window:
```
> .\.venv\Scripts\Activate.ps1
> python3 -m txt2tmx -c en#ar C:\full-path\your-file.txt
```