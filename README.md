# WarehouseLoadingSystem
Warehouse Loading System


Scenario
You are hired as a developer for a logistics warehouse. You must build a console-based Warehouse Loading System that lets staff:

Store arriving items into the warehouse (stack — last in, first out)
Register arriving trucks waiting to be loaded (queue — first in, first out)
Load the next truck using the top item from the stack and the front truck from the queue


Requirements
1. Create ADT Classes
Item class
Fields: code, name, quantity
Constructor to initialize values
toString() to display item info like:
C101 | Rice Sack         | qty=20


Truck class
Fields: plate, driver
Constructor to initialize values
toString() to display truck info like:
ABC-123 | Juan Dela Cruz


2. Use the Following Data Structures
ArrayDeque<Item> warehouseStack — to store items (LIFO)
ArrayDeque<Truck> truckQueue — to store trucks (FIFO)


3. Implement Menu Operations
=== Warehouse Loading System ===
[1] Store item (push)
[2] View warehouse stack
[3] Register arriving truck (enqueue)
[4] View waiting trucks
[5] Load next truck (pop item + poll truck)
[0] Exit


Behavior:
• [1] Store item
Ask for code, name, and quantity
Push it to the top of the warehouseStack


• [2] View warehouse stack
Show items from top to bottom (stack order)
Sample Output:

TOP →
C103 | Soap Box           | qty=50
C102 | Water Bottle Pack  | qty=10
C101 | Rice Sack           | qty=20
← BOTTOM

• [3] Register arriving truck
Ask for plate and driver
Enqueue into truckQueue
Sample Output:

Truck plate: ABC-123
Driver name: Juan Dela Cruz
Registered: ABC-123 | Juan Dela Cruz


• [4] View waiting trucks
Show trucks from front to rear (queue order)
Sample Output:

FRONT →
ABC-123 | Juan Dela Cruz
XYZ-456 | Maria Santos
← REAR


• [5] Load next truck
Pop the top item from warehouseStack
Poll the front truck from truckQueue
Print loading result
Sample Output:

Loaded: C103 | Soap Box | qty=50 → ABC-123 | Juan Dela Cruz
Remaining items in warehouse: 2
Remaining trucks waiting: 1

• [0] Exit
Ends the program

Submission
Submit:
Source code
Screenshot showing a full run of:
Adding at least 3 items
Registering at least 2 trucks
Viewing both lists
Successfully loading 1 truck
