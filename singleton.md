Ref: https://gist.github.com/ademar111190/de7c5fdc4a7ba29d8f5c

Using Singleton on Kotlin
~~~
public object MySingleton {
  public fun foo() {
  }
}

// use it on Kotlin
MySingleton.foo()

~~~


Using Singletons in Java 7
~~~
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
~~~
