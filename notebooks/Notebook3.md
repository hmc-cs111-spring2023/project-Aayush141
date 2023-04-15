# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

I made some pretty big design changes.

Fluency, and allowing method chaining. For operators like "-", I ensured that they took in AND returned the unorderString type. By doing so, you can chain methods and you don't have to worry about it popping and out of uoString. 

I also added in "extension(s :String)" to, essentially, allow easy explicit conversion from String to either of the new types. 


var v1 = "hello world" u   <-- v1 will be an unorderedString. 

var v2 = "hello world"./ <---- v2 will be a PhonemicString.

So, you still have all the implicit conversions to get in and out of types, and so - if you use any of the new operators on string, it will automatically switch into the correct type and perform the operation. But, if you use an operator that is in both String and unorderedString, like "+", you can chose which route you want to go by using "u". 

u for unordered string is pretty straighfoward. / for phString is pretty cool because linguists already use / to denote an end of Phoneme and by putting "/" at the end, you not only allow linguists to denote a phoneme ending as they usually would, but it also calls the function to turn it into a phoneme. The function call itself is disguised as a design feature.  



A major shift was with the loop structures. Scala has "for(char <- String)" type loops already, and I wanted to extend these to the new types, and expand these to have more functionality to work with strings. 

New route: Just have broad for-loop structures. Intead of having any overly complicated set of control structures, I just decided to create one broad for loop 

I had already made a simple for-loop in class, as part of the puzzle. So, I built something similar this time. There are two key differences though. Firstly, the overloading. I used overloading to have loops with defaults. You can choose to define all three (i = 0, i < 10, i += 1), or you can have two (i < 10, i += 1) where the default is just "i = 0", or you can have (10) where the default is "i = 0 and i += 1" (single increment, with 0 indexing). I thought about the third option being (i < 10), but since most people would use "i <" each time, I decided to abstract that way and make things easer for the programmer by just having (10). They don't have to use this option, but since most of the remaining boiler plate code of for-loops is the same, "for(10)" is a convenient option to have. 

The second difference is the syntax. I used 2 parameter lists this time, instead of four.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

1 hour - planning, ideating, talking.
6 hours - coding.
1 hour - critiquing (inside and outside class)
2 hours - notebook.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Things went slightly differently this week versus my expectations. But, I am still happy with my progress. 
