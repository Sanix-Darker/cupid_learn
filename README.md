# CUPID (Composable Unix Predictable Ideomatic Domain base)

## LEARN MAP

![map](./cupid.svg)

[CHECK THE INTERACTIVE MAP](https://sanix-darker.github.io/cupid_learn/cupid.html)

## CONCEPTS

## Introduction to CUPID
- What is CUPID?
  - CUPID (Composable Unix Predictable Ideomatic Domain base) is a framework for building Unix-based systems with predictable behavior and composability.
  - It emphasizes ideomatic design principles and domain-specific customization.

## Core Concepts of CUPID

- Composable Architecture
  ```python
  import cupid

  # Define reusable components
  class DatabaseComponent(cupid.Component):
      def setup(self):
          print("Setting up database component.")

  class WebServerComponent(cupid.Component):
      def setup(self):
          print("Setting up web server component.")

  class LoggingComponent(cupid.Component):
      def setup(self):
          print("Setting up logging component.")

  # Create a CUPID system
  system = cupid.System()

  # Add components to the system
  system.add_component(DatabaseComponent())
  system.add_component(WebServerComponent())
  system.add_component(LoggingComponent())

  # Start the system
  system.start()
  ```

- Unix Philosophy
  - Understanding the principles of Unix design, such as modularity, simplicity, and composability.
  ```python
  # Example: Unix Philosophy
  # Using pipes to compose Unix commands
  import subprocess

  output = subprocess.run(["ls", "-l"], capture_output=True)
  print(output.stdout.decode())
  ```

- Predictable Behavior
  -  Ensuring consistent and deterministic behavior of CUPID-based systems under various conditions.
  ```python
  # Example: Predictable Behavior
  # Writing unit tests for a CUPID component
  import unittest
  import cupid

  class TestPredictableBehavior(unittest.TestCase):
      def test_addition(self):
          calculator = cupid.Calculator()
          result = calculator.add(2, 3)
          self.assertEqual(result, 5)

  if __name__ == '__main__':
      unittest.main()
  ```

- Ideomatic Design
  - Embracing standard practices and conventions in Unix system design for clarity and consistency.
  ```python
  # Example: Ideomatic Design
  # Following PEP 8 style guide in CUPID code
    def greet(name):
        """
        Greets the user by name.
        """
        print(f"Hello, {name}!")

    greet("Alice")
  ```

- Domain-specific Customization
  - Tailoring CUPID-based systems to specific use cases and domains for optimal performance and flexibility.
  ```python
  # Example: Domain-specific Customization
  # Customizing a web server component in a CUPID system
  import cupid

  web_server = cupid.WebServer()
  web_server.configure(port=8080, ssl=True)
  web_server.start()
  ```
