# Decentralised_Splitwise

We have made a decentralised payment splitting app.
Our app checks most of the boxes which are expected from a payment splitting app.

Let’s dive into the details of our app.

Its a decentralised way to handle group expenses and it splits bills among friends or colleagues seamlessly. With the help of Solidity for smart contract formation, HTML for the user interface, and CSS for styling, we've created a user-friendly and efficient app.

We start by registering Accounts in the contract, each person enters their name and a unique username(which will be very helpful in reducing the tedious and error-prone handling of addresses by users). 

Then one of the registered member forms a group and is assigned the role of the owner of the group. 

The owner has the rights to add or remove members from the group and only has to use the unique usernames of the other person to add them to the group. This makes it very easy and efficient than having to enter entire addresses into the function which can lead to errors. 

After the owner has created the group and has all the required members he can call the add expenses function to tell the smart contract the total amount paid by the owner. 

For the sake of simplicity we have assumed that the owner pays in full, of the total bill and the bill is distributed evenly amongst all the members. 

One can use the getShare function to find out the price that every person has to pay, and getAdd function to get the address of the receiver. 

After this has happened all the members can individually call the makePayment function to give the payment to the owner of the group by passing their username(so that they can be sure that they are sending the money from their username only) and the address of the receiver. 

The owner can call the PaymentSettled function at any point of time and it will return a boolean True if all the members have paid their part or False otherwise.




