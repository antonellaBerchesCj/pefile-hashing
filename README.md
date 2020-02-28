# pefile-hashing

Details:
   -  First off it loads kernel32.dll and searches for the export directory and in it it finds the number of names, address of functions (addresses to exported functions).
   - The program has stored some hashed (names of) functions.
   - The hash consists of a rol and a xor
   - For every hash in memory it goes through the names of exported functions of kernel32.dll and hashes their names and compares the hash with the one stored in memory
   - The program replaces the hashes from memory with the addresses of the coresponding exported functions.
   - The functions it searches for are:
    ExitProcess
    WinExec
    CreateProcessA
    GetModuleHandleA
    VirtualFreeEx
    VirtualAllocEx
    lstrcatA
    WriteProcessMemory
    CloseHandle
    GetShortPathNameA
    GetModuleFileNameA
    GetEnvironmentVariableA
    LoadLibraryA_02
    GetProcAddress
    ResumeThread
    GetThreadContext
    
  - Creates a new process in suspended mode
    Inserts in the new process code which downloads from http://user.free2.77169.net/meimeileyuan/2.exe the executable using URLDownloadToFileA from urlmon and saves it as c:\\1.exe
  - Runs 1.exe
  - Uses cmd to delete itself
