# Dart language codestyle guidelines

## Naming

### Types

UpperCamelCase should be used to name classes, enum types and type parameters.

 You should capitalize the first letter of each word and do not use underscores.

```dart
class SomelessWidget  { ... }

typedef Predicate<T> = bool Function(T value);
```

### Packages

Lowercase letters with underscore should be used when naming packages and libraries.

```dart
import 'library_name.dart';
```

### Methods & Variables

Lower Camel Case should be used to name variables and methods

```dart
var variableOne;
String variableTwo;

void loadMethodThreee() {

}
```

## Order of class members

- Private members of class should be located in the beginning of the class
- Public properties are on the second place
- Cunstructors are on the third place
- Public methods are on the fourth place

## Code formatting

- Dart already has a built-in formatting tool. You should use  ``dart format``

- You should avoid lines longer than 80 characters

- You should use curly braces for all flow control statements.

    ```dart
    if (true) {
        print('Always true');
    } else {
        print('Something is wrong...');
    }
    ```

## Unused callback variables

You should use  _, __, etc. for unused callback parameters

```dart
button.onTap((_,__) {
  print('Tap');
});
```

## Practical tips

- Use null check operator to check for null variables. It reduces lines of code and improves readability
  
    ``dart
    variable.isTrue ?? false``
- Use async/await keywords

    ``` dart
    function () async {
        var data = await loadData();
        // Do something…
    }
    ```

- You should prefer named parameters. They are less error prone and easier to read than positional parameters, optional or not.
- Define constants for magic numbers. They serve as documentation of the meaning of its value.
  
  ```dart
  const double pi = 3.14159;
  ```

- Use fat-arrow rather than block syntax. If handlers are multi-liners, create a function.
  
    ```dart
    numbers.forEach((element) => printSqrt(element.toDouble()));
    ```

- Avoid large functions and widgets
  - Split large function into smaller functions
  - Split large widget into multiple (private or reusable) widgets
- Comments
  - Use comments when the code is not self-explanatory
  - Prefer commenting why something is done, rather than how
- When importing, you should use relative paths instead of full paths
