# Sambar/LeBar/k8or Codebase Naming Convention

This document summarizes the naming convention for various programming elements within the Sambar/LeBar/k8or codebase. Consistent and descriptive naming enhances code readability and maintainability.

## Content

1. **[Namespace Naming Convention](#Namespace-Naming-Convention)**
2. **[Class Naming Convention](#Class-Naming-Convention)**
3. **[Function Naming Convention](#Function-Naming-Convention)**
4. **[Method Naming Convention](#Method-Naming-Convention)**
5. **[Property Naming Convention](#Property-Naming-Convention)**
6. **[Document Metadata](#Document-Metadata)**

<h1 id="Namespace-Naming-Convention">Namespace Naming Convention</h1>

**Definition:** A namespace is a declarative region that encapsulates identifiers, providing a scope for elements such as types, functions, and variables. It serves as an organizational mechanism within codebases, preventing naming conflicts that can arise from multiple code components or external libraries utilizing identical identifiers.

**Purpose:** Defines a hierarchical structure within the codebase.

**Type case:** `PascalCase`. 

**Pascal Case** is a naming convention in programming where:

* The first letter of every word in a compound identifier is capitalized.
* There are no spaces or other characters between words.

**Major Languages with Namespaces:**

* **C++:** One of the earliest languages to introduce namespaces. It uses the `namespace` keyword to define them.
* **Java:** Namespaces are implicitly defined by package structures.
* **C#:** Similar to Java, uses namespaces for organizing code.
* **Python:** Uses modules as a form of namespaces.
* **JavaScript:** Introduced namespaces through the ES6 module system.
* **PHP:** Supports namespaces since version 5.3.
* **Ruby:** Uses modules as a namespace-like mechanism.
* **Go:** Employs packages for organizing code.
* **Rust:** Uses modules for namespaces.

| Component | Type       | Description                                               | Example   |
| --------- | ---------- | --------------------------------------------------------- | --------- |
| Company   | Noun       | Indicates the organization owning the namespace codebase. | Sambar    |
| NSP       | Classifier | Classifies the resource as a namespace.                   | NSP       |
| Example   | -          | Complete namespace name structure                         | SambarNSP |

<h1 id="Class-Naming-Convention">Class Naming Convention</h1>

**Definition:** A class serves as a blueprint or template, defining the attributes and behaviors shared by a group of objects. It encapsulates the structure and potential actions of entities within a system. An object, in contrast, is a concrete instantiation of a class. It possesses specific values for the attributes defined within its corresponding class and can execute the methods associated with that class. Essentially, objects are instances of classes, each representing a unique entity with its own state and behaviors.

**Purpose:** Represents a blueprint for creating objects.

**Type case:** `PascalCase`. 

**Major Class-Based Languages:**

* **C++**
* **Java**
* **C#**
* **Python** (introduced in Python 2.2)
* **PHP**
* **Ruby**
* **Objective-C**
* **Swift**
* **TypeScript**

| Component            | Type       | Description                                  | Example           |
| -------------------- | ---------- | -------------------------------------------- | ----------------- |
| SpecificClassPurpose | Noun       | Indicates the specific purpose of the class. | InvitationCode    |
| CLS                  | Classifier | Classifies the resource as a class.          | CLS               |
| Example              | -          | Complete class name                          | InvitationCodeCLS |

<h1 id="Function-Naming-Convention">Function Naming Convention</h1>

**Definition:** A function is a self-contained block of code that performs a specific task. It's designed to be reusable, meaning it can be called multiple times from different parts of a program.

**Purpose:** Defines a reusable block of code to perform a specific task.

**Type case:** `CONSTANT CASE` with `camelCase`. 

**Constant Case** is a naming convention where all letters are uppercase, and words are separated by underscores.

**CamelCase** is a naming convention where multiple words are combined without spaces or punctuation, and each word (except the first) starts with a capital letter. It's named after the "humps" formed by the uppercase letters, similar to a camel's back.

**Major Function-Based Languages:**

* **C**
* **C++**
* **Java**
* **Python**
* **JavaScript**
* **C#**
* **Ruby**
* **PHP**
* **Go**
* **Others**

| Component          | Type       | Description                                     | Example                   |
| ------------------ | ---------- | ----------------------------------------------- | ------------------------- |
| VERB               | Verb       | Indicates the action performed by the function. | VALIDATE                  |
| specificVerbTarget | Noun       | Indicates the specific target of the function.  | invitationCode            |
| FUN                | Classifier | Classifies the resource as a function.          | FUN                       |
| Example            | -          | Complete function name                          | VALIDATEinvitationCodeFUN |

<h1 id="Method-Naming-Convention">Method Naming Convention</h1>

**Definition:** A method is a function associated with an object. It defines the behavior or action that an object can perform. In essence, it's a procedure that operates on the data contained within an object.

**Purpose:** Defines an action performed on an object.

**Type case:** `camelCase`.

**Major Method-Based Languages:**

* **Java**
* **C#**
* **Python**
* **JavaScript**
* **Ruby**
* **Swift**
* **Objective-C**
* **C++**

| Component        | Type       | Description                                         | Example          |
| ---------------- | ---------- | --------------------------------------------------- | ---------------- |
| verb             | Verb       | Indicates the action performed by the method.       | get              |
| SpecificVerbData | Noun       | Indicates the specific data involved in the method. | LeBarTotal       |
| MTH              | Classifier | Classifies the resource as a method.                | MTH              |
| Example          | -          | Complete method name                                | getLeBarTotalMTH |

<h1 id="Property-Naming-Convention">Property Naming Convention</h1>

**Definition:** A property is a special kind of class member that provides a flexible mechanism to read, write, or compute the value of a private field.

**Purpose:** Represents a data attribute associated with an object.

**Type case:** `Prefix` with `camelCase`. The `$_` prefix is commonly used in PHP to indicate a private property.

A **prefix** is a character or group of characters placed at the beginning of a word or identifier. In this case, the `$_` prefix is used in PHP programming language to indicate a private property.

**Major Property-Based Languages:**

* **C#**
* **Java**
* **Python**
* **JavaScript**
* **Ruby**

| Component        | Type       | Description                              | Example           |
| ---------------- | ---------- | ---------------------------------------- | ----------------- |
| $_               | Symbol     | Indicates a private property.            | $_                |
| propertyDataType | Noun       | Indicates the data type of the property. | emailAddress      |
| PRP              | Classifier | Classifies the resource as a property.   | PRP               |
| Example          | -          | Complete property name                   | $_emailAddressPRP |

<h1 id="Variable-Naming-Convention">Variable Naming Convention</h1>

**Definition:** A variable is a named storage location used to hold data within a computer program. It's like a container that can store different values of various data types (numbers, text, etc.). These values can be changed throughout the program's execution.

**Purpose:** Represents a named storage location for data within the code.

**Type case:** `Prefix` with `camelCase`.

A **prefix** is a character or group of characters placed at the beginning of a word or identifier. In this case, the dollar sign (`$`) is used to indicate a variable in PHP programming language.

**Major Variable-Based Languages:**

* **C**
* **C++**
* **Java**
* **Python**
* **JavaScript**
* **C#**
* **Ruby**
* **PHP**
* **Go**
* **Others**

| Component       | Type       | Description                            | Example          |
| --------------- | ---------- | -------------------------------------- | ---------------- |
| $               | Symbol     | Indicates a variable.                  | $                |
| variablePurpose | Noun       | Indicates the purpose of the variable. | databaseName     |
| VAR             | Classifier | Classifies the resource as a variable. | VAR              |
| Example         | -          | Complete variable name                 | $databaseNameVAR |

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Sambar/LeBar/k8or Codebase Naming Convention |
| | Description | This document summarizes the naming convention for various programming elements within the Sambar/LeBar/k8or codebase. Consistent and descriptive naming enhances code readability and maintainability. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 10, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |