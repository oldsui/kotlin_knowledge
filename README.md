# Kotlin Learn

### Using nullable variables
#####
Ref: https://stackoverflow.com/questions/34498562/in-kotlin-what-is-the-idiomatic-way-to-deal-with-nullable-values-referencing-o

The !! operator asserts that the value is not null or throws an NPE. This should be used in cases where the developer is guaranteeing that the value will never be null. Think of it as an assert followed by a smart cast.

The ? safe call operator returns null if the value to the left is null, otherwise continues to evaluate the expression to the right.

The ?: Elvis operator allows you to provide an alternative value when an expression to the left of the operator is null

```kotlin
val something: Xyz? = createPossiblyNullXyz()

// access it as non-null asserting that with a sure call
val result1 = something!!.foo()

// access it only if it is not null using safe operator, 
// returning null otherwise
val result2 = something?.foo()

// access it only if it is not null using safe operator, 
// otherwise a default value using the elvis operator
val result3 = something?.foo() ?: differentValue

// null check it with `if` expression and then use the value, 
// similar to result3 but for more complex cases harder to do in one expression
val result4 = if (something != null) {
                   something.foo() 
              } else { 
                   ...
                   differentValue 
              }

// null check it with `if` statement doing a different action
if (something != null) { 
    something.foo() 
} else { 
    someOtherAction() 
}
```
#####


### Singleton
##### 
Ref: https://gist.github.com/ademar111190/de7c5fdc4a7ba29d8f5c
```kotlin
public object MySingleton {
  public fun foo() {
  }
}

// use it on Kotlin
MySingleton.foo()
```


Using Singletons in Java 7
```java
public class MySingleton {
  private static MySingleton instance;
  private MySingleton() {
  }
  public static MySingleton getInstance(){
    if(instance == null) {
      instance = new MySingleton();
    }
    return instance;
  }
  public void foo() {}
}

//Use it in Java
MySingleton.getInstance().foo()
```
#####
