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
<img width="887" height="111" alt="594687893-4286b51a-cee7-4810-93d6-b3a0cfede39b" src="https://github.com/user-attachments/assets/c0c59301-a242-4846-94d4-059bac77fa8b" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="911" height="55" alt="594687974-d74ba5df-9c89-485d-904f-7a404682bddf" src="https://github.com/user-attachments/assets/56fd6b20-7daa-471e-a57a-f1c78285f3d7" />


Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="767" height="107" alt="594688081-0fc42efd-f38e-4613-b668-8efffe545e83" src="https://github.com/user-attachments/assets/a0080874-77c5-4316-90c1-c4f1c74a91df" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="819" height="107" alt="594688134-a976c61c-d359-46e5-8ef6-11e19b471959" src="https://github.com/user-attachments/assets/e2392ce9-72c0-41df-90c2-a094d35582d8" />
<img width="819" height="107" alt="594688134-a976c61c-d359-46e5-8ef6-11e19b471959" src="https://github.com/user-attachments/assets/11a6994e-1ebc-412a-9350-4315ebce618e" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="594688301-4e9412f5-298d-46ce-ac55-76fc24b974f5" src="https://github.com/user-attachments/assets/4876c374-edde-4d54-a4e8-a9c0cf98ad43" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="658" height="171" alt="594688503-d9e4271f-f442-462f-874a-daece1ce36cb" src="https://github.com/user-attachments/assets/767ad718-bbe2-469a-ad3c-c94a5022b025" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="594688677-55c37ab9-f8b7-4bcd-8abe-2d3ecf8a095b" src="https://github.com/user-attachments/assets/cc2e61be-6a03-404c-8cb5-9d1679563f4b" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="574" height="613" alt="594688731-e39c6f23-6469-4d05-abee-a445fc6d187a" src="https://github.com/user-attachments/assets/b9fd3f04-fac8-446c-af42-752f552a317a" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="614" height="218" alt="594688807-e71be7a2-f2fd-451e-bc1e-14cbc99854fa" src="https://github.com/user-attachments/assets/8c2aa4b7-de6c-463c-9a2b-8e07d55102e2" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".


```
@echo off
set name=John
echo Hello, %name%!
pause
```


## OUTPUT
<img width="506" height="80" alt="594688993-045b5c2d-3d26-42c8-bbe6-93df0904db8a" src="https://github.com/user-attachments/assets/e9dc12f1-5d61-472f-b4c9-2514acd254e7" />



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


<img width="664" height="159" alt="594689167-e85a0b3c-389c-4192-b8f2-a772c3e966ae" src="https://github.com/user-attachments/assets/49b818bd-3ce3-42cc-a826-9f1c4b1f7516" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT

<img width="550" height="204" alt="594689335-c4efefe8-ae2a-4f56-831f-43d7eaaa8249" src="https://github.com/user-attachments/assets/96673946-4e76-4a5f-abc3-af31e50d3560" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
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
<img width="488" height="80" alt="594689555-17278ad2-109e-417d-bbe5-556106173178" src="https://github.com/user-attachments/assets/b42a082e-0e61-4468-a1a1-141ffe1f4ce0" />


DEVELOPED BY: MIRDULA D

REGISTRATION NO. 212225040234

# RESULT:
The commands/batch files are executed successfully.

