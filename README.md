namespace _00
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            // Initialize total
            int iTotal = 0;

            // Get and process coffee price and quantity if "coffee" is selected
            string strCoffeePrice = tbCoffeePrice.Text;
            string strCoffeeQuantity = tbCoffeeQuantity.Text;

            int iCoffeePrice = 0;
            int iCoffeeQuantity = 0;
            try
            {
                if (coffee.Checked)  // Check if the "coffee" option is selected
                {
                    iCoffeePrice = int.Parse(strCoffeePrice);
                    iCoffeeQuantity = int.Parse(strCoffeeQuantity);
                    // Calculate coffee total
                    iTotal += iCoffeePrice * iCoffeeQuantity;
                }
            }
            catch (Exception)
            {
                // Handle exceptions
                iCoffeePrice = 0;
                iCoffeeQuantity = 0;
            }

            // Get and process green coffee price and quantity if "green" is selected
            string greenCoffeePrice = tbGreenCoffeePrice.Text;
            string greenCoffeeQuantity = tbGreenCoffeeQuantity.Text;

            int iGreenCoffeePrice = 0;
            int iGreenCoffeeQuantity = 0;
            try
            {
                if (grr.Checked)  // Check if the "green coffee" option is selected
                {
                    iGreenCoffeePrice = int.Parse(greenCoffeePrice);
                    iGreenCoffeeQuantity = int.Parse(greenCoffeeQuantity);
                    // Calculate green coffee total
                    iTotal += iGreenCoffeePrice * iGreenCoffeeQuantity;
                }
            }
            catch (Exception)
            {
                // Handle exceptions
                iGreenCoffeePrice = 0;
                iGreenCoffeeQuantity = 0;
            }

            // Display the total in the TextBox
            tbTotal.Text = iTotal.ToString();
        }

        private void maskedTextBox5_MaskInputRejected(object sender, MaskInputRejectedEventArgs e)
        {

        }

        private void maskedTextBox4_MaskInputRejected(object sender, MaskInputRejectedEventArgs e)
        {

        }
    }
}
