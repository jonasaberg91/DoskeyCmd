#Doskey
Ever find yourself limited on a Windows platform development environment? With Doskey's you can get closer to the Unix terminal you love, simply bind your macros using Doskey's and start coding!
##Installation
####Setting things up
1. [Download .bat file](https://github.com/jonasaberg91/DoskeyCmd/archive/master.zip)
2. Create a folder on your disk (Folder location is optional) Example: *C:\Windows\bin* and place .bat file in the folder

####Enable your Doskey's every time you start your Command Prompt
1. Open Regedit
2. Create a new String value in *HKEY_CURRENT_USER\SOFTWARE\Microsoft\Command Processor*, with Value Name: AutoRun and Value Data is must be the complete PATH of your .bat file. Example: *C:\Windows\bin\doskeys.bat*

##Syntax Guide
Here's an overview of syntax included in the .bat file you can use

**Display Doskey history**

```
	F7,
	Alt + F7,
	or type doskey /history
```

**Linux commands**

```
doskey alias   = doskey $*
doskey cat     = type $*
doskey clear   = cls
doskey cp      = copy $*
doskey cpr     = xcopy $*
doskey grep    = find $*
doskey history = doskey /history
doskey kill    = taskkill /PID $*
doskey ls      = dir $*
doskey mv      = move $*
doskey ps      = tasklist $*
doskey pwd     = cd
doskey rm      = del $*
doskey rmr     = deltree $*
doskey sudo    = runas /user:administrator $*
```

**Simplified navigation**

```
doskey ..    = cd ..\$*
doskey ...   = cd ..\..\$*
doskey ....  = cd ..\..\..\$*
doskey ..... = cd ..\..\..\..\$*
```

**Bind your own applications**

Example:
```
doskey subl="C:\Program Files\Sublime Text 3\sublime_text.exe" $*
```

Adding your own applications
```
doskey nameofyourlink="PATH" $*
```

##Additional information

[Doskey - Microsoft Technet](https://technet.microsoft.com/en-us/library/bb490894.aspx)