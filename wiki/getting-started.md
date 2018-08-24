 == [Class](https://github.com/hw-core/js-library-class/blob/master/Class.js) ==

### Getting started

    First of all, you've to configure your environment to run HWCore framework ( take a look at kernel [documentation](https://github.com/hw-core/js-kernel) )

    Now, there are 2 ways to define a class:

    [Basic syntax](#class-basic) ( faster performance but verbose and a little more complex )

    [Friendly syntax](#class-friendly) ( slower performance but less verbose and very friendly )

    This is an example using friendly syntax. Use links above for more details.  

    ![Code](https://lh4.googleusercontent.com/-Aq5KBz3V5f8/VH4u116weHI/AAAAAAAAAeQ/jch0BxfyEzU/w901-h692-no/js-class-typehint.png) 

### Current supported features

    *   Abstract class: Cannot be instantiated
    *   Static class: A class that has only static members and cannot be instantiated
    *   Final class: Cannot be extended
    *   Base/Extension: your object inherits all methods of extended class and they shares
            prototype that allows you to cast the instanceof succesfully
        
    *   Use: it's the mechanism of traits used also by other languages 
            that enables horizontal composition of behavior. in few words: 
            you can use methods from other objects. 
        
    
    
    *   Protected members: accessible only from its original class and childs
    *   Private members
    *   Public members
    
    *   Static members
    *   Final members: its value cannot be changed
    *   Type\-hinted members 

### Work in progress features

    *   Abstract methods
    *   methods override
    *   extend support for inner/nested classes
    *   Friend class: [wikipedia](http://en.wikipedia.org/wiki/Friend_class)
    *   Interfaces and templates to consider 

### Reserved words and "magic" methods

All magic methods starts with \_\_ prefix, so don't use this prefix for your variables name

 **Class public instance methods:**

    *   \_\_isClass
    *   \_\_construct: called at class instantiation
    *   \_\_destruct: this is just a pattern that calls all destroyers in chain. 
            It's not called at GC object deletion. It's not possible with javascript at the moment
    *   \_\_st: to call static methods from an instance
    *   \_\_inherit
    *   \_\_addMembers

 **Class public static methods**

    *   \_\_isClass
    *   \_\_getBase
    *   \_\_isChildOf
    *   \_\_addMembers
    *   \_\_getMembers
    *   \_\_isAbstract
    *   \_\_isStatic
    *   \_\_isFinal

 **Class methods scope reserved variables**

    *   this.i : to access public/protected instance members
    *   this.s : to access public/protected static members
    *   this.\_i : to access private instance members
    *   this.\_s : to access private static members
    *   this.\_\_super : to call parent method
    *   this.\_\_scope : the scope of function, internally used 

### Some class examples can be found here:

*   [Sample files](https://github.com/hw-core/js-library-class/tree/gh-pages/samples)
    *   [Test file](https://github.com/hw-core/js-library-class/blob/tests/tests/class.js)