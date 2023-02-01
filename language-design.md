_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates
are:

- Something you agreed with / resonates with your own experience
- Something you disagree with
- Something that is interesting, a new idea or perspective you'd like to remember
- Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

* "Thus I think that programming languages need to be more like the languages we
speak—but it might be good, too, if we were to use the languages we speak more in the
way that we now use programming languages." (Steele 1998)

I thought this quote was significant because it was the culmination of Steele building his own verbal language over the course of his talk. I really liked this structure - it was super unique and make me think a lot about what it takes to build a programming language from the ground up. I also thought this led to some funny moments in the paper - like having to describe a trademark as "the laws of marks of trade". Lastly, using shorter words reminded me of how Writ 1 emphasizes brevity over fancy prose. It was good to think back to this as I write my responses here!

* "You can’t please everyone so aim to displease everyone equally." (Bloch 2006)

I liked this quote a lot, because it really gets to the core of why software development can be so difficult. There are so many different end users out there, each with different use cases, as well as different expectations for what a programming language/API should be able to do. Bloch and Steele both seem to agree on a tightly constrained language from the original developers that end users can expand upon if they wish. 

* "The broad computer science academic community has not paid a tremendous amount of attention to programming language usability. I think that our discipline mostly uses anecdotes to argue about programming languages." (Pavlus 2012)

This quote really reminded me of all the language wars that go on in the computer science community. These debates are typically rooted in what a language can _do_ (and how fast it can do it), rather than what it is like to use. I agree with Stefik that more conversations about PL usability are needed, but not when people are only speaking from their personal experiences. I think that studies like Stefik's will be central to improving the usability of programming languages, and speaks to how these efforts must be interdisciplinary to succeed.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

When discussing how a language is designed, it's important to separate the perspectives of a first-time user of a language from someone who is fluent in it. In my opinion, well-designed languages need to be accessible for begineers while being feature-rich enough for power users to accomplish everything that the language sets out to enable. As Steele describes, well-designed languages are much more likely to be adopted by a community of programmers that will continue using it over the years, maybe even expanding upon if they so desire. 

On the other hand, poorly designed languages fail one or both of the above groups. One way that languages fail beginners is when they do not make intuitive decisions when it comes to syntax. A good example of this in in the _Fast Company_ article by Pavlus (with the core research done by Stefik), where Perl performs similarly to Randomo - a language where all the operators are random words - in usabilty for beginning programmers. Of course, many who are experienced in Perl would disagree that it is poorly designed, but poor experiences out the gate sandbag a language's future success. Poorly designed languages fail experienced users when they lack the mechanisms through which successful languages grow over time. For example, Steele mentions how APL was successful initially but lost its userbase due to its 'cathedral-like' design, where it was very hard for the community to improve the language.


---

**Question**

How might the themes of _Growing a Language_ relate to ideas from the Fowler reading?

**Response**

The Fowler reading stands in firm support of small and focused DSLs, where developers should "guard firmly against" any sort of unnecesary expansion. In _Growing a Language_, Steele sees such small languages as starting points for inevitable future expansion if the language is to succeed. While Fowler states that "a typical project might use half a dozen or so DSLs", Steele focuses on a single language that can get it all done. While they seem opposed, I think that these two perspectives can be unified somewhat. If one takes both of their readings to heart, you ought to design DSLs not with the intention to expand on them, but in the 'wrapper' manner described by Steele, such that the door is left open to do so if it really make sense.

---

**Question**

In what way is an API a language?

**Response**

Steele defines a language as "a vocabulary and rules for what a string of words might mean to a person
or a machine that hears them". I think that an API easily satisfies this definition. It should be fairly obvious that APIs have vocabularies, for they are coded just the same as any programming language. As a language, an API is in a unique position, for its purpose is to translate between two or more other languages. This means that its rule set is largely dictated by what the languages it is translating between need to work. However, the rules of DSLs are constrained in a similar way by the demands of the domain it is operating within. Finally, it's worth noting that many of the skills for designing a programming language are relevant for designing an API. Bloch outlines some of these: good documentation, intuitive syntax, choosing carefully what to include and what can be left to the user, and so on.

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

One big thing that Verou's blog post demonstrates about API design is that with such a tight design of the language (as suggested by Bloch), every little decision means a big deal to end users. However, what Verou does is smart: compile a bunch of different proposals for the syntax, then lean on the CSS community to vote and comment. One of the top comments was even a great suggestion of grayscale(lightness [, alpha])! Of course, the notion of "not being able to please everyone" rings true here. People have different intuitions for what is most natural. But I believe that this 'bazaar' approach (to borrow from Steele) to making tricky syntax choices is a smart one!

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:

> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
> [[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

I do not think that these two descriptions are at odds with each other, because both approaches went to different lengths in implementing human-inspired design. There is a major difference between changing how you name abstractions (the Quorum approach) versus making the cadence of code more human-like, as Cook describes. I think that this is due to a clear distinction between human languages and computer languages, that being the room for error. When you chat with another person, if you lack the words to explain something precisely, you can use other words to approximate what you mean, and the other person can intuit what you're getting at. The same is not true for computers! When it comes to vocabularies and the scope in which languages are processed, Steele puts it quite nicely: "next to English, all computer programming languages are small". I would definitely like to include natural language when I design my own DSLs in this class, but I will opt for the Quorum route of choosing the words that best describe what each operation in my language accomplishes. Messing with the syntax to make it more speech-like is not worth the effort, in my opinion.

---
