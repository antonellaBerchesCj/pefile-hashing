# pefile-hashing
Python

Details:
- get kernel32.dll and user32.dll export functions and hash them (used rol + xor)
- using COMSPEC take cmd control and delete the exe file  (/c del "file.exe.new") !showWindow mode
- using WriteProcessMemory function to write multiple bytes into the process. The written buffer contains the method URLDownloadToFile which download data from an infected link and put them into the file  c:\\1.exe
