# Batch file – Programming

<br>

# Index
<details>
<summary>Open Navigation</summary>
<ul>
    <li><a href="#HELP">HELP</a></li>
    <li><a href="#comment">Comment</a></li>
    <li><a href="#ATTRIB">ATTRIB</a></li>
    <li><a href="#CD">CD</a></li>
    <li><a href="#CHOICE">CHOICE</a></li>
    <li><a href="#CLS">CLS</a></li>
    <li><a href="#CMD">CMD</a></li>
    <li><a href="#COPY">COPY</a></li>
    <li><a href="#DATE">DATE</a></li>
    <li><a href="#DEL">DEL</a></li>
    <li><a href="#EXIT">EXIT</a></li>
    <li><a href="#FIND">FIND</a></li>
    <li><a href="#MD">MD</a></li>
    <li><a href="#MORE">MORE</a></li>
    <li><a href="#MOVE">MOVE</a></li>
    <li><a href="#RD">RD</a></li>
    <li><a href="#REN">REN</a></li>
    <li><a href="#SET">SET</a></li>
    <li><a href="#START">START</a></li>
    <li><a href="#SHUTDOWN">SHUTDOWN</a></li>
    <li><a href="#TASKLIST">TASKLIST</a></li>
    <li><a href="#TASKKILL">TASKKILL</a></li>
    <li><a href="#SYSTEMINFO">SYSTEMINFO</a></li>
    <li><a href="#TITLE">TITLE</a></li>
    <li><a href="#variables">variables</a></li>
    <li><a href="#Arithmetic-Operators">Arithmetic Operators</a></li>
    <li><a href="#Relational-Operators">Relational Operators</a></li>
    <li><a href="#Logical-shift-and-re-directional-Operators">Logical shift and re directional Operators</a></li>
    <li><a href="#Assignment-Operators">Assignment Operators</a></li>
    <li><a href="#Conditional-Operator">Conditional Operator</a></li>
    <li><a href="#if-else-statement">if else statement</a></li>
    <li><a href="#Loop">Loop</a></li>
    <li><a href="#return-code">return code</a></li>
    <li><a href="#Error-Level">Error Level</a></li>
    <li><a href="#Functions">Functions</a></li>
    <li><a href="#Mini-Projects">Mini Projects</a></li>
</ul>
</details>

<br>

**Extensions:**  `.bat` or `.cmd`

**Create batch file :** Open a text file and save it as `.bat`

**How to run file?** just click on that damm file >_<

