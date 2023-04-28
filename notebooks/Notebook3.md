# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

My partner suggested I add in some error handling for the new functions, and I agreed with that critique. However, I was more caught up in the design this week. So I will be adding in error handing next week. Some functions like "-" especially suffer from a lack of "what to do under bad conditions". For instance, if you subtract "abc" from "ab", the program will not know what to do since "abc" is bigger. I will be working to fix this, and issues like these. 

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

I made some pretty big design changes.


*Chapter One:*

Fluency, and allowing method chaining. For operators like "-", I ensured that they took in AND returned the unorderedString type. By doing so, you can chain methods and you don't have to worry about it popping out of unorderedString. 


*Chapter Two:*

I also added in "extension(s :String)" to, essentially, allow easy conversion from String to either of the new types. To denote which type you want, explicitly. (Without having to do the whole "unorderedString("hello world");")

var v1 = "hello world" u   <-- v1 will be an unorderedString. 

var v2 = "hello world"/ <---- v2 will be a PhonemicString.

So, you still have all the implicit conversions to get in and out of types, and so - if you use any of the UnorderedString operators on string, it will automatically switch into the correct type and perform the operation. But, if you use an operator that is in both String and unorderedString, like "+", you can chose which route you want to go by using "u". I have also added an implicit conversion to String, so you can use String operators on UnorderedString and it will pop into String, do the operation, and pop back into unorderedString.

On the design decision,

"u" for unordered string is pretty straighfoward and obvious. It is like "d" for double or "r" for regex. "/" for phString is pretty cool because linguists already use "/" to denote an end of Phoneme and by putting "/" at the end, you not only allow linguists to denote a phoneme ending as they usually would, but it also calls the function to turn it into a phoneme. The function call itself is disguised as a design feature.  


*Chapter Three*

A big design shift I made was with the loop structures. Scala has "for(char <- String)" type loops already, and I wanted to extend these to the new types, and expand these to have more functionality to work with strings in general. 7 or 8 new control structures just for looping.

New route: Just have one broad for-loop structure. Instead of having any overly complicated set of control structures, I just decided to create one broad for loop. "for (i = 0, i < x; i++)" style for loops can allow you to do essentially any kind of repition, and that is what I decided to add into the language. Some overloading allows the for loop to be even easier and more intuitive to be used. 

I had already made a simple for-loop in class, as part of the puzzle. So, I built something similar this time. There are two key differences though. Firstly, the overloading. I used overloading to have loops with defaults. You can choose to define all three (i = 0, i < 10, i += 1), or you can have two (i < 10, i += 1) where the default is just "i = 0", or you can have (10) where the default is "i = 0 and i += 1" (single increment, with 0 indexing). I thought about the third option being (i < 10), but since most people would use "i <" each time, I decided to abstract that way and make things easer for the programmer by just having (10). They don't have to use this option, but since most of the remaining boiler plate code of for-loops is the same, "for(10)" is a convenient option to have. The user need not remember multiple loop keywords since all of them go under the same name. Because, overloading.

The second difference is the syntax. I used 2 parameter lists this time, instead of four. They are parameter LISTS, so I just had the first one have all three, as a list. (i = 0, i < 10, i += 1) {body}. (Instead of for_loop (i = 0) (i < 10) (i += 1) (body).)

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I am actually happy with the overall direction. Both weeks, I added a lot of operations, functions, abstractions, conversions, control structures, fluency, and DSL-yness and I would like to continue moving in this direction. I still have to add more functions, operators, DSLy-ness, control structures - to actually land at the desired goal of a well designed DSL. I have a good basis in terms of implementation and design to work on and, eventually, meet my goal.

My main pressing issue though, is that it still feels like a general language and not a DSL. But, as I keep changing and bending Scala each week - little by little, I hope it will be more like a DSL by the end.

**What questions do you have for your critique partners? How can they best help
you?**

What are some changes I can make to remove the flavor of the host language - Scala? In many ways, it already feels different. But in many ways, it is still feels like Scala with a lot of garnish on top. I was wondering what I could do to make it more domain specific and take out any non-essential Scala-ness from the language.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

1 hour - planning, ideating, talking.

6 hours - coding.

1 hour - critiquing (inside and outside class).

2 hours - notebook entry.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Things went slightly differently this week versus my expectations. But, I am still happy with my progress. I tried a lot of new things, and not all of it worked. And I had to bite the bullet and remove some old code - as I went a different direction in terms of the loop design. I also decided to axe the third datatype, and only have two - UnorderedString and PhonemicString.

But, despite this - I still made a lot of progress. This progress was just different from what I had expected. I added in more fluency, extended String, created a nice/big loop structure, and made a lot of design decisions that I intend to further add in.

I also have some new operation and function ideas that I have for these two types, that I will be putting in.

For next week, I also want to add in documentation for the DSL, and fill up the "read me".
