## 1. Overview
MEL script for Autodesk Maya.
You can change the name of one or more (two or more) objects you select at any one time.
As for the name change method, it is made to be able to select either of ①, ② below.

① Change name by deleting character string ([3-4] to be described later)
Change the name by deleting some of the character strings in the object name string.

② Rename by character string replacement ([3-5] described below)
B. Change the name by replacing some character strings in the string of object names or all character strings with another character string.

Creation date: 2017.10.3
Ver: v1.0.0
Operation confirmed OS: Windows 10 Pro
Operation confirmed Maya: Maya 2013, Maya 2014, Maya 2015, Maya 2016, Maya 2017
Character code: Shift_JIS
※ The character code is set to Shift_JIS. It will be for garbled characters in Japanese. Following the description on the official website below.
[◆ Prepare a Maya file containing Japanese or Simplified Chinese text] (https://knowledge.autodesk.com/en/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2016/EN// Maya / files / GUID-88109151-076A-4AB1-836A-85370B32A256-htm.html "Autodesk")

- - -

## 2. How to run MEL script

#### [2-1] Place MEL script file under appropriate directory of your choice.
 
#### [2-2] Launch Maya and open the script editor from the Window menu.

#### [2-3] From the script editor's File menu, click the source script.

#### [2-4] Selecting a MEL script file to be loaded will be selected, so select and load the MEL script placed with 1.
* It is OK to drag and drop the MEL script file into the input field in the script editor without [2-3] and [2-4].

#### [2-5] Press Ctrl + Enter in the entry field where the loaded script is displayed. This will be executed.

- - -

## 3. About each item in Window of script
#### [3 - 1] Rename Object
The title of the Window (which means the name of this MEL script) is displayed.

#### [3-2] Edit
Click here to display the following menu ①, ②.
① Clear Result of rename by string delete (Clear the result of name change by deleting character string)
Click here to clear the contents of ④ of [3-4] below.

② Clear Result of rename by string substitute (Clear name change result by string replacement)
Click here to clear the contents of ⑥ of [3-5] below.

#### [3-3] Information
Click here to display the menu of ① below.
① About RenameObject (About RenameObject)
Click here to display version information and creator of this MEL script.

#### [3-4] Rename by string delete (rename by deletion of string)
It is a tab for setting and executing for renaming by deleting a character string, and displaying the result.

① Setting of rename by string delete (setting name change by deleting character string)

② Search string (search character string)
Enter the character string to be searched for deletion.

③ Rename by string delete (rename by deleting character string)
When this button is pushed, rename processing by character string deletion is executed.
Only the part that matches the search character string entered in ② is deleted.

④ Result of rename by string delete (result of renaming by deletion of character string)
It becomes a box that displays the message of name change related processing by deleting character string.
The contents of the box can be cleared from [3-2].

#### [3-5] Rename by string substitute (renaming by string replacement)
It is a tab for setting and executing for renaming by string replacement, and displaying results.

① Setting of rename by string substitute (setting of name change by character string replacement)

② Target in name of object (subject of object name)
When renaming an object, you can select Whole (Whole) or Part (Partial) to replace the string.
If Whole is selected, all of the object's name will be replaced with the character string entered in ④ below.
When Part is selected, it searches whether the character string entered in the next ③ exists in the object name,
When it is found, it will be replaced with the character string entered in ④.

③ Search string (search character string)
Enter the character string to be searched for replacement.
You can enter only when Part is selected in ②.

④ Substitute string (replacement character string)
Enter the character string to replace.
You can enter it regardless of what you select in ②.

⑤ Rename by string substitute (Rename by string replacement)
When this button is pushed, name change processing by character string replacement is executed.
The character string to be replaced changes according to the selection contents of ②.

⑥ Result of rename by string substitute (result of renaming by character string replacement)
It becomes a box that displays the message of name change related processing by string replacement.
The contents of the box can be cleared from [3-2].

#### [3-6] Close window button
By pressing this button you can close the GUI window of this MEL script and exit.
