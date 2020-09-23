<div align="center">

## Input/Output to a text file


</div>

### Description

This code demonstrate a simple procedure for reading and writing to and from a text file. Level: Beginners
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[G\. M\. Faggiano](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/g-m-faggiano.md)
**Level**          |Unknown
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/g-m-faggiano-input-output-to-a-text-file__1-1837/archive/master.zip)





### Source Code

```
' Example
' Write and read from a text file
' for beginners
'
' Note: this type of read/write will
' only allow for one line to be
'  writen or read from a file.
' A seperate file must be used in
'  each instance using this method.
' This is not the best method, but
'  probably the easiest.
' ===============================
'
' Author: G. M. Faggiano
' Faggiano Internet Business Development
' http://fibdev.com
' vb@fibdev.com
' ======================================
'
' Step 1,
' Create a new project and save it or open
' an existing project
' Step 2,
' Put a textbox object on form1
' Step 3,
' place two command buttons, command1 and
' command2
' Step 4,
' In the project directory create a text file
' and name it test.txt
' General Declarations
' Variable to hold the location
' of the text file
Dim txtPath As String
' Variable to hold the text to
' be writen to the text file
Dim txtOut As String
' Variable to hold the text
' to be read from the text file
Dim txtIn As String
Private Sub Command1_Click()
 ' Set variable to hold the location
 ' of the text file
 txtPath = App.Path & "\test.txt"
 ' error handle file location
  If InStr(thefile, "\\") Then _
   thefile = App.Path & "test.txt"
 ' set variable as the contence of the
 ' text box
 txtOut = Text1.Text
 ' open the text file to be
 ' writen to
 Open txtPath For Output As #1
 ' write the contence of the variable to
 ' the text file
 Print #1, txtOut
 ' close the text file
 Close #1
 ' clear the text box
 Text1.Text = ""
End Sub
Private Sub Command2_Click()
 ' Set variable to hold the location
 ' of the text file
 txtPath = App.Path & "\test.txt"
 ' error handle the variable
  If InStr(thefile, "\\") Then _
   thefile = App.Path & "test.txt"
 ' open the text file to be read from
 Open txtPath For Input As #1
 ' set the input variable to the contence
 ' of the text file
 Input #1, txtIn
 ' set the text box text to the variable
 Text1.Text = txtIn
 ' close the file
 Close #1
End Sub
```

