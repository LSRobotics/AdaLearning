# AdaLearning Ch1L2
Now that you have learnt how to write a short program, let's continue by adding some more sauce to it.

##if statements
In ada, if statements can be written as:
```
...
if X < 0.0 then
    Put('Not valid');
end if;
```
As you can see, the structure is controlled by `if` and `end if` with no exceptions.

##Loops
In ada, loops can be written as:
```
loop
    exit when X = 0.0;
end loop

```
This loop is equivalent to a while loop in C/Java:
```
while(X!= 0.0) {
 //
 }
```
Except in Ada you're able to control when `exit` is executed, whereas in most C-derived languages, you can only put such clause in either the beginning or the end.

##Difference between Procedures and functions

But how to write a procedure that returns a value? Let's take a look at a specific example:
```
with Simple_IO;
...
function Get_Shoe_Maker return String is -- returns the name of Shoe Maker received via stdin
    use Simple_IO;
    Shoe_Maker: String;
begin
  Get(Shoe_Maker);
  Put("The Shoe Maker's name is");
  New_Line;
  Put(Shoe_Maker);
  return Shoe_Maker;
end Shoe_Maker;
```
As it turns out, it's relatively simple! First off, you'll have to declare what is the datatype being returned (strong typing system!) Secondly, you return a data of the specific datatype whereever you want, therefore ending the procedure. Let's take a look at a synonymous Python program that does the same thing:

```
# @return String
def Get_Shoe_Maker():
  Shoe_Maker = input()
  print("Your shoe maker is\n")
  print(Shoe_Maker)
  return Shoe_Maker
```

Again, Python here, as you can see, does not have a static typing system, and on a large scale, makes everything vague.

##Example
Whew! We've already learnt alot! Let's take a look at this example:
```
procedure Get_Shoe_Maker return String is -- returns the name of Shoe Maker received via stdin
    use Simple_IO;
    Shoe_Maker: String;
begin
  loop
      Get(Shoe_Maker);
      Put("The Shoe Maker's name is");
      New_Line;
      Put(Shoe_Maker);
  end loop;
  return Shoe_Maker;
end Shoe_Maker;
```
