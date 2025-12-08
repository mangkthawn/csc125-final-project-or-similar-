# csc125-final-project-or-similar-
My Python final project for CSC-125"
Display "Welcome to UKP Burmese Restaurant"

Create a dictionary called menu
Add "Sushi" with price 10.99
Add "Pepsi" with price 2.99
Add "Pizza" with price 9.99

Set tax_rate to 0.07

Create an empty dictionary called order

Display "Restaurant Menu"
For each item and price in menu
 Display item and price
End For

Ask user "Please enter your name:"
Read customer_name

Display "Please start ordering. Type 'done' when finished."

While True
 Ask user "Enter an item you want to order:"
 Read item

 If item equals "done"
  Break the loop
 End If

 If item not in menu
  Display "Sorry, that item is not in the menu. Please try again."
  Continue to next loop
 End If

 Ask user "Enter quantity for this item:"
 Read quantity

 If quantity is not a whole positive number
  Display "Quantity must be a whole positive number."
  Continue to next loop
 End If

 If quantity is less than or equal to 0
  Display "Quantity must be at least one."
  Continue to next loop
 End If

 If item already in order
  Add quantity to existing amount in order
 Else
  Add item and quantity to order
 End If
End While

If order is empty
 Display "You did not order anything. Goodbye."
 Stop program
End If

Set subtotal to 0

For each item and quantity in order
 Set price to menu[item]
 Set line_total to price times quantity
 Add line_total to subtotal
End For

Calculate tax as subtotal times tax_rate
Calculate total as subtotal plus tax

Display "Receipt"
Display "Customer: " followed by customer_name

For each item and quantity in order
 Set price to menu[item]
 Set line_total to price times quantity
 Display item, quantity, price, and line_total
End For

Display "Subtotal: $" followed by subtotal
Display "Tax: $" followed by tax
Display "Total: $" followed by total
Display "Thank you for your order!"
