~~Didn't Dijkstra hates ts?~~

# Other paradigms
- procedural = fn/steps = c
- oop = java, cpp
- fn = fn & expr = Lisp
- logic = logic= prolog
# Programming Paradigms
## OOP history 
- introduced at MIT in 50s
- in 1980s C++ was unleashed.
- in early 90s, Java . 
## OOP?
- Paradigm based on idea of _**objects**_ that may contain data, in the form of fields (aka _**attributes**_) in the form of procedures aka _**methods**_
- aim is to bind the data & fn that operate on 'em do that no other part of code can access that data except that fn
### Attributes
- Properties/Data
- Like name, id
### Methods
- Behavior/fn
- like enroll(), takeexam()
### Why?
### Core concepts
- ***Encapsulaion***
	Making data hidden in other classes. Aka private   class
- ***Abstraction***
	Hiding the internal implementation details of something and show only the essential features that the user needs to work with
- ***Inheritance***
	Allows code reuse whenever possible, reducing redundancy
- ***Polymorphism***
	Allows same method name to behave differently depending on the caller object
## Java naming Conventions

| Element (e.g)                     | Conventions       |
| --------------------------------- | ----------------- |
| Class (OrderMgr)                  | PascalCase        |
| Method \[calculateSalary()]       | camelCase         |
| Variable (studentName.totalPrice) | ''                |
| Const (MAX_COUNT)                 | UPPER_SNAKE_ CASE |
| Package (com.company)             | lowercase         |
| Generic type \<T>                 | Single uppercase  |
# Class & Objects 

| Obj               | Cls                           |
| ----------------- | ----------------------------- |
| Instance of class | Definition of connected thing |


| Obj state | Obj behavior              |
| --------- | ------------------------- |
| Value     | Action def'd thru methods |

| Constructor                                   | Destructor                    |
| --------------------------------------------- | ----------------------------- |
| Member fn of class w/ same name as class name | Methods when obj is destroyed |

Destructor doesn't _exactly_ apply to java because it has garbage collection

## Instantation
Process of creating a real obj from a class template
- think of it as building from blueprint (class)
E.g,

```java
public class []{
[] s1, s2, s3;

[Constructor, same name as class](d.a, d.b, d.c){
s1 = a; s2 = b; s3 = c;


	public double perimeter(){
		
	}
}

}

```

