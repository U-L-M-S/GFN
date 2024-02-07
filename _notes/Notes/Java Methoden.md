---
tags: 
- java/method
links: 
reference: 
path: Tools
created: 2023-08-20 20:45
modified: 2023-08-20 20:45
---
## Java Methoden 

>Syntax
>accessModifier returnDateType methodName (parameters) throws exceptionList

access modifer kann `public`, `privated`, `protected`, `default`. Es hängt nur davon ab, vonwo man die Methode zugreifen möchte.

| public    | Anywhere in the program                                                     |
| --------- | --------------------------------------------------------------------------- |
| Private   | Within the class in which it is declared                                    |
| Protected | Within the class in which it is declared, and from subclasses of that class |
| Default   | Within the package in which it is declared                                  |
|           |                                                                             |

```java
public class AwesomeJavaProgram{
// A method that throws a `NullPointerException` if the object is null
	public void printName(String name) throws NullPointerException {
		if (name == null) {
		    throw new NullPointerException("The name cannot be empty");
		}
		System.out.println(name);
	}

}

```



