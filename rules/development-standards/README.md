# Development Standards

This directory contains rules and guidelines for development standards and best practices.

## Rules

### Java Programming
- **Java 21 Programming** (`java21-programming-always.mdc`)
  - Modern Java development practices
  - Java 21 features and patterns
  - Performance optimization techniques
  - Best practices for Java applications

- **Java 11 Programming** (`java11-programming-always.mdc`)
  - Java 11 specific features
  - HTTP Client API usage
  - String and Collection improvements
  - File operation best practices

### Functional Programming (`functional-coding-practices.mdc`)
- Functional programming principles
- Immutable data structures
- Pure functions and side effects
- Functional design patterns

### Code Quality (`no-hardcoded-strings.mdc`)
- String management best practices
- Internationalization guidelines
- Configuration handling
- Resource management

## How to Use

### Quick Start Guide

1. **For New Projects**
   ```bash
   # 1. Choose Java Version
   - For Java 21: Review java21-programming-always.mdc
   - For Java 11: Review java11-programming-always.mdc
   - Set up your project with chosen Java version
   - Configure your IDE for Java features

   # 2. Apply Functional Programming practices
   - Read functional-coding-practices.mdc
   - Structure your code using functional patterns
   - Use immutable data structures

   # 3. Implement Code Quality standards
   - Follow no-hardcoded-strings.mdc
   - Set up internationalization
   - Configure resource management
   ```

2. **For Existing Projects**
   ```bash
   # 1. Review current codebase
   - Check Java version compatibility
   - Identify areas for functional improvements
   - Find hardcoded strings

   # 2. Apply rules incrementally
   - Start with critical components
   - Refactor gradually
   - Add tests for new patterns
   ```

### Practical Examples

1. **Java Version Features**
   ```java
   // Java 11
   var message = "Hello";
   var lines = Files.readString(path).lines()
       .filter(line -> !line.isBlank())
       .collect(Collectors.toList());

   // Java 21
   var message = "Hello";
   var lines = Files.readString(path).lines()
       .filter(Predicate.not(String::isBlank))
       .toList();
   ```

2. **Functional Programming**
   ```java
   // Before
   public void processData(List<Data> dataList) {
       for (Data data : dataList) {
           data.setProcessed(true);
           saveToDatabase(data);
       }
   }

   // After
   public void processData(List<Data> dataList) {
       dataList.stream()
           .map(data -> data.withProcessed(true))
           .forEach(this::saveToDatabase);
   }
   ```

3. **No Hardcoded Strings**
   ```java
   // Before
   String message = "User not found";

   // After
   String message = ResourceBundle.getBundle("messages")
       .getString("error.user.not.found");
   ```

## Best Practices

1. **Code Organization**
   - Keep related functionality together
   - Use clear package structure
   - Follow single responsibility principle

2. **Testing**
   - Write unit tests for all new code
   - Include integration tests
   - Test edge cases

3. **Documentation**
   - Document public APIs
   - Include usage examples
   - Keep documentation up to date

## Common Pitfalls

1. **Avoid These Mistakes**
   - Mixing imperative and functional code
   - Using mutable state unnecessarily
   - Hardcoding configuration values
   - Ignoring Java version features

2. **Solutions**
   - Plan architecture before coding
   - Use configuration management
   - Leverage modern Java features
   - Follow functional principles

## Tools and Resources

1. **Recommended Tools**
   - IntelliJ IDEA or VS Code
   - Maven or Gradle
   - JUnit 5
   - Checkstyle

2. **Learning Resources**
   - Java Documentation (11 & 21)
   - Functional Programming Guides
   - Code Quality Tools Documentation

## Need Help?

1. **Getting Started**
   - Read the rule files thoroughly
   - Start with small changes
   - Ask for code reviews

2. **Troubleshooting**
   - Check common pitfalls
   - Review error messages
   - Consult team members

3. **Best Practices**
   - Follow examples in rule files
   - Use provided templates
   - Maintain consistency

## Usage

These rules should be followed for all new development work and when maintaining existing code. They ensure:
- Consistent coding standards
- Modern development practices
- Maintainable and scalable code
- High-quality output 