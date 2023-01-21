# JS

# 목차

1. [Class와 Object](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
2. [Document Inherit](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
3. DOM, [EventTarget, Node, Element](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
4. [The difference between using `className`and `classList`](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
5. [What does classList.toggle do?](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
6. [Interface VS Class](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)
7. [Private VS Public In Class](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

# [1. Class, Instance, Object](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- Class
    - 클래스는 속성과 행위로 구성된 일종의 설계도이다.
- Instance
    - 클래스 구조로 컴퓨터 저장 공간에 할당된 실체이다.
- Object
    - 객체는 클래스와 인스턴스가 포함된 개념이다.

# [2. Document Inherit](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- 문서 상속은 객체와 클래스의 개념을 살펴보면 이해하기 쉽다. 객체는 클래스와 인스턴스를 포함한 개념이다. 따라서 클래스에서 정의된 속성과 행위를 상속받는다.
- 또, 객체는 클래스 구조를 지닌 구체적인 실체이다. 그러므로, 기본적으로 클래스 구조를 포함하는 것과 동시에 추가 속성과 행위를 가질 수 있다.

# [3. EventTarget, Node, Element](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- DOM(Document Object Model)
    - 브라우저의 웹페이지를 나타낸다.
- EventTarget
    - 이벤트를 수신하고 이벤트 수신기를 가질 수 있는 객체를 나타내는 웹 API의 인터페이스입니다. 일반적으로 브라우저의 웹 페이지를 나타내는 DOM(Document Object Model)에서 이벤트를 처리하는 데 사용됩니다. EventTarget 인터페이스를 구현하는 개체는 이벤트 수신기를 연결할 수 있으며, 이는 개체에서 특정 이벤트가 발생할 때 호출됩니다.
- Node
    - DOM의 단일 노드를 나타내는 웹 API의 인터페이스입니다. DOM은 웹 페이지의 구성과 내용을 나타내는 **트리와 같은 구조**입니다. DOM의 각 노드는 요소, 텍스트, 주석 또는 다른 유형의 노드일 수 있습니다. 노드 인터페이스는 상위 노드와 하위 노드, 내용 및 속성과 같은 DOM의 노드와 상호 작용하기 위한 속성과 방법을 제공합니다.
        - Tree란?
            
            트리는 컴퓨터 과학과 프로그래밍에서 일반적으로 사용되는 데이터 구조이다. 트리는 각 노드가 하나 이상의 하위 노드를 가질 수 있지만 최상위 노드인 루트 노드를 제외하고 상위 노드가 없는 하나의 상위 노드만 가질 수 있는 노드 모음입니다.
            
            DOM(Document Object Model)의 컨텍스트에서 트리는 웹 페이지의 구성과 내용을 나타내는 데 사용됩니다. 트리의 각 노드는 웹 페이지의 요소, 텍스트, 주석 또는 다른 유형의 노드를 나타낼 수 있습니다. 트리의 루트 노드는 전체 웹 페이지를 나타내고 하위 노드는 웹 페이지의 요소와 내용을 나타냅니다. 각 하위 노드는 고유한 하위 노드를 가질 수 있으며, 계층 구조를 만들 수도 있습니다.
            
            이러한 계층 구조를 통해 웹 페이지를 효율적으로 조작할 수 있는데, 이는 특정 요소를 쉽게 탐색하고 찾을 수 있게 해주며, 트리를 가로질러 여러 요소의 속성을 한 번에 변경할 수도 있기 때문이다.
            
            트리 데이터 구조는 컴퓨터 과학, 수학, 언어학 등과 같은 다양한 분야에서 사용될 수 있다. 파일 시스템, 조직 구조, 의사 결정 트리 등과 같은 계층적 데이터를 나타내기 위해 널리 사용되는 데이터 구조입니다.
            
- Element
    - DOM의 요소 노드를 나타내는 웹 API의 인터페이스이다. 요소는 HTML 또는 XML 요소를 나타내는 특정 유형의 노드입니다. 요소 인터페이스는 태그 이름, 특성 및 내용과 같은 요소와 상호 작용하기 위한 속성 및 방법을 제공합니다. 요소는 노드 유형이기 때문에 요소 인터페이스는 노드 인터페이스에서 속성과 메서드를 상속하며 요소와 관련된 추가 속성과 메서드도 가지고 있습니다.

# [4. The difference between using className and classList](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- Both **`className`** and **`classList`** are properties of DOM elements that allow you to access and manipulate the class attributes of an element. However, there are some differences in how they work and what you can do with them.
- **`className`** is a property that gets or sets the class attribute of an element as a string. You can use the **`className`** property to set or get the entire class attribute of an element, which contains all the class names separated by spaces.
- Here's an example of how you can use the **`className`** property to get and set the class attribute of an element:

```

let element = document.querySelector("#my-element");

// get the class attribute
let classAttribute = element.className;
console.log(classattribute); // "highlight active"

// set the class attribute
element.className = "selected";

```

- On the other hand, **`classList`** is a property that returns a **`DOMTokenList`** object, which provides a more convenient way to manipulate the class attribute of an element. It allows you to add, remove, and toggle classes individually, without having to manipulate the class attribute string.
- Here's an example of how you can use the **`classList`** property to add, remove and toggle the class attribute of an element:

```

let element = document.querySelector("#my-element");

// add a class
element.classList.add("selected");

// remove

```

# [5. What does classList.toggle do?](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- The **`classList.toggle()`** method is a method of the **`classList`** property in the DOM API that allows you to toggle (add or remove) a specific class on an element.
- Here's an example of how you can use the **`classList.toggle()`** method:

```

let element = document.querySelector("#my-element");
element.classList.toggle("highlight");

```

- In this example, the **`querySelector()`** method is used to get a reference to an element on the web page with the ID of "my-element". The **`classList.toggle()`** method is then used to toggle the "highlight" class on that element. If the element already has the "highlight" class, it will be removed, if not, it will be added.
- You can also pass a second argument to the toggle method, a boolean, indicating whether the class should be added or removed, if it's not present.

```

element.classList.toggle("highlight", true); // the class "highlight" will be added
element.classList.toggle("highlight", false); // the class "highlight" will be removed

```

- This method is useful for changing the styling or behavior of an element on the web page depending on certain conditions in your JavaScript code.

# [6. Interface VS Class](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- Here's an example of an interface in JavaScript:

```jsx

// Defining an interface for a shape
interface Shape {
    area(): number;
}
```

- In this example, the **`Shape`** interface defines a single method called **`area()`** that takes no arguments and returns a number. Any class that implements this interface must have a method called **`area()`** that has the same signature (i.e., takes no arguments and returns a number).
- Here's an example of a class that implements the **`Shape`** interface:

```jsx

class Square implements Shape {
    constructor(private side: number) {}

    area() {
        return this.side * this.side;
    }
}
```

- In this example, the **`Square`** class implements the **`Shape`** interface by providing an implementation for the **`area()`** method. The class has a constructor that takes a single argument, **`side`**, which is used to calculate the area of the square in the **`area()`** method.
- Here's an example of how the interface and class can be used together:

```jsx

const mySquare = new Square(5);
console.log(mySquare.area());  // prints 25
```

- In this example, an instance of the **`Square`** class is created with a side length of 5, and the **`area()`** method is called on the instance, which returns 25 (5x5).
- It's worth noting that JavaScript does not have built-in support for interfaces, but the concept of interfaces can be emulated using the syntax.

# [7. Keyword Private VS Public In Class](https://www.notion.so/JS-77187841c5b44fb0b5f95141c5d9bf99)

- In the context of classes in JavaScript, the keywords **`private`** and **`public`** are used to define the accessibility of class properties and methods.
- **`public`**: Properties and methods that are declared as **`public`** are accessible from anywhere, both within the class and outside of it. This means that they can be accessed and modified by other objects, and also by the methods of the class itself.

```jsx

class MyClass {
  public myProperty = "Hello";
  public myMethod() {
    console.log("Hello World!");
  }
}
const myObj = new MyClass();
console.log(myObj.myProperty); // "Hello"
myObj.myMethod(); // "Hello World!"

```

- **`private`**: Properties and methods that are declared as **`private`** are only accessible from within the class. They cannot be accessed or modified by other objects or by the methods of the class.

```jsx

class MyClass {
  private myProperty = "Hello";
  private myMethod() {
    console.log("Hello World!");
  }
}
const myObj = new MyClass();
console.log(myObj.myProperty); // Error: Property 'myProperty' is private and only accessible within class 'MyClass'
myObj.myMethod(); // Error: Property 'myMethod' is private and only accessible within class 'MyClass'

```

- It's worth noting that JavaScript does not have a built-in support for private properties and methods, but you can use the naming convention for the properties and methods to indicate that they are intended to be private, and also use closures to limit the access to the private properties/methods.
- By using the private keyword, it's easier to maintain the code and to know which properties and methods are intended to be private and should not be accessed or modified from outside the class.

<aside>
💡 **How can we use the naming convention for the properties and methods to indicate that they are intended to be private?**

</aside>

# <1> prefixing Underscore _

- In JavaScript, there is no built-in support for private properties and methods, however, you can use naming conventions to indicate that certain properties and methods are intended to be private. One common convention is to prefix the name of a private property or method with an underscore (_).
- Here's an example of how you can use this convention to indicate that a property or method is intended to be private:

```jsx

class MyClass {
  _privateProperty = "Hello";
  _privateMethod() {
    console.log("Hello World!");
  }
}

```

- In this example, the properties and methods are prefixed with an underscore (_) to indicate that they are intended to be private. While this is not a strict way of making properties and methods private, it serves as a reminder to other developers and yourself that these properties and methods should not be accessed or modified from outside the class.
- It's worth noting that this naming convention is only a convention and does not actually prevent access to the properties and methods. It's up to the developer to use other techniques to limit the access to the private properties and methods, such as closures.

## *** <2> Closure

- A closure is a function that has access to variables in its parent scope, even after the parent function has finished executing. It is a way to "remember" the variables that were in scope at the time the function was defined, and to access them even when the function is invoked outside of that scope.
- A closure is created when a function is defined inside another function, and the inner function has access to the variables in the outer function's scope. The inner function can access those variables even after the outer function has finished executing and returned.

Here's an example of closure in JavaScript:

```jsx

function makeCounter() {
  let count = 0;
  return function() {
    return count++;
  };
}
let counter = makeCounter();
console.log(counter()); // 0
console.log(counter()); // 1
console.log(counter()); // 2
```

- Here's the step-by-step process of how this code runs:
1. The **`makeCounter`** function is defined, which creates a variable **`count`** and assigns it a value of 0.
2. Within the **`makeCounter`** function, another function is defined and returned, which increments the value of **`count`** by 1 and returns the new value of **`count`**.
3. The **`makeCounter`** function is invoked and its return value (the inner function) is assigned to the variable **`counter`**.
4. **`console.log(counter())`** is called, which invokes the inner function, which returns the value of **`count`** (0) and increments the value of **`count`** by 1.
5. **`console.log(counter())`** is called again, which invokes the inner function again, which returns the new value of **`count`** (1) and increments the value of **`count`** by 1 again.
6. **`console.log(counter())`** is called for the third time, which invokes the inner function for the third time, which returns the new value of **`count`** (2) and increments the value of **`count`** by 1 again.
- In this example, **`makeCounter`** function returns an inner function, which can access the **`count`** variable defined in the outer function. Even after the **`makeCounter`** function has finished executing, the inner function can still access and update the value of the **`count`** variable.
- Closures are a powerful feature of JavaScript that allows you to create private variables and methods, and also to create function factories, among other things.

---

- A closure is a function that has access to variables in its parent scope, even after the parent function has finished executing. You can use closures to limit access to private properties and methods in JavaScript.
- Here's an example of how you can use closures to create private properties and methods in a class:

```jsx

class MyClass {
  constructor() {
    let privateProperty = "Hello";
    this.getPrivateProperty = function() {
      return privateProperty;
    }
  }
}
const myObj = new MyClass();
console.log(myObj.privateProperty); // undefined
console.log(myObj.getPrivateProperty()); // "Hello"

```

- In this example, the **`privateProperty`** variable is defined within the constructor of the class, and is only accessible within the scope of the constructor. A public getter method **`getPrivateProperty`** is created which has access to the **`privateProperty`** variable via closure, so it's able to return its value.
- You can also use closures to create private methods in the same way, where the private method is defined within the constructor and returned as a function.

```jsx

class MyClass {
  constructor() {
    let privateMethod = function() {
      console.log("Hello World!");
    }
    this.executePrivateMethod = function() {
      return privateMethod();
    }
  }
}
const myObj = new MyClass();
myObj.privateMethod(); // Uncaught TypeError: myObj.privateMethod is not a function
myObj.executePrivateMethod(); // "Hello World!"

```

- In this example, the **`privateMethod`** function is defined within the constructor, and only accessible within