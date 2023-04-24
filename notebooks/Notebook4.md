# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

Problem: The DSL still felt like Scala - the host language. The design was inconsistent, and the user often had to rely on and learn both - my DSL syntax, and Scala syntax. 

Suggestion: Write "test" code in the DSL, and notice things that bother you - and you would like to appear different. Things that would benefit from being different. Finally, create a cohesive design for the overall language. 

How it helped: I did just that this week! You can barely tell it is Scala anymore, and the design closely matches with linguistic operations. 

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

It looks and feel like a DSL! With a design centered around linguistic operations, and ease of use. 

Here is what happened:

I switched out a lot of the Scala syntax with new design features that matched the rest of the "operator" feel. 

The if-statement is basically function with two parameter lists in Scala. Instead of a function with two parameter lists, the implementation in the DSL is a function that is an extension of boolean and has one parameter. It looks like an operator, because it is. It is an entailment operator.

BOOLEAN -> BODY

var v1 = "hello"
("hello" == v1) -> (v1 = "bye")

//The body only runs if the boolean is true

The entailment operator "->" is already used by linguists for, well, entailment. if A then B.


The print statement syntax has been swapped out too. Again, in favor of operators and to match with the rest of the design.

"hello"↓

//prints "hello". 

Essentially, the linguist can do things like Input/Output - without having to know functions and how "println" works. The down arrow is just another operation. By having a uniform aesthetic, the linguistic need not know any other programming language as a prereq. They just need to know the operations like "+", "-", "->", "⊆", "/", "~", "↓". And since these match those that linguists already use, it should not be too hard to learn! (The print operation also has more functionality than regular print statements - in that you can chose the format of the print)

The loop matches this form of "variable first, single parameter" design:

10 times {

  body
  
}

(It is essentially "10.times(body)" with an extension (i: Int). The user is expected to use the above syntax though)

The for_loop from last week is still there, and provides more functionality. But, this is a simpler syntax and does most things a linguist would want. 

----

I also added some new extension functions to work with the new syntax. For instance, "(Unit) ln" will print a leave line. And "n lines" will print n leave lines. This is because the ↓ operator, by default, does not leave a line. But you can just tack on a "ln" or "n lines).

Beyond these changes, I also added error handling. Error messages in case things go wrong.

---

Finally, I also wasted more time than I should have on coming up with a name💀 I am really happy with the final name though. 

"PP++" is the name. It stands for "Palatal Plosive Plus Plus" 

Explanation:

- C, C++, C#, etc. There is a host of languages with C in them. For linguistics, "c" represents the "Palatal Plosive". 
So, "Palatal Plosive Plus Plus" essentially translates to "C++".

- Palatal Plosive Plus Plus is an alliteration. It is not just an alliteration, it is a second order alliteration. The first TWO consonents of each word is the same - "PL PL PL PL". Not only is it a second level alliteration, the first two letters "PL" stand for "Programming Language". Which is what this is! "Programming-Language Programming-Language Programming-Language Programming-Language". 

 
## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Nothing major, which is good seeing as we are approaching the end. Some minor tweaks, maybe add some more abstractions, organize my files. Some operations are still a little confusing, so maybe simplify them. Finalize my documentation and readme file.  

**What questions do you have for your critique partners? How can they best help
you?**

I feel like my DSL is ready! At the very least, there is a strong basis to work off of. I was wondering if my critique partners felt anything else was missing.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

2 hours - ideating, talking, planning, and more.

5 hours - coding

1 hour - coming up with a name for the language👀

2 hours - notebook

45 minutes - critique

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

It went great! The language design is appropriate for linguistics, is consistent, and is very different from the host language.
