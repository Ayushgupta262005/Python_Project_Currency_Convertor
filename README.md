This Python project is a command-line currency converter that allows users to convert an amount from Indian Rupees (INR) to various other currencies. The conversion rates are read from a file named currencyData.txt. Here’s a detailed explanation of the project's components and workflow:

Workflow:
Reading the Currency Data:

The program begins by opening the currencyData.txt file using a with open statement, which ensures the file is properly closed after being read.
The readlines() method reads all lines from the file into a list called lines. Each line contains a currency name and its corresponding conversion rate to INR, separated by a tab (\t).
Storing Conversion Rates in a Dictionary:

An empty dictionary, currencyDict, is created to store the currency data.
The program iterates over each line in the lines list, splitting each line into two parts using the tab character as a delimiter. The first part is the currency name, and the second part is the conversion rate.
These values are stored in the dictionary with the currency name as the key and the conversion rate (as a string) as the value.
User Input for Amount:

The program prompts the user to enter an amount in INR that they wish to convert.
Displaying Available Currencies:

It then displays all available currency options by printing the keys from the currencyDict dictionary, allowing the user to see the target currencies.
Selecting the Target Currency:

The user is asked to choose one of the displayed currencies by entering its name.
Performing the Conversion:

The program converts the amount in INR to the target currency by multiplying the amount by the conversion rate obtained from the dictionary.
The conversion rate is first converted to a float for the multiplication.
Displaying the Result:

Finally, it prints the converted amount, showing the original amount in INR and the equivalent amount in the selected currency.Limitations and Improvements:
Hardcoded Data File: The program requires the currencyData.txt file with a specific format. Error handling could be added for missing or incorrectly formatted files.
Conversion Rate Updates: The current implementation uses static rates from the file. To improve, the program could fetch real-time rates from an API.
Enhanced User Input Validation: The code could include checks for non-numeric values and invalid currency names.
GUI Option: Adding a graphical interface using libraries like tkinter would make the converter more user-friendly.
