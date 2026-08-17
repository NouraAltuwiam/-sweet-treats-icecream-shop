# -sweet-treats-icecream-shop
# Sweet Treats – Ice Cream Shop Management System (v2)

A Java desktop application simulating a full ice cream shop ordering system, built with an emphasis on Object-Oriented Design, custom data structures, and persistent storage. This is an extended version of an earlier console-only implementation, upgraded with a linked-list-based inventory model, custom exception handling, and a Swing-based GUI layer.

## Features

- Manage up to 5 carts, each holding ice cream orders
- Add, remove, and search ice cream items within a cart
- Automatic price calculation based on flavor type and scoop count
- Save and reload cart/shop data to text files between sessions
- Graphical interface (Java Swing) alongside the console menu
- Input validation with a custom checked exception for invalid cart operations

## Project Structure

```
Project2/
├── src/
│   ├── IceCream.java          # Abstract base class
│   ├── RegularIceCream.java   # Abstract subclass
│   ├── SpecialIceCream.java   # Abstract subclass
│   ├── Vanilla.java
│   ├── Chocolate.java
│   ├── SugarFreeVanilla.java
│   ├── SugarFreeChocolate.java
│   ├── Node.java              # Linked list node
│   ├── Cart.java              # Linked-list-based cart
│   ├── Shop.java              # Manages multiple carts
│   ├── InvalidCartException.java
│   ├── TestIceCreamShop.java  # Main entry point (console menu)
│   ├── Frame1.java / .form    # GUI: main window
│   ├── CartsFrame.java / .form
│   └── OrderFrame.java / .form
```

## Design Overview

- **Abstraction & Inheritance:** `IceCream` is an abstract base class extended by `RegularIceCream` and `SpecialIceCream`, which are in turn extended by concrete flavor classes (`Vanilla`, `Chocolate`, `SugarFreeVanilla`, `SugarFreeChocolate`).
- **Polymorphism:** each concrete flavor overrides `calculatePrice()` with its own pricing rule.
- **Custom Data Structure:** `Cart` stores its ice cream items using a self-built singly linked list (`Node`) instead of an array, supporting dynamic insertion/removal.
- **Exception Handling:** `InvalidCartException` is thrown when a cart exceeds its item limit, and caught at the point of use to keep the program running.
- **File I/O:** `Cart` and `Shop` can serialize their state to text files (`Cart_X_Details.txt`, `Shop_Summary.txt`) and reload it on the next run.
- **GUI Layer:** `Frame1`, `CartsFrame`, and `OrderFrame` provide a Swing-based interface built with the NetBeans GUI builder.

## How to Run

1. Open the project in NetBeans (recommended, since it includes `.form` files) or import `src/` into any Java IDE.
2. Build and run `TestIceCreamShop.java` as the main class.
3. Follow the on-screen console menu, or launch the GUI window if enabled.

## Skills Demonstrated

Java · Object-Oriented Programming · Abstraction & Inheritance · Polymorphism · Custom Exception Handling · Linked Lists (Data Structures) · File I/O · Java Swing (GUI) · NetBeans IDE
