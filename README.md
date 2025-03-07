**Cafeteria Management Console Application**

Overview

The Cafeteria Management Console Application is a C# program that allows users to register, log in, and manage their cafeteria orders. The system provides functionalities such as placing orders, modifying orders, canceling orders, viewing order history, and managing wallet balances.

Features

1. Main Menu

     * User Registration
      
     * User Login
      
     * Exit

2. User Registration

Users need to provide:
    
   * Name
    
   * Father Name
    
   * Mobile Number
    
   * Email ID
    
   * Gender
    
   * WorkStation Number
    
   * Initial Wallet Balance

A unique UserID (e.g., SF1001) is auto-generated upon successful registration.

3. User Login

Users log in using their UserID. After successful login, they can:

   * View Profile
    
   * Order Food
    
   * Modify Order
    
   * Cancel Order
    
   * View Order History
    
   * Recharge Wallet
    
   * Check Wallet Balance
    
   * Logout

4. Food Ordering System

      Users can view available food items and select products based on FoodID.

If the required quantity is available, the system reduces the stock and adds items to a temporary cart.

      Users confirm or cancel their cart before finalizing the order.

      If sufficient wallet balance is available, the order is placed successfully; otherwise, users are prompted to recharge.

5. Modify Order

      Users can modify an existing order by selecting an OrderID.
      
      The system allows modifying item quantities and recalculates the order price.

6. Cancel Order

      Users can cancel an order if it has the status "Ordered".
      
      Canceled orders restore the deducted amount to the user's wallet and return the food quantity to stock.

7. Order History

      Users can view their past orders, including details such as OrderID, Order Date, Total Price, and Order Status.

8. Wallet Management

      Users can recharge their wallet by adding funds.
      
      Wallet balance can be checked anytime.

**Classes and Responsibilities**

**PersonalDetails Class**

Stores basic user information.

**IBalance Interface**

Defines methods for wallet management (WalletRecharge, DeductAmount).
**
UserDetails Clas**s

Inherits PersonalDetails and implements IBalance.

Stores user details and manages wallet operations.

**FoodDetails Class**

Stores food-related details (e.g., FoodID, FoodName, FoodPrice, AvailableQuantity).

**OrderDetails Class**

Stores order details (e.g., OrderID, UserID, Order Date, Total Price, Order Status).

**CartItem Class**

Stores items added to an order.

**Operations Class**

Handles all system operations, including:

Registering users

Logging in users

Ordering food

Modifying and canceling orders

Managing wallet transactions

**Program Class**

Contains only the Main() method to start execution.



**How to Run**

Open the project in Visual Studio Code or any C#-compatible IDE.

Ensure .NET SDK is installed.

Run the application using the terminal:

dotnet run

**Future Enhancements**

Implement a database to store user and order details persistently.

Add an admin panel to manage food items and orders.

Implement a GUI version of the application.
