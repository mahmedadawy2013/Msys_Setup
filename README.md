# Msys_Setup
Installation for unix environment on windows 
QuestaSim simulator must be installed on Windows<br/>
* Install Anaconda<br/>
   * Download Anaconda from the official website and install it on windows: [Anaconda.com/download](https://www.anaconda.com/download/).<br/>

* Install MSYS2<br/>
   * Download MSYS2 from the following website and install it on windows: [MSYS2.org](https://www.msys2.org/).<br/>

* Install TCL<br/>
   * Download TCL from the following Link and install it on windows: [TCL Download Link](https://www.mediafire.com/file/f8mz3hx4fh6lnba/ActiveTcl-8.6.13.0000-MSWin32-x64-559160e0.rar/file).<br/>

* After MSYS2 Setup<br/>
   * Open the MSYS2 terminal and execute the following commands:<br/>
     * `pacman -S mingw-w64-ucrt-x86_64-gcc`<br/>
     * `pacman -Suy` (the terminal will close after this command)<br/>
     *  Re-open the MSYS2 terminal and execute the following commands.<br/>
     * `pacman -Su`<br/>
     * `pacman -S git make`<br/>
     * Close the terminal.<br/>

* Configure Anaconda<br/>
   * Open the Anaconda terminal as an **administrator**(opening as administrator is a must).<br/>
   * Don't forget to choose anaconda as **default** python interpeter(this step is a must)<br/>
   * Open the Anaconda terminal then run the following commands:<br/>
     * `conda install -c msys2 m2-base m2-make`<br/>
     * `pip install cocotb`<br/>
     * `pip install pyuvm`<br/>
     * `pip install tabulate`<br/>

* Modify MSYS2 Bash configuration<br/>
   * Open the MSYS2 Bash configuration file located at `msys2/home/yourname/.bashrc` and edit it.<br/>
   * Paths must not include any space for example:
     * `export PATH=Program Data/questasim64_10.7c/win64:$PATH-----> will not work`<br/>
     * `export PATH=ProgramData/questasim64_10.7c/win64:$PATH-----> will work`<br/>
   * Add the following lines to the file:<br/>
     * `export PATH=yourpath/questasim64_10.7c/win64:$PATH`<br/>
     * `export PATH=yourpath/anaconda3:$PATH`<br/>
     * `export PATH=yourpath/anaconda3/Scripts:$PATH`<br/>

* Open control panel then edit your enviromental variables and add the following paths<br/>
   * yourpath/msys2/usr/bin
   * yourpath/questasim/win64
   * yourpath/anaconda3
   * yourpath/anaconda3/Scripts

* Open PowerShell as an administrator.<br/>
   * Run the command: `set-executionpolicy remotesigned`<br/>
   * Run the command: `conda init`<br/>
   * Close PowerShell.<br/>


https://github.com/user-attachments/assets/73fe46ac-3660-430e-b3c1-2db753f1001b

