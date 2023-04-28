# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

I had lots of ideas, but they were disorganized and sometimes abstract. I planned to create a list with all the types, operators an flow control stuctures - and I was told by my critique partner to organize it all in a spreadsheet, ranked by importance and order of implementation. I actually did that this week! It is a live sheet, that is subject to change - but I do think the sheet has helped ground the project and gave me clear direction for the rest of the week. I will also be sharing the sheet with my critique partners so that they can give suggestions and ideas for for other implementations. The sheet gives clear basis for me, and my critique partners to work with. 

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

Exciting milestones: I actually met all the "base" milestones I wanted to meet for the project. I created UnorderedString and PhonemicString. I implemented several operators, such as - subset, superset, minus, genral string operations, equals and equalsdistinct for UnorderedString -- AND toXcase, toIPACase, =~, length for PhonemicString. I also implemented the loop. Last week, I only had a barebones structure for only PhonemicString and the loop - and now I have actually functioning strings with several implemented functions, operators and flow control structures for two of the three types. 

Beyond that, as mentioned, I also created a spreadsheet which specifies the three distinct types, and the functionality associated with each one.

![image](https://user-images.githubusercontent.com/79538073/230794237-7f391bd4-6353-43d8-aa84-9240bcaecdcb.png)

{screenshot of a portion of the spreadsheet! The sheet guided the aforementioned programming progress this week}

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

My largest issues are design. I knew design would be a bigger component of the project, and I need to make the language actually usable instead of what is now - just a series of implementations. 

Of course, I still have to add many more operators and functions and flow control structures, but I do think I have that aspect under control. Getting the design down is a more pressing issue now.

To move forward with design, I will be talking to my Linguistics Prof again - next week. Discuss what might be intuitive, and what might not. Then, I will be talking to Prof Ben about HOW to actually mold the current design to match the desired one. A lot of it, I feel like I know how to do or I can figure out myself. But some of it, such as the "/text here/" problem specied in my previous notebook entry, are harder and I may need some help. 

**What questions do you have for your critique partners? How can they best help
you?**

Some specific design ideas may require parsers and shifting(?) towards an external DSL. I was wondering if that might be the right direction.

And as last week, what are some forms of String manupulation that you would like to see? What are some operators I could add?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

4 hours on coding and implementation
3 hours on ideating, and creating a spreadsheet and coming up a proper, organised list of what I want to do. 
50 minutes on filling on this notebook entry, and bringing all my material together. 
70 minutes on critiques (in class, and outside).

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Pretty great! I wanted to have a few working datatypes with implicit conversions(in and out), operators, functions, flow control, etc. - and I got that! I need to now bend Scala a bit to get the desired design, or implement a parser for certain design ideas. 
