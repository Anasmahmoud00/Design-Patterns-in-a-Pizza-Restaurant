1. Factory Pattern:

    SOLID Principle Addressed: Open/Closed Principle 
    Explanation: The PizzaFactory class is responsible for creating pizza objects without directly invoking constructors, making it open for extension  but closed for modification . By following the Factory Pattern, the system can accommodate future pizza types without changing the existing code.

2. Decorator Pattern (ToppingDecorator):

    SOLID Principle Addressed: Open/Closed Principle 
    Explanation: The ToppingDecorator class allows the dynamic addition of toppings to pizzas without modifying the existing pizza classes. This aligns with the OCP, as new toppings can be added by creating new decorator subclasses rather than altering the base pizza class. This pattern also facilitates easy extensions of toppings without altering core pizza behavior.

3. Singleton Pattern (InventoryManager):

    SOLID Principle Addressed: Single Responsibility Principle 
    Explanation: The InventoryManager class uses the Singleton Pattern to ensure that only one instance of the inventory manager exists throughout the system. Its responsibility is solely to manage inventory, keeping it simple and in line with SRP. By ensuring only one instance of the class, the system prevents any unnecessary complexity and ensures that the inventory management logic remains centralized and consistent.

4. Strategy Pattern (PaymentMethod and Subclasses):

    SOLID Principle Addressed: Dependency Inversion Principle 
    Explanation: The PaymentMethod interface defines a strategy for payment, and different payment methods  implement this interface. The system depends on the PaymentMethod abstraction rather than concrete payment classes. This ensures that high-level modules depend on abstractions rather than concrete implementations, adhering to the DIP and allowing for easy addition of new payment methods without modifying existing code.

5. **General SOLID Principles Addressed:**

    Single Responsibility Principle : Each class in the design has a single responsibility .

    Liskov Substitution Principle : Subtypes can be substituted for the base type ToppingDecorator without altering the correctness of the program.

    Interface Segregation Principle: The PaymentMethod interface is designed in a way that allows different classes to implement only the methods they need, avoiding "fat" interfaces.
    
    Dependency Inversion Principle : High-level modules like payment processing depend on the PaymentMethod abstraction, ensuring low-level details are encapsulated.
