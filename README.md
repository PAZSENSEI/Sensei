# Sensei
Projetos


Public Class Form1

    Private Sub Form1_Load(sender As System.Object, e As System.EventArgs) Handles MyBase.Load
        'Process.Start("MSPAINT")
        'WebBrowser1.Navigate("https://www.visaonline.com/login/LoginMain.aspx?goto=https%3A%2F%2Fsecure.visaonline.com%3A443%2F")

        'Timer1.Start()

    End Sub


    Private Sub Timer1_Tick(sender As System.Object, e As System.EventArgs) Handles Timer1.Tick

        WebBrowser1.Document.GetElementById("ctl00$PlaceHolderMain$txtUsername").SetAttribute("value", "paz")
        'Application.DoEvents()
        WebBrowser1.Document.GetElementById("ctl00$PlaceHolderMain$txtPassword").SetAttribute("value", "G")
        'Application.DoEvents()
        WebBrowser1.Document.GetElementById("btnLogin").InvokeMember("click")

        Timer1.Stop()
        Timer2.Start()

    End Sub

    Private Sub Timer2_Tick(sender As System.Object, e As System.EventArgs) Handles Timer2.Tick

        Application.DoEvents()
        WebBrowser1.Document.GetElementById("spanpersonaName").InvokeMember("click")
        Application.DoEvents()
        Timer2.Stop()

        Timer3.Start()

    End Sub


    Private Sub Timer3_Tick(sender As System.Object, e As System.EventArgs) Handles Timer3.Tick

        Application.DoEvents()
        WebBrowser1.Document.GetElementById("linkSwitchProfile").InvokeMember("click")
        Application.DoEvents()
        Timer3.Stop()
        Timer4.Start()

    End Sub

    Private Sub Timer4_Tick(sender As System.Object, e As System.EventArgs) Handles Timer4.Tick

        Timer4.Stop()

    End Sub

    Private Sub btnInicio_Click(sender As System.Object, e As System.EventArgs) Handles btnInicio.Click
        Dim myElemnt As HtmlElement = WebBrowser1.Document.GetElementById("aaw")
        Dim target As String = myElemnt.GetAttribute("href")
        WebBrowser1.Navigate(target)

        Dim TESTE As String
        Dim PageElements As HtmlElementCollection = WebBrowser1.Document.GetElementsByTagName("a")

        For Each CurElement As HtmlElement In PageElements

            For i = 0 To WebBrowser1.Document.GetElementsByTagName("a").Count - 1
                TESTE = (WebBrowser1.Document.GetElementsByTagName("a").Item(i).InnerText)

                If TESTE = "Banco do Nordeste" Then
                    CurElement.InvokeMember("Click")
                    GoTo pulou
                End If

                'WebBrowser1.Document.GetElementById(CurElement.ToString).InvokeMember("click")


            Next


        Next
pulou:
        'Dim TESTE As String
        'For Each item As HtmlElement In WebBrowser1.Document.Links
        '    ' Do whatever you want with found links

        '    TESTE = item.GetAttribute("href")
        '    If item.GetAttribute("href") = "https://vollnx.visaonline.com/secure/queue/goToQueue.do?queueType=w~709&page=work" Then
        '        item.InvokeMember("href")
        '        Exit For
        '    End If
        'Next





        'WebBrowser1.Navigate("https://vollnx.visaonline.com/secure/queue/goToQueue.do")

        'Dim myElemnt As HtmlElement = WebBrowser1.Document.GetElementById("return submitRequest(this.href, document.forms[0].sessionToken)")
        'Dim target As String = myElemnt.GetAttribute("href")
        'WebBrowser1.Navigate(target)

        '/secure/queue/goToQueue.do?queueType=w~709&page=work

        'Dim myElemnt As HtmlElement = WebBrowser1.Document.GetElementById("aaw")
        'Dim target As String = myElemnt.GetAttribute("href")
        'WebBrowser1.Navigate(target)



        '        Application.DoEvents()
        '        WebBrowser1.Document.GetElementById("spanpersonaName").InvokeMember("click")

        '        Application.DoEvents()
        '        WebBrowser1.Document.GetElementById("linkSwitchProfile").InvokeMember("click")

        '        Application.DoEvents()

        '        'GoTo pulou

        'pulou:
        '        Application.DoEvents()

    End Sub
    Private Sub HOME_Click(sender As System.Object, e As System.EventArgs) Handles HOME.Click

        WebBrowser1.Navigate("https://www.visaonline.com/login/LoginMain.aspx?goto=https%3A%2F%2Fsecure.visaonline.com%3A443%2F")

    End Sub


    

   

    

    Private Sub Timer5_Tick(sender As System.Object, e As System.EventArgs) Handles Timer5.Tick
 
    End Sub

    'Private Sub txtTime_MouseClick(sender As Object, e As System.Windows.Forms.MouseEventArgs)

    '    Application.DoEvents()


    '    WebBrowser1.Document.GetElementById("VOL.Global.switchProfile('14264586','/_layouts/GVOLProfileSwitch/GVOLProfileSwitch.aspx')").InvokeMember("click")

    '    'WebBrowser1.Document.GetElementById("ctl00$PlaceHolderMain$txtUsername").SetAttribute("value", "z")
    '    'WebBrowser1.Document.GetElementById("ctl00$PlaceHolderMain$txtPassword").SetAttribute("value", "0")
    '    'WebBrowser1.Document.GetElementById("btnLogin").InvokeMember("click")
    '    Application.DoEvents()

    '    Timer2.Start()

    'End Sub




 
End Class
