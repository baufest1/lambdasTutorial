# Documentation: Classes and Objects - Lambda Expressions

## Table of Contents

- [Classes and Objects](#classes-and-objects)
    - [Classes](#classes)
        - [Declaring Classes](#declaring-classes)
        - [Declaring Member Variables](#declaring-member-variables)
        - [Defining Methods](#defining-methods)
        - [Providing Constructors for Your Classes](#providing-constructors-for-your-classes)
        - [Passing Information to a Method or a Constructor](#passing-information-to-a-method-or-a-constructor)
    - [Objects](#objects)
        - [Creating Objects](#creating-objects)
        - [Using Objects](#using-objects)
    - [More on Classes](#more-on-classes)
        - [Returning a Value from a Method](#returning-a-value-from-a-method)
        - [Using the this Keyword](#using-the-this-keyword)
        - [Controlling Access to Members of a Class](#controlling-access-to-members-of-a-class)
        - [Understanding Class Members](#understanding-class-members)
        - [Initializing Fields](#initializing-fields)
        - [Summary of Creating and Using Classes and Objects](#summary-of-creating-and-using-classes-and-objects)
        - [Questions and Exercises (Classes and Objects)](#questions-and-exercises-classes-and-objects)
    - [Nested Classes](#nested-classes)
        - [Inner Class Example](#inner-class-example)
        - [Local Classes](#local-classes)
        - [Anonymous Classes](#anonymous-classes)
    - [Lambda Expressions](#lambda-expressions)
        - [Ideal Use Case for Lambda Expressions](#ideal-use-case-for-lambda-expressions)
        - [Approach 1: Create Methods That Search for Members That Match One Characteristic](#approach-1-create-methods-that-search-for-members-that-match-one-characteristic)
        - [Approach 2: Create More Generalized Search Methods](#approach-2-create-more-generalized-search-methods)
        - [Approach 3: Specify Search Criteria Code in a Local Class](#approach-3-specify-search-criteria-code-in-a-local-class)
        - [Approach 4: Specify Search Criteria Code in an Anonymous Class](#approach-4-specify-search-criteria-code-in-an-anonymous-class)
        - [Approach 5: Specify Search Criteria Code with a Lambda Expression](#approach-5-specify-search-criteria-code-with-a-lambda-expression)
        - [Approach 6: Use Standard Functional Interfaces with Lambda Expressions](#approach-6-use-standard-functional-interfaces-with-lambda-expressions)
        - [Approach 7: Use Lambda Expressions Throughout Your Application](#approach-7-use-lambda-expressions-throughout-your-application)
        - [Approach 8: Use Generics More Extensively](#approach-8-use-generics-more-extensively)
        - [Approach 9: Use Aggregate Operations That Accept Lambda Expressions as Parameters](#approach-9-use-aggregate-operations-that-accept-lambda-expressions-as-parameters)
        - [Lambda Expressions in GUI Applications](#lambda-expressions-in-gui-applications)
        - [Syntax of Lambda Expressions](#syntax-of-lambda-expressions)
        - [Accessing Local Variables of the Enclosing Scope](#accessing-local-variables-of-the-enclosing-scope)
        - [Target Typing](#target-typing)
        - [Target Types and Method Arguments](#target-types-and-method-arguments)
        - [Serialization](#serialization)
    - [Method References](#method-references)
    - [When to Use Nested Classes, Local Classes, Anonymous Classes, and Lambda Expressions](#when-to-use-nested-classes-local-classes-anonymous-classes-and-lambda-expressions)
        - [Questions and Exercises (Nested, Local, Anonymous, Lambda)](#questions-and-exercises-nested-local-anonymous-lambda)
    - [Enum Types](#enum-types)
        - [Questions and Exercises (Enums)](#questions-and-exercises-enums)
- [Home Page > Learning the Java Language > Classes and Objects](#home-page--learning-the-java-language--classes-and-objects)
- [« Previous](#previous)
- [• Trail](#trail)
- [• Next »](#next)
- [Important Notes](#important-notes)

* * *

## Classes and Objects

[Back to TOC](#table-of-contents)

### Classes

[Back to TOC](#table-of-contents)

#### Declaring Classes

[Back to TOC](#table-of-contents)

#### Declaring Member Variables

[Back to TOC](#table-of-contents)

#### Defining Methods

[Back to TOC](#table-of-contents)

#### Providing Constructors for Your Classes

[Back to TOC](#table-of-contents)

#### Passing Information to a Method or a Constructor

[Back to TOC](#table-of-contents)

### Objects

[Back to TOC](#table-of-contents)

#### Creating Objects

[Back to TOC](#table-of-contents)

#### Using Objects

[Back to TOC](#table-of-contents)

### More on Classes

[Back to TOC](#table-of-contents)

#### Returning a Value from a Method

[Back to TOC](#table-of-contents)

#### Using the this Keyword

[Back to TOC](#table-of-contents)

#### Controlling Access to Members of a Class

[Back to TOC](#table-of-contents)

#### Understanding Class Members

[Back to TOC](#table-of-contents)

#### Initializing Fields

[Back to TOC](#table-of-contents)

#### Summary of Creating and Using Classes and Objects

[Back to TOC](#table-of-contents)

#### Questions and Exercises (Classes and Objects)

[Back to TOC](#table-of-contents)

### Nested Classes

[Back to TOC](#table-of-contents)

#### Inner Class Example

[Back to TOC](#table-of-contents)

#### Local Classes

[Back to TOC](#table-of-contents)

#### Anonymous Classes

[Back to TOC](#table-of-contents)

### Lambda Expressions

[Back to TOC](#table-of-contents)

One issue with anonymous classes is that if the implementation of your anonymous class is very simple, such as an interface that contains only one method, then the syntax of anonymous classes may seem unwieldy and unclear. In these cases, you're usually trying to pass functionality as an argument to another method, such as what action should be taken when someone clicks a button. Lambda expressions enable you to do this, to treat functionality as method argument, or code as data.

The previous section, Anonymous Classes, shows you how to implement a base class without giving it a name. Although this is often more concise than a named class, for classes with only one method, even an anonymous class seems a bit excessive and cumbersome. Lambda expressions let you express instances of single-method classes more compactly.

This section covers the following topics:

#### Ideal Use Case for Lambda Expressions

[Back to TOC](#table-of-contents)

#### Approach 1: Create Methods That Search for Members That Match One Characteristic

[Back to TOC](#table-of-contents)

#### Approach 2: Create More Generalized Search Methods

[Back to TOC](#table-of-contents)

#### Approach 3: Specify Search Criteria Code in a Local Class

[Back to TOC](#table-of-contents)

#### Approach 4: Specify Search Criteria Code in an Anonymous Class

[Back to TOC](#table-of-contents)

#### Approach 5: Specify Search Criteria Code with a Lambda Expression

[Back to TOC](#table-of-contents)

#### Approach 6: Use Standard Functional Interfaces with Lambda Expressions

[Back to TOC](#table-of-contents)

#### Approach 7: Use Lambda Expressions Throughout Your Application

[Back to TOC](#table-of-contents)

#### Approach 8: Use Generics More Extensively

[Back to TOC](#table-of-contents)

#### Approach 9: Use Aggregate Operations That Accept Lambda Expressions as Parameters

[Back to TOC](#table-of-contents)

#### Lambda Expressions in GUI Applications

[Back to TOC](#table-of-contents)

#### Syntax of Lambda Expressions

[Back to TOC](#table-of-contents)

#### Accessing Local Variables of the Enclosing Scope

[Back to TOC](#table-of-contents)

#### Target Typing

[Back to TOC](#table-of-contents)

#### Target Types and Method Arguments

[Back to TOC](#table-of-contents)

#### Serialization

[Back to TOC](#table-of-contents)

### Method References

[Back to TOC](#table-of-contents)

### When to Use Nested Classes, Local Classes, Anonymous Classes, and Lambda Expressions

[Back to TOC](#table-of-contents)

#### Questions and Exercises (Nested, Local, Anonymous, Lambda)

[Back to TOC](#table-of-contents)

### Enum Types

[Back to TOC](#table-of-contents)

#### Questions and Exercises (Enums)

[Back to TOC](#table-of-contents)

## Home Page > Learning the Java Language > Classes and Objects

[Back to TOC](#table-of-contents)

## « Previous

[Back to TOC](#table-of-contents)

## • Trail

[Back to TOC](#table-of-contents)

## • Next »

[Back to TOC](#table-of-contents)

## Important Notes

[Back to TOC](#table-of-contents)

The Java Tutorials have been written for JDK 8. Examples and practices described in this page don't take advantage of improvements introduced in later releases and might use technology no longer available.  
See Dev.java for updated tutorials taking advantage of the latest releases.  
See Java Language Changes for a summary of updated language features in Java SE 9 and subsequent releases.  
See JDK Release Notes for information about new features, enhancements, and removed or deprecated options for all JDK releases.


> *This is a quote*
