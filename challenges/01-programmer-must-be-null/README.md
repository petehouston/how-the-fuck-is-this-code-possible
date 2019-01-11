# 01. Programmer must be null.

Yeah, I mean it. Programmer should not be null, but in facts, we need **Programmer must be null**.

**It is customer's requirement!!!**.

So, one great fucking day, customers give us an awesome legacy, you get it!

```java
public class Programmer {
    final String name;

    public Programmer(String name) {
        this.name = name;
    }

    public String getName() {
        return this.name;
    }

    public static Programmer newInstance(String name) {
        return new Programmer(name);
    }

    public static void main(String... args) {
        Programmer awesomeProgrammer = new Programmer("Super Coder");
        System.out.println("[1] Programmer: " + awesomeProgrammer);

        if(awesomeProgrammer == null) {
            System.out.println("[2] Programmer: null");
        } else {
            System.out.println("[2] Programmer: NOT null...Thanks God!");
        }
    }
}
```

Our customers expect the following output:

```
[1] Programmer: null
[2] Programmer: NOT null...Thanks God!
```

Your task:

- Patch this code to meet customers' expectation.
- Don't ever touch or modify `main()` method, it's the core business logic. Super dangerous! You're warned!
- Just work inside `Programmer` class. Customers are really pro on `Open-Closed Principle`.