# Lab-5-and-6
Public Class Form1
    Private Sub GroupBox1_Enter(sender As Object, e As EventArgs) Handles GroupBox1.Enter

    End Sub
    
    

    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles btnCalculate.Click
        ' Try Catch Statement for 20 % multiplier
        Try
            Const decMULTIPLIER As Decimal = CDec(0.2)

            Dim decAdultGross As Decimal
            Dim decChildGross As Decimal
            Dim decTotalGross As Decimal
            Dim decAdultNet As Decimal
            Dim decChildNet As Decimal
            Dim decTotalNet As Decimal



            'Calculate and display Adult Gross Sales
            decAdultGross = CDec(txtAdultTicketPrice.Text) *
                CDec(txtAdultTicketsSold.Text)
            lblAdultGross.Text = decAdultGross.ToString("c")

            'Child Gross Pay
            decChildGross = CDec(txtChildTicketPrice.Text) *
                CDec(txtChildTicketsSold.Text)
            lblChildGross.Text = decChildGross.ToString("c")

            'Add Adult and Gross Sales'
            decTotalGross = decChildGross + decAdultGross
            lblTotalGross.Text = decAdultNet.ToString("c")

            'Calculate and Show Adult Net Sales
            decAdultNet = decAdultGross * decMULTIPLIER
            lblAdultNet.Text = decAdultNet.ToString("c")

            'Calculate and Show Child Net Sales
            decChildNet = decChildGross * decMULTIPLIER
            lblChildNet.Text = decTotalNet.ToString("c")

        Catch
            'Error message
            MessageBox.Show("All input must be numeric")
        End Try
    End Sub



    Private Sub btnClear_Click(sender As Object, e As EventArgs) Handles btnClear.Click
        txtAdultTicketPrice.Clear()
        txtAdultTicketsSold.Clear()
        txtChildTicketPrice.Clear()
        txtChildTicketsSold.Clear()
        lblAdultGross.Clear()
        lblAdultNet.Clear()
        lblChildGross.Clear()
        lblChildNet.Clear()
        lblTotalNet.Clear()
        txtAdultTicketPrice.Focus()
    End Sub



    Private Sub btnExit_Click(sender As Object, e As EventArgs) Handles btnExit.Click
        Me.Close()
    End Sub
End Class
