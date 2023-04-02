# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

I received feedback and ideas about some of the new operators I could introduce, and maybe even an "if" statement structure. I had thought about a lot of these before, but it was still helpful to talk about it and explain it to my critique partners. Just talking and explaining helps clarify, and maybe even get new ideas from both sides. 

Other people's DSL implementation ideas were also helpful. On Monday we spoke about using excel spreedsheets, APIs, regex, and some other interesting implementation ideas which while I don't think I be using just yet - but helped me branch out my line of thinking.  And some of these ideas may be important in the future, if and when I run into issues and barriers with my own implementation.

Was it helpful in addressing the most pressing issues in your project?

I still have not run into pressing issues, since it is really only the first week of the project - but I look forward to future critique sessions. 

A couple ideas of mine are still abstract - and I was hoping to create a live list of operators and features I would like to add. This is would help grounding the project, and also help future critique sessions!

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

I added some very basic internal DSL implementations! A very barebones PhonemicString type, a very basic "=~" operator, and a very basic loop implementation. I can now build off of this. 

Outside of coding, I also focused on the other aspects of getting started with the project : picking a host language, picking an internal/external DSL approach, talking experts in the Domain, etc.

Picking a host language: 
![image](https://user-images.githubusercontent.com/79538073/229378181-51c31208-7ec9-48f8-9b51-bccfe7d5f405.png)

After a table analysis attached above, Scala came out the winner. 

Internal DSL: I chose the internal DSL route.

Domain Expert:
I also spoke to my Linguistics professor about the DSL class, and I mentioned something about Regex which she was thoroughly confused by. So I thought about that. I think regex implementations can be really important while working with strings, but it is really unintuitive. Aside from the features I already intended on adding, I am also thinking about adding some regex features in the language that are more "readable", usable and better designed. 


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Design decision: Currently my phonemic string looks like this: 

"/text here/"

And I think it would be more intuitive and concise if it looked like this instead: 

/text here/

The quotes are unnecessary and may confuse a Linguist (linguists use // anyways. Unlike programmers). It would also help differentiate the language from Scala, and differentiate the datatype from String. And make it more DSL-y by removing some flavor of the host language. 

This poses me with an implementation issue, because I do not know how to do this without external techniques which I am trying to avoid. 

This is a minor issue though, and I will not worry about it for next week. Currently, I would like to reach some of the milestones and then go into the nitty gritties of design. "/text here/" works for now.

Bigger picture: Currently, PLs have a string datatype that is just a string of characters. It is not intended to mirror language. It just contains a string of characters. This is unlike numeric datatypes, which actually allow you to do math with them. Introducing new datatypes to represent the diverse types of strings that Linguistics work with would greatly help abstract basic tasks that Linguists have to deal with while programming. 

**What questions do you have for your critique partners? How can they best help
you?**

What are some forms of String manupulation that you would like to see? I have some ideas, but the more the merrier! What are some operators I could add? Again, I have some ideas for operators specific to phonemic string - but I was looking for more. 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

4 hours experimenting in Scastie.

2 hours on picking a DSL and speaking to linguistics people I know, including my prof. 

90 minutes on filling on this notebook entry, and bringing all my material together. 

75 minutes on critiques (in class, and outside). 


**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

Pretty good! I got all the "getting off the ground" work done, including a skeleton code and scala experimentation in Scastie. I wasn't able to delve into some of the design aspects and decisions, but I will be doing that next week. 
