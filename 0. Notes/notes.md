# `if` Statements and Control Flow

In programming, we have **conditional statements** that will make a decision based on a **condition** and choose to execute or skip a section of code. These conditions are boolean values, and are most often in the form of the **boolean expressions** that we covered in Unit 3 Section 1. It is important to understand that conditional statements have the ability to break our **control flow**, where the computer may no longer perform each and every line of code and could now potentially skip some given that conditions work out a certain way.

---

## `if` Statements

In Java, we can use an **`if` statement** to check a condition and decide whether or not to execute a section of code. If the **boolean condition** that the `if` statement checks is `true`, then the program will execute the next line(s) of code, whereas if it is `false`, it will skip them and move on in the program. Here is an example of this from the `NotesIf1.java` file for us to break down:

```java
if (true) {
    System.out.println("This only prints if true.");
}
System.out.println("This will print regardless of the if statement.");
```

We can see at the start here we have the keyword `if`, followed by the parentheses with the boolean value `true`, which is functioning as our **boolean condition**. Then, similar to the constructors/methods we've seen before, we have the curly braces `{` and `}` to denote what counts as *inside* the `if` statement. Anything between the two curly braces are subject to whether or not the boolean condition is `true`. In this case, since we wrote the value `true` for the boolean conditional, it does have to do what's inside of the curly braces and then move on to everything else, so we get the following output:

```
This only prints if true.
This will print regardless of the if statement.
```

We can see it ran the print statement inside the curly braces and then moved on to the lines of code after the curly braces to end up printing both statements. Here is a sample from the `NotesIf2.java` file that changes the boolean condition to `false`:

```java
if (false) {
    System.out.println("This only prints if true.");
}
System.out.println("This will print regardless of the if statement.");
```

This is otherwise identical to the first example, but since the boolean condition is false, we expect it to skip everything inside of the curly braces and only do things afterward, producing the following output:

```
This will print regardless of the if statement.
```

We can see in this output that it skips the print statement inside of the curly braces and only does the one after.

We will almost never actually write a boolean value inside an `if` statement, and instead would write some **relational operation** (see Unit 3 Section 1) that would calculate and result in a boolean value for the `if` statement to use. Here is a couple of examples from the `NotesIf3.java` file:

```java
int value1 = 20;
int value2 = 30;

if (value1 > value2) {
    System.out.println(value1 + " is greater than " + value2);
}
if (value1 < value2) {
    System.out.println(value1 + " is less than " + value2);
}
if (value1 == value2) {
    System.out.println(value1 + " is equal to " + value2);
}
```

In this code, we can see the values of the variables `value1` and `value2` and we know that some of the sentences like "20 is equal to 30" is not accurate, but the beauty of `if` statements means that just because we wrote the sentence in a print statement, doesn't mean that the sentence will actually get printed out. Our boolean conditions are going to protect us from printing out the wrong information if we set them up correctly:

```
20 is less than 30
```

We can see that when we run it, it only prints out correct sentences because our boolean conditionals prevent the `if` statement from being run when it shouldn't.

---

## Assignment

Now that you have gone through the notes for this section, you can check out the `Try.md` and `Try.java` files to try a short assignment using this material.
