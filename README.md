# Kotlin Learn

### Using Singleton on Kotlin

#### 
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
#### 