## Starting Format
```
@echo OFF

PAUSE
```
or
```
@echo off

pause
```
Dosent matter whatever way use. Because these are reserve keywords. What are reserve keywords? [Here More Info](https://en.wikipedia.org/wiki/Reserved_word)

***Note:*** DOS or Batch commands are not case sensitive

Now, If we don’t put `@echo off` at the top of the script, it will produce an output where ‘echo’ itself will also be displayed. *Test yourself*

`Pause` is used to hold the screen until we press a key. If pause is not used, the output screen will vanish away within a blink of an eye and we won’t be able to see the output.

## HELP
This will display all the available commands with their functionalities in the console.
```batch
@echo OFF
HELP
PAUSE
```

To know about specific cmd, just type `help` and the `command` you want to know about.
```batch
@echo OFF
HELP copy
PAUSE
```

## Comment
`::` or `REM`

```
:: This line is commented
```
or
```
REM This line also
```

## ATTRIB
Used to display the file attributes or set an attribute to a file in the working directory.

```batch
@echo OFF
:: To display attribute of note.txt
ATTRIB note.txt

:: To make it read only by adding 'r'
ATTRIB +r note.txt
ATTRIB note.txt

:: To make it hidden by adding 'ah'
ATTRIB +ah note.txt
ATTRIB note.txt

:: To remove attribute read only
ATTRIB -r note.txt
ATTRIB note.txt
```
Output
```
A        note.txt
A  R     note.txt
A  R  AH note.txt
A     AH note.txt
```
Here in this output, A means Archived, R means Read only and AH means Hidden file.

## CD
Helps in navigating through different directories and changing directories or displaying current directory.

```batch
@echo OFF
:: CD without any parameters displays the current working directory
CD
:: Changing to the parent directory one level up.
CD..
CD
:: Changing the path to Programs
CD\Programs
CD
PAUSE
```
Output
```
C:\Users\abc
C:\Users
C:\Programs
```

## CHOICE
Provides a list of options to the user.
```batch
@echo OFF
ECHO Its raining?
ECHO Enter Y for yes
ECHO Enter N for no
CHOICE /c YN /m "Yes or No"
```
Output
```
You want coffee?
Enter Y for yes
Enter N for no
Yes or No [Y,N]?
```
Now the console waits for your input and once you enter your answer it will terminate.

## CLS
The batch cmd clears the screen.
```batch
@echo OFF
CLS
PAUSE
```

## CMD
The batch command `CMD` invokes/creates a new command prompt window.

## COPY
Used for copying files from one location to another.
```
@echo OFF
:: For copying from one drive to another -xyz.txt from C:\ to D:\
COPY C:\xyz.txt D:\

:: If file has whitepace between name - use double quote
COPY "C:\my file.txt" D:\

PAUSE
```

## DATE
`DATE` displays the current date in the system.

## DEL
Used for deleting files.

*Note:* `DEL` command only deletes files, not directories.

```batch
@echo OFF
:: To delete a single file xyz.txt
DEL C:\xyz.txt

:: To delete all the files of .txt extensions and ask for confirmation before deleting
DEL /p/s C:\*.txt

:: Remove \p to delete without confirmation
DEL /s C:\*.txt
```

## EXIT
Terminates and exits the console.
```batch
@echo OFF
echo "Did you see anything?"
EXIT
```

## FIND
The batch command search the given file to find the desired string and if located, it displays the corresponding line in which the string exists.
```batch
@echo OFF
FIND "find me" example.txt
PAUSE
```
This script will search for the string “find me” in example.txt file and if it exists in example.txt, it will display the corresponding line on the console.

## MD
Creates a new directory or folder in the working directory.
```batch
@echo OFF
MD abc
```

## MORE
Displays the content of a file one by one.
```batch
@echo OFF
MORE C:\example.txt
```
This will display the contents of example.txt line by line, one at a time.

## MOVE
Moves files from one directory to another, rename the directories and move the directories as well.

```batch
@echo OFF
:: To move xyz.txt from dir1 to dir2
MOVE C:\dir1\xyz.txt C:\dir2

:: To rename directory dir1 to dir2
MOVE C:\Program\dir1 C:\Program\dir2

:: To move directory dir1 from D:\ to D:\music
MOVE D:\dir1 D:\music\
```

## RD
used for removing the empty directories, directories with contents or files inside cannot be removed with RD command.

```batch
@echo OFF
:: To remove directory xyz from C:\>
RD C:\xyz

:: To remove multiple directories from working location
RD dir1 dir2
```

## REN
Used for renaming files and directories.
```batch
@echo OFF
:: To rename x.php to y.php
REN C:\x.php C:\y.php
```

## SET
Displays the list of environment variables of the system. It also used when create variable.

## SHUTDOWN
Shuts down the computer.

## START
Used to open a file or start a new program.
```batch
@echo OFF
START paint.exe
```

## TASKKILL
Used to terminate a running task. If you were to terminate the notepad running in your PC, then following script is used.
```batch
@echo OFF
TASKKILL /im notepad.exe
```

## TASKLIST
Lists all the running tasks in the console.
```batch
@echo OFF
TASKLIST
```

## SYSTEMINFO
Displays all the configuration of the computer and operating system.
```batch
@echo OFF
SYSTEMINFO
```

## TITLE
Sets new title for output console.
```batch
@echo OFF
TITLE "New Titl >.<"
```

## variables
Here is how the batch variables are declared.
```batch
SET varibale_name=variable_value

:: for assigning numeric value
SET /A variable_name=nameric_value
```
***Note:*** Variable name not case sensitive as DOS or Batch commands are not case sensitive & `/A` is used for assigning numeric values. Uninitialized variables are empty strings in batch files.

> How to verify if batch variables are defined already by system or you already defined but forgot?

```batch
IF DEFINED MyVar (ECHO MyVar IS defined) ELSE (ECHO MyVar is NOT defined)
```

### Print Variable

```batch
@echo OFF
SET name=Apple
ECHO %name%

:: For numberic variable
SET a=2
ECHO %a%
PAUSE
```
> Using whitespace between variable and value. `SET name=Apple` will work but `SET name = Apple` will not.

### Global variables and Local variables

```batch
@echo oFF
SET var1=var1 is global variable
SETLOCAL
SET var2=var2 is a local variable

ECHO %var1%
ECHO %var2%
ENDLOCAL
PAUSE
```
Output
```
var1 is global variable
var2 is a local variable
Press any key to continue . . .
```
Now let’s see what happens when we try to use a local variable beyond its scope i.e using after `ENDLOCAL`

```batch
@echo oFF
SET var1=var1 is global variable
SETLOCAL
SET var2=var2 is a local variable

ECHO %var1%
ENDLOCAL
ECHO %var2%
PAUSE
```
Output
```
var1 is global variable
ECHO is off.
Press any key to continue . . .
```
When we try to use local variable beyond its scope, instead of executing commands with the local variable, the ECHO is turned off.

## Arithmetic Operators
| Operators | Description | Example |
| --------- | ----------- | ------- |
| + | Addition operator | Set /A 5+5 = 10 |
| - | Subtraction operator | Set /A 10-5 = 5 |
| % | Modulus operator | Set /A 5%2 = 1|
| /	| Division operator	| Set /A 20/2=10|
| * | Multiplication operator |	Set /A 2*2 = 4|

```batch
@echo off
SET /A a = 2
SET /A b = 4
Set /A s = %a% + %b%
echo Sum = %s%
pause
```
Output
```
Sum = 6
```
### Precedence of Arithmetic operators
The precedence of arithmetic operators are in the following order:
```
/  *  %  +  -
```
```batch
@echo off
Set /A s = (20 - 5) * 2 + 8 / 2
echo s = %s%
pause
```
Output
```
s = 34
```
**Explanation:**

The expression enclosed inside ( ) gets the highest priority in the precedence.

In the above example, (20 - 5) gets the highest priority and calculated first giving 15.

Then division operator / gets next priority thus 8 / 2 is evaluated giving 4.

After this multiplication operator * gets next priority thus 15 * 2 yields 30.

Finally, addition operator + performs addition operation 30 + 4 giving final result 34.

## Relational Operators

|Operators|	Description|	Example|
|---|---|---|
|EQU|	equal to|	x EQU y = Return true if x is equal to y|
|NEQ|	not equal to|	x NEQ y = Returns true if x is not equal to y |
|LSS|	less than|	x LSS y = Returns true if x is less than y|
|LEQ|	less than or equal to|	x LEQ y = Returns true if x is less than or equal to y|
|GTR|	greater than|	x GTR y = Returns true if x is greater than y|
|GEQ|	greater than or equal to|	x GEQ y = Returns true if x is greater than or equal to y|

```batch
@echo off
SET /A x = 3
SET /A y = 4
if %x% EQU %y% echo x is equal to y
if %x% NEQ %y% echo x is not equal to y
if %x% LSS %y% echo x is less than y
if %x% LEQ %y% echo x is less than or equal to y
if %x% GTR %y% echo x is greater than y
if %x% GEQ %y% echo x is greater than or equal to y
pause
```

## Logical shift and re directional Operators
Redirection operator is used to redirecting the output of one command to the other file.
|Operators|	Description|	Example|
|-|-|-|
|>>|	Logical shift operator|	command > filename <br> Append the output to a file|
|>	|Re directional operator|	command > filename <br> Redirect the output to a file|
|<|	Re directional operator|	command < filename <br> Redirect text to command|

> Example 1
```batch
@echo off
echo Testing of redirection operator > test.txt
```
The above command will redirect the output of echo command 'Testing of redirection operator' to a text file named test.txt.

If there is no text file named test it will create a new one.

> Example 2
A file named Num.txt which contains numbers in random order as follow:
```
4
3
7
1
8
```

```batch
@echo off
SORT < Num.txt
pause
```

> Example 3
Create a file with value
```batch
@echo off
type "Here some text" > test.txt
```

Create a file without value
```batch
@echo off
type nul > test.txt
```

## Conditional Operator
<table class="table table-bordered" style="border: 10px solid #f2f2f2;">
<tbody>
<tr style="background-color: #f2f2f2; color: black;">
<th>Operators</th>
<th>Description</th>
</tr>
<tr>
<td><b>&amp;&amp;</b></td>
<td>For using Multiple Commands</td>
</tr>
<tr>
<td><b>||</b></td>
<td>For executing one from many commands</td>
</tr>
</tbody>
</table>

```batch
@echo off
SET /A x = 4 && SET /A x += 2
echo x = %x%
pause
```
Output
```
x = 6
```

## Assignment Operators

<table class="table table-bordered" style="border: 10px solid #f2f2f2;">
<tbody>
<tr style="background-color: #f2f2f2; color: black;">
<th>Operators</th>
<th>Example</th>
<th>Description</th>
</tr>
<tr>
<td><b>+=</b></td>
<td>Set /A x = 4<br>
x += 2<br>
Value of x: 6</td>
<td>2 is added to the value of x and<br>
the result is assigned to x</td>
</tr>
<tr>
<td><b>-=</b></td>
<td>Set /A x = 4<br>
x -= 2<br>
Value of x: 2</td>
<td>2 is subtracted from the value of x<br>
and the result is assigned to x</td>
</tr>
<tr>
<td><b>*=</b></td>
<td>Set /A x = 4<br>
x *= 2<br>
Value of x: 8</td>
<td>2 is multiplied to the value of x<br>
and the result is assigned to x</td>
</tr>
<tr>
<td><b>/=</b></td>
<td>Set /A x = 4<br>
x /= 2<br>
Value of x: 2</td>
<td>The value of x is divided by 2<br>
and the result is assigned to x</td>
</tr>
<tr>
<td><b>%=</b></td>
<td>Set /A x = 4<br>
x %= 2<br>
Value of x: 2</td>
<td>This will find the modulus<br>
and result is assigned to x</td>
</tr>
</tbody>
</table>

```batch
@echo off
SET /A x = 4
SET /A x += 2
echo x = %x%
SET /A x -= 2
echo x = %x%
SET /A x *= 2
echo x = %x%
SET /A x /= 2
echo x = %x%
SET /A x %= 2
echo x = %x%
pause
```

## if else statement
Syntax:
```batch
if (condition) dosomething

:: For if..else if
if (condition) (statement1) else (statement2)
```

> Example: Checking Integer Variables And String Variables
```batch
SET /A a=2
SET /A b=3
SET name1=Aston
SET name2=Martin

:: Using if statement
IF %a%==2 echo The value of a is 2
IF %name2%==Martin echo Hi this is Martin

:: Using if else statements
IF %a%==%b% (echo Numbers are equal) ELSE (echo Numbers are different)
IF %name1%==%name2% (echo Name is Same) ELSE (echo Name is different)
PAUSE
```

> Example: Check If Variable Is Defined Or Not
```batch
@echo OFF

::If var is not defined SET var = hello
IF "%var%"=="" (SET var=Hello)

:: This can be done in this way as well
IF NOT DEFINED var (SET var=Hello)
```

> Example: Check If A File Or Folder Exists

`EXIST` command is used to check if a file exists or not.
```batch
@echo OFF
::EXIST command is used to check for existence
IF EXIST D:\abc.txt ECHO abc.txt found
IF EXIST D:\xyz.txt (ECHO xyz.txt found) ELSE (ECHO xyz.txt not found)
PAUSE
```

## Loop
Syntax:
```batch
FOR %%var_name IN list DO example_code
```
***Note:*** In batch file for loops is that, variable declaration is done with `%%var_name` instead of `%var_name%`

>Example
```batch
@echo OFF
FOR %%x IN (1 2 3) DO ECHO %%x
PAUSE
```


## return code


|Exit Code/Error Code|	Details/Description|
|-|-|
|0|	Program successfully executed.|
|1	|Incorrect function. Indicates that Action has attempted to execute non-recognized command in Windows command prompt cmd.exe.|
|2	|Indicates that the system cannot find the file in that specified location.|
|3|	Indicates that the system cannot find the specified path.|
|5	|Access is denied. So the user has no access right to specified resource.|
|90090x2331|	Program is not recognized as an internal or external command, operable program or batch file. Indicates that command, application name or path has been misspelled when configuring the Action.|
|32212254770xC0000005-1073741819|	Access violation. Indicates that the executed program has terminated abnormally or crashed.|
|32212254950xC0000017-1073741801	|Not enough virtual memory is available. Indicates that Windows has run out of memory.|
|32212257860xC000013A-1073741510|	The application terminated as a result of a CTRL+C. Indicates that the application has been terminated either by user’s keyboard input CTRL+C or CTRL+Break or closing command prompt window.|
|32212257940xC0000142-1073741502|	The application failed to initialize properly. Indicates that the application has been launched on a Desktop to which current user has no access rights. Another possible cause is that either gdi32.dll or user32.dll has failed to initialize.|
|2212254950xC0000017-1073741801|	Not enough virtual memory is available. It indicates that Windows has run out of memory.|
|32212265050xC0000409-1073740791|	Stack buffer overflow / overrun. Error can indicate a bug in the executed software that causes stack overflow, leading to abnormal termination of the software.|
|37625075970xE0434F4D-532459699|	Unhandled exception in .NET application. More details may be available in Windows Event log.|


## Error Level
The environmental variable %ERRORLEVEL% contains the return code or the latest error level in the batch file, which is the latest error codes from the last command executed.

A common way of checking Error levels using %ERRORLEVEL% variable is:
```batch
IF %ERRORLEVEL% NEQ 0 Echo An error was found
IF %ERRORLEVEL% EQU 0 Echo No error found
```
Besides this, the command `EXIT /B %ERRORLEVEL%` at the end of the batch file also returns the error codes from the batch file.

`EXIT /B < exitcodes >` is used to return custom return codes.

## Functions
**Function Definition:**
```batch
:function_name 
Some_Operational_Code 
EXIT /B 0
```

**Functions Call:**
```batch
:: To call function without parameters 
CALL :function_name
 
:: To call function with parameters
CALL :function_name param1, param2,...,paramN

:: To call function with return values
CALL :function_name return_value1,return_value2,..,return_valueN
```

> Example
```batch
@echo OFF
CALL :basic_function 
EXIT /B %ERRORLEVEL% 
:basic_function
SET n=Harry
ECHO My name is %n%
PAUSE
EXIT /B 0
```

> Example: function with parameters
```batch
@echo OFF
CALL :param_function 20, 400
EXIT /B %ERRORLEVEL% 
:param_function
ECHO The square of %~1 is %~2
PAUSE
EXIT /B 0
```

> Example: function with return values
```batch
@echo OFF
CALL :retun_value_function ret_val1,ret_val2
ECHO The square root of %ret_val1% is %ret_val2%
PAUSE
EXIT /B %ERRORLEVEL% 
:return_value_function
SET %~1=100
SET %~2=10
EXIT /B 0
```

## Mini Projects

## Program to shutdown, reboot, hibernate, and logoff the computer

```batch
@echo OFF

ECHO "Choose an option .."
ECHO "1 = Logoff"
ECHO "2 = Reboot"
ECHO "3 = Hibernate"
ECHO "4 = Shutdown"

SET /p option=Choose one option-

IF %option%==1 SHUTDOWN /l
IF %option%==2 SHUTDOWN -r -t 10
IF %option%==3 SHUTDOWN /h
IF %option%==4 SHUTDOWN /s /f /t 0

PAUSE
```

## Create folder and files at current directory
This one I did for myself for being too lazy ><

```batch
@echo OFF
::Batch title
TITLE Laravel

::Creating folder if not exist
if not exist %cd%\layouts md layouts

::Goto `layout` folder
cd layouts

::Creating files
::File names with space. If file name have space, then use as follow "var name" or 'var name'. Example: varname varName 'var name' var-name var_name
SET list=header navbar footer all-css all-js alert sidenav
FOR %%a in (%list%) DO (
   type nul > %%a.blade.php
)

echo Following files created for [44mlayout[0m folder
FOR %%a in (%list%) DO (
   echo %%a
)

::Go back to main/parent directory
cd..

if not exist %cd%\pages md pages

cd pages

SET list=index about contact slider product
FOR %%a in (%list%) DO (
   type nul > %%a.blade.php
)

echo.
echo Following files created for [44mpage[0m folder
FOR %%a in (%list%) DO (
   echo %%a
)

PAUSE
```

## Coloring your batch scripts
Credits [@mlocati](https://gist.github.com/mlocati/)
Original [gist link](https://gist.githubusercontent.com/mlocati/fdabcaeb8071d5c75a2d51712db24011/raw/b710612d6320df7e146508094e84b92b34c77d48/win10colors.cmd)

Not Working? How to use? 
1. Go to original gist link
2. Copy from there & save it to bat/txt file
3. Then use the code from saved file to your project. 
That way it should work.
```batch
@echo off
cls
echo [101;93m STYLES [0m
echo ^<ESC^>[0m [0mReset[0m
echo ^<ESC^>[1m [1mBold[0m
echo ^<ESC^>[4m [4mUnderline[0m
echo ^<ESC^>[7m [7mInverse[0m
echo.
echo [101;93m NORMAL FOREGROUND COLORS [0m
echo ^<ESC^>[30m [30mBlack[0m (black)
echo ^<ESC^>[31m [31mRed[0m
echo ^<ESC^>[32m [32mGreen[0m
echo ^<ESC^>[33m [33mYellow[0m
echo ^<ESC^>[34m [34mBlue[0m
echo ^<ESC^>[35m [35mMagenta[0m
echo ^<ESC^>[36m [36mCyan[0m
echo ^<ESC^>[37m [37mWhite[0m
echo.

PAUSE
```
[color.txt](https://github.com/mehediishere/Linux/files/10001501/color.txt)

