# zSoft_Interview

## Regarding the relationship between Hashmap and HashSet?

HashSet, HashMap, and HashTable work using a hashing technique. That means behind the scenes a unique code is generated called a hashcode that is used to distinguish between the different elements inside the collections.
Also, HashSet uses HashMap internally to store its object, whenever we create a HashSet object one HashMap object associated with it is also created, this HashMap object is used to store the elements you enter in the HashSet.

## Regarding the relationship between the TreeSet and TreeMap
+ Both TreeMap and TreeSet are used to save collections and collection of collections.
+ Java TreeSet class contains unique elements like HashSet.
+ Java TreeSet and TreeMap class doesn't allow null elements.
+ Both TreeMap and TreeSet are sorted.

## Regarding Generic Types

Object is the superclass of all other classes and Object reference can refer to any type object. These features lack type safety. Generics adds that type safety feature.
Here is and example of the usage of generic types:

Indented code

    public class GenericsExample<T> {

        private T userName;

        public void show1(T object){
            System.out.println(object);
        }

        public void show2(T object){
            System.out.println(object);
        }
    }
    
    public class Main {
        public static void main(String[] args) {
            GenericsExample<Integer> ge = new GenericsExample<Integer>();
            ge.show1(5);
            ge.show1("String"); // This line doesn't work because we have declared the main object Integer

            GenericsExample<String> ge2 = new GenericsExample<String>();
            ge2.show1("String");
            ge2.show1(2);
        }
    }

We can see that we can declare using the same class different instance types with generic types, the first one is of integer Type and the second is of String type.
I have used Java generics previously in Android dev when implementing the adapter design pattern, it is just that it has been a long time since I have used them, and I didn't use them that often lately.

## Regarding SOLID Concept

+ **S** Single Responsibility Principle, regarding this principle I have learned it and use it many times during my Internship. The main idea of this principle is that we never give a function a method more than one specific task.
+ **O** Open closed principle, Entities should be open to extension but closed to modification, I have not used this principle that much so far, or maybe i have used it unintentionally.
+ **L** Liskov substitution principle, I don't know this principle and I have not used it to what I remember, but the main idea of the principle is that objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.
+ **I** Interface segregation principle.
+ **D** Dependency Inversion principle, This principle is the same as the one Used in Spring framework in the IOC container, instead of having a tight dependency between classes by directly initiating using new, we use Annotation to declare beans and then give the task of charging dependencies to the framework.



