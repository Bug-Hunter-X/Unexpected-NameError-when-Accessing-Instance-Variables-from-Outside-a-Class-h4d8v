# Ruby Instance Variable Access Bug

This repository demonstrates a common but subtle error in Ruby related to accessing instance variables from outside the class definition.  Attempting to directly access an instance variable from outside its class will result in a `NameError` unless you use methods like `instance_variable_get`.

The `bug.rb` file shows the problematic code, while `bugSolution.rb` offers a corrected version.

## Bug Description
Directly accessing an instance variable (@value) from outside the class where it's defined leads to a `NameError`. This occurs because the instance variable's scope is limited to the class's methods and can not be accessed globally or from outside the class's context.