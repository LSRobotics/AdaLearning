#AdaLearning Ch1L3

##Difference between functions and procedures

It's somewhat crucial to address the difference between functions and procedures in Pascal-like languages including Ada, and to clarify a few confusing perks in the last few lessons.

Functions, as you know in common procedural and OOP languages, are simply functions (:P). They describe an action with feedback information, that is, function returns. Sometimes a function finds that the action it describes requires no specific information to be returned, so it returns, mostly, a `void`. This is categorized in C++ as

```
void someFunction() {
  return;
}
```
The `return` here, is the feedback process in which no specific information is involved. However it is crucial to know that although a return may not involve any information, every function has a feedback process, that is, `return`.

On the other hand, procedures require no such feedback action/process. Procedures is simply a bunch of codes doing some work, but with no feedback. A procedure can be seen as a function **without** returns. In Ada, a procedure is written as:

```
procedure Test_Procedure is

 -- ...
begin

end Test_Procedure;
```
 Whereas a function is written as:
 ```
 function Test_Function is
  returns Void;

begin
 return;
end Test_Procedure;
