# SQL
数据库------A course in TJU grade2

Task of the first month：VB.NET
last homework: make a creative project
idea:1) using mathmodel's idea, connecting access and vb
     2)make use of vusial function of vb.net
     3)make an menu for ordering: change statistics in access and order in vb
     4)simulate Mc selp-heip ordering system

https://github.com/EbookFoundation/free-programming-books/blob/master/free-programming-books-zh.md

VB.net lab9: menu ordering system 

lab10: do a math plot system----sin
Private Sub Command1_Click()
Const pi = 3.14159
Dim x As Single, a As Single, w As Single, f As Single, y As Single
Dim cz As Single, zz As Single
Picture1.Scale (-5, 10)-(10, -10)
Picture1.DrawWidth = 3
Picture1.Line (-5, 0)-(10, 0)
Picture1.Line (0, -10)-(0, 10)
Picture1.Line (0, 10)-(0.2, 9.5)
Picture1.Line (10, 0)-(9.5, 0.2)
Picture1.Line (10, 0)-(9.5, -0.2)
a = Val(Text1.Text)
w = Val(Text2.Text)
f = Val(Text3.Text)
Picture1.ForeColor = RGB(255, 0, 0)
Picture1.DrawWidth = 2
cz = -f / w
zz = (2 * pi - f) / w
For x = cz To zz Step (zz - cz) / 200
y = a * Sin(w * x + f)
Picture1.PSet (x, y)
Next x
End Sub
Private Sub Command2_Click()
Picture1.Cls
Picture1.Scale (-5, 10)-(10, -10)
Picture1.ForeColor = RGB(255, 255, 0)
Picture1.DrawWidth = 3
Picture1.Line (0, 10)-(-0.2, 9.5)
Picture1.Line (0, 10)-(0.2, 9.5)
Picture1.Line (10, 0)-(9.5, 0.2)
Picture1.Line (10, 0)-(9.5, -0.2)
Picture1.Line (-5, 0)-(10, 0)
Picture1.Line (0, -10)-(0, 10)
End Sub
Private Sub Command3_Click()
End
End Sub
Private Sub Form_Load()
Text1.Text = 1
Text2.Text = 1
Text3.Text = 0
End Sub
Private Sub Text1_LostFocus()
If Abs(Val(Text1.Text)) > 9 Then
Text1.Text = 1
End If
End Sub
Private Sub Text2_LostFocus()
If Abs(Val(Text2.Text)) > 9 Then
Text2.Text = 1
End If
End Sub
