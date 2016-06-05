# AdaLearning Ch1L1
Let's first take a look at an example Ada program.
```
with Sqrt, Simple_IO;

procedure Get_Square_Root is
    use Simple_IO;
    X: Float;
begin
    Get(X); -- Get the value for Float variable X from stdin
    Put(Sqrt(X)); -- Output the sqrt of it using stdout
end Get_Square_Root;
```
Wow, lots of stuff! Let's break down and go right into the details.

First of all, any random programmer might notice now that the way of commenting is different in Ada, than in most C-derived languages. Ada employs the use of `--`, where the comment begins after it, on the same line. In short, the effect of `--` is the same as `//` in Java or C++.

Secondly, a Java or Python programmer might also notice that Ada organizes code in a slightly different fashion, that there isn't classes and methods here. To explain this, let's rewrite the above Ada code in a Java fashion:

```
public static void Get_Square_Root() {
    float X;
    Scanner s = new Scanner();
    X = s.hasNextFloat();
    System.out.println(Math.sqrt(X));
}
```
Notice that using the Ada style naming in Java isn't the best practice; it is used simply for comparability here. Back to the topic: One can see that `procedure` in Ada is similar with a method in Java or any other similar OOP; It's useful to note that a procedure contains **no returns** whereas functions also exist in Ada. This often leads to confusion in beginners who have no experiences with a Pascal-like language and a more detailed explanation, covered later in this chapter, can be found in Ch1L3. One can also see that Ada seperates the declaration and the actual expression, that is, all variable declarations are handled between `procedure` and `begin`, but not after `begin`. After `begin` exists solely the operations being done on the given variables. This unique organization, as you will later see, is one of the main advantages for Ada in programming, as it promotes sensibility and readability.

Another thing to notice is that Ada, unlike the C-derived languages, does not use the `==` operator. Aiming to be more mathmatically-precise, Ada uses `:` for value assignment and `=` for comparing variables. This practise is more similar to what is used in mathmatics, pseudocode, and proves: `:=` and `=`. This shows that Ada is designed to be mathmatically robust, providing huge benefits for mission-critical applications where specific proving is needed. More sophisticated languages built on Ada, e.g. Spark, provides better access to such needs.

Finally, let's go through an official introduction of the Ada OOP style. Ada breaks programs down into subunits. A main program is among one of the subunits. In actual execution, procedures, organized into packages, can reference other procedures in other packages, just as methods in java referencing other methods inside other classes. In order to do so, an `import` in Java is needed; the same needs to be done in Ada. On the top of the example code, we can see that there's a line `with Sqrt, Simple_IO`. This means importing the two packages to the package we're in. The fun thing happens in the `Get_Square_Root` procedure, however. One can see that in order to use `Simple_IO`, a declaration of `use Simple_IO` is needed, while there isn't such line as `use Sqrt()`. This is similar to the difference of `static` and `nonstatic` in Java, which we'll cover later.

There's one last thing to note - some common styles for writing Ada programs. Since in Ada, all preserved keywords - `begin`, `procedure`, `use`, `is`, `end` etc, are written in lowercase letters - Uppercase Letters Are Used For Variable Names - E.g. `Salary`, `Month`, `I`, `X`, and also procedure names - `Get_Monthly_Salary`. However, note that Ada programmers do not use the traditional little camel naming method - A name shall be written as `Get_Monthly_Salary` instead of `GetMonthlySalary`. Of course, this practice is intended to promote readability in programs, which is what Ada aimed for - readability, maintainability along with integrity.

Ada OOP is very different comparing with other languages. A more detailed intro can be found in Chapter 2.
