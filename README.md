# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations


Create a directory named "my-folder"
## COMMAND AND OUTPUT

<img width="887" height="111" alt="601347019-c0c59301-a242-4846-94d4-059bac77fa8b" src="https://github.com/user-attachments/assets/121a8d5b-12d0-47ef-9398-a55514e4bce4" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="911" height="55" alt="601347102-56fd6b20-7daa-471e-a57a-f1c78285f3d7" src="https://github.com/user-attachments/assets/40cb10a5-3360-4be5-96c0-bed9d69a0dde" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="767" height="107" alt="601347183-a0080874-77c5-4316-90c1-c4f1c74a91df" src="https://github.com/user-attachments/assets/8169972d-7b94-43b1-ab01-9fda3245b5c4" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="819" height="107" alt="601347238-e2392ce9-72c0-41df-90c2-a094d35582d8" src="https://github.com/user-attachments/assets/5882f4bc-e64f-4694-a3fd-9b449b7127d1" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="601347383-4876c374-edde-4d54-a4e8-a9c0cf98ad43" src="https://github.com/user-attachments/assets/ea2afde4-44a1-4ba0-a3f6-92e50e636f3e" />



Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="658" height="171" alt="601347421-767ad718-bbe2-469a-ad3c-c94a5022b025" src="https://github.com/user-attachments/assets/3526c12c-7bd9-4322-93d9-95964b1e30a8" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="601347464-cc2e61be-6a03-404c-8cb5-9d1679563f4b" src="https://github.com/user-attachments/assets/c0ebd0cc-ebf9-40c8-96f0-9b51762b60c8" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="574" height="613" alt="601347495-b9fd3f04-fac8-446c-af42-752f552a317a" src="https://github.com/user-attachments/assets/85cc1ca0-96c3-46b5-8c0f-62f34d62f5c3" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="614" height="218" alt="601347562-8c2aa4b7-de6c-463c-9a2b-8e07d55102e2" src="https://github.com/user-attachments/assets/cd382d2b-a483-49fa-b404-4d22ad404b37" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```

@echo off
set name=John
echo Hello, %name%!
pause

```



## OUTPUT

<img width="506" height="80" alt="601347698-e9dc12f1-5d61-472f-b4c9-2514acd254e7" src="https://github.com/user-attachments/assets/7bd59cce-b5db-48d5-a0ab-c22245444834" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

```

## OUTPUT

<img width="664" height="159" alt="601347830-49b818bd-3ce3-42cc-a826-9f1c4b1f7516" src="https://github.com/user-attachments/assets/9d185dc3-0f71-4a48-b11e-5a93392990ab" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```


## OUTPUT

<img width="550" height="204" alt="601347915-96673946-4e76-4a5f-abc3-af31e50d3560" src="https://github.com/user-attachments/assets/489ee91c-3217-4bf9-87db-faed4df0b376" />


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

<img width="488" height="80" alt="601348046-b42a082e-0e61-4468-a1a1-141ffe1f4ce0" src="https://github.com/user-attachments/assets/cca562e8-d0d5-4681-bcff-0928c944349b" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

Instructions: Use the IF EXIST conditional statement. Make sure the script works for files located in the same directory as the batch file. Use pause to keep the command window open after displaying the message. Expected Output (if the file exists):

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```

## OUTPUT

<img width="488" height="80" alt="601348046-b42a082e-0e61-4468-a1a1-141ffe1f4ce0" src="https://github.com/user-attachments/assets/cca9fcd8-cb87-4f56-bfd6-838617b78e70" />


# RESULT:
The commands/batch files are executed successfully.

