## DSA Lab 1 - Inventory Management System

#### **Objective:**

- Students will design and implement a simple inventory management system using C++, using objects, and applying constructors and member functions.

#### **Assignment Details:**

1. **Create the `Item` Class:**
    - **Attributes:**
        - `string name`: The name of the item.
        - `int quantity`: The number of units available.
        - `double price`: The price per unit.
    - **Member Functions:**
        - **Constructor:** Initialize the attributes.
        - **Destructor:** Display a message indicating that the object is being destroyed.
        - `void displayItem()`: Print the item's details (name, quantity, and price).
        - `void addItem(int amount)`: Increase the quantity by the given amount.
        - `void removeItem(int amount)`: Decrease the quantity by the given amount.
        - `double calculateTotalValue()`: Return the total value of the item based on quantity and price.
2. **Create the `Inventory` Class:**
    - **Attributes:**
        - `Item items[64]`: An array of `Item` objects, with a fixed size of 64.
        - `int itemCount`: Keeps track of the current number of items in the inventory.
    - **Member Functions:**
        - **Constructor:** Initialize the inventory with an empty array and set `itemCount` to 0.
        - `void addItem(const Item& newItem)`: Add a new item to the inventory. Ensure that `itemCount` does not exceed 64.
        - `void removeItem(const string& itemName)`: Remove an item from the inventory by name.
        - `void displayInventory()`: Print the details of all items in the inventory.
        - `Item* findItem(const string& itemName)`: Return a pointer to an item in the inventory by name (or `nullptr` if not found).
3. **Main Program:**
    - In the `main` function, create an `Inventory` object.
    - Add several `Item` objects to the inventory.
    - Use the `displayInventory` function to show the items in the inventory.
    - Modify the inventory by adding or removing quantities from specific items.
    - Calculate and display the total value of all items in the inventory.

#### **Deliverables:**

- Provide the full source code with appropriate comments.
### Hardcode Mode: Deep Copies and References

#### **Objective:**

- Enhance the Inventory Management System to explore advanced OOP concepts such as deep copying and using references in C++.

#### **Activity Details:**

1. **Implement Deep Copy in `Item` Class:**
    - Modify the `Item` class to include a deep copy constructor and an overloaded assignment operator.
    - Explain how these changes prevent shallow copying issues, especially when dealing with dynamic memory allocation (e.g., if you added a dynamically allocated array to `Item`).
2. **References in `Inventory` Class:**
    - Modify the `findItem` function in the `Inventory` class to return a reference to the `Item` object instead of a pointer.
    - Add a new function `void updateItemPrice(const string& itemName, double newPrice)` that uses the reference to modify the price of an item directly.
3. **Test Cases:**
    - In the `main` function, demonstrate the deep copy functionality by creating a new `Item` using the copy constructor.
    - Use the `updateItemPrice` function to change the price of an existing item and display the updated inventory.

#### **Deliverables:**

- Provide the full source code with appropriate comments.


### Rurbic:

*Course Content*

- 6 points - All required items are present. 
- 5 points - Task was completed, but supplementary materials are weak or missing.
	- Code was uncommented. 
	- Solution is correct but is significantly difficult to read, highly inefficient, very clumsy, very difficult to extend etc. From the original Jargon File, we would refer to solutions like this as *kluge*.
	- Reflection questions related to content were incorrect.
- 4 points - Task was attempted, but is missing major components. 
	- Coding prompt was only partially completed
	- Some deliverables are missing
- 3 points - Did not attempt or student should reattempt. 

*Workforce Readiness*

- 4 points - Exemplified  WFR standards
	- Language is professional. 
	- Work is clear and easy to read. 
	- Used deductive reasoning guide solution.
	- Reflection on own work was thoughtful and honest.
- 3 points - Practiced WFR standards
	- Language is readable but not professional. 
	- Work is understandable but not completely clear. 
	- Reflection on own work was weak.
	- Citations were not complete.
- 2 points - Developing WFR standards
	- Work is unprofessional. Significant spelling or grammar errors.
	- Did not attempt or student should reattempt. 
