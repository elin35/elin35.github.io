---
title: "Episode 5: First time Teaching"
date: 2023-8-14
---

I've been incredibly busy juggling life and mathematics and many things have happened since my last post. Research has been progressing slow and steady and I've felt a whirlwind of emotions on that topic from one month to another. I've had quite a few personal trips to travel and take a bit of a break from work and for the topic of this post, I was finally granted the opportunity to teach my own class this Summer. This will be the topic of this episode and I will save delving into research for the following post.

At UCR, our Summers are split into two short 5 week sessions, one which runs from the end of June to the end of July, and a following one which picks up there and runs until the end of August. Behind these is a long term Summer session which runs for 10 weeks, but this seems to be reserved for specific classes which I don't think I'll encounter. The 5 week sessions meet Monday through Thursday, so timewise, it is equivalent to the usual 10 week quarters, just condensed into 5 weeks.

I was given the opportunity to teach our Math/CS 11: Discrete Mathematics during session A of Summer 2023 here at UCR.

While I've been TAing for quite a while now at UCR, I have never had the chance to teach in any meaningful way and I would not consider the times I do have to lecture on a topic during discussion equivalent to teaching as I don't have to prepare nearly as much and it was usually just for a single week out of the quarter. Math departments in the US also generally don't have any kind of training on how to teach so my personal confidence and idea on how to teach came from the following sources:

- The first and most meaningful place where I got an idea of how I'd like to teach is just from being a student. I have my fair share of good and bad teachers, so from that I had a sense of what I would want as a student or what I wish teachers and mentors had done more of. It's tempting to desire that a teach does absolutely everything and spoon feeds the entire course, but I hopefully had a little more restraint than that.
- The next source comes from my time as a graduate student. More time is spent on the faculty side, so we get to see a bit of how the older faculty hold themselves while teaching and notice small details about things they do in their courses to promote teaching. We also see a lot of bad habits and poor practices, so there are good observations to be made from both sides of the coin.
- I've spent a few quarters in our education seminar led by Sara Lapan and we've had some good discussions about modern math education practices that I was interested in putting into practice. For example, active learning was a term that was thrown around constantly in the seminar and some of the readings helped me come up with other ideas about how mathematics at the undergraduate level can be taught in a less algorithmic and robotic way. 
- A large part of a mathematics course is the presentation of material. From reading several textbooks, attending lots of courses, and getting accustomed to mathematical writing, I came to develop my own style of how I like to see and present notes. I was hoping this would also be a well organized way to do so in lecture.
- This might also be quite important, but the way in which I speak about mathematics has developed quite a lot over the years. For example, given some topics in mathematics, it can be helpful to not always discuss it in a rigorous, technical manner, but instead to speak of it loosely in a more intuitive way. In some calculus discussions, I've found that when I use more friendly descriptive language (like calling things "big", "small", "fast", "slow") instead of more technicaly terms (like "convergence", "asymptotic", etc) that students pick up on a few of those intuitive ideas which in turn help them get a handle on the formal technical understanding of certain topics. 

General teaching practices aside, there is a lot to be said about the specific course I was given to teach, Math/CS 11. You'll notice that the subject is "Math/CS". This is due to discrete mathematics being crosslisted for mathematics majors as well as CS majors. In reality, it's mostly CS majors because there are very few mathematics majors, but that's beyond the point. This didn't necessarily pose a challenge as all the students are coming from more or less the same mathematical background, but it does make the topics of the course a little more interesting as there is a push to involve some algorithm analysis and pseudocode type exmples in the course. 

Another difficulty for the course is more of an issue with updating our departments standards as far as curriculum goes. Presumably, new professors (VAPs, postdocs, me) who are teaching the course and would like to know how UCR's math department tends to teach it would look at the official syllabus for the course. For courses like calculus, linear algebra, or differential equations, it's more or less standard across most schools in the US (this is almost certainly not true, but I want to believe that it's true). I've taken discrete mathematics in community college, but it was from a very CS perspective with very little math. In my undergraduate institution, we had an "introduction to proofs" course that simulated what I imagine a discrete mathematics course should look like from a more rigorous math perspective. For UCR, the discrete mathematics course recommends the following for a normal 10 week quarter:

- Text: Schaum's Outline of Discrete Mathematics 3ed by Lipschutz and Lipson
- Topics:
	- 3 weeks spent on sets and functions (ch. 1,2,3)
	- 2 weeks spent on logic and propositional calculus (ch. 4)
	- 1.5 weeks spent on basic combinatorics (ch. 5)
	- 2 weeks spent on advanced counting and recursion (ch. 6)
	- 1.5 weeks spent on probability (ch. 7)

This is purely my opinion, but I think this is a bit of a strange list of topics. Probability, even discrete probability, doesn't seem to belong here and the section on logic and propositional calculus coming after sets and functions seems a little strange. It's possible that giving the students time to work with more familiar objects like sets and functions will given them a bit of a "warmup" time before moving onto something more formal and rigorous, but the section on logic is, for many students, quite dull and painful. There is also an issue of how to introduce proof techniques (direct, contrapositive, contradiction) when starting with sets and functions. It made a lot more sense to me to start with logic and introduce proof techniques as they do with truth tables, emphasizing logical equivalence between things like the direct proof and contrapositive. It is a slog to get through truth tables, but the reward is the streamlining of the rest of the course. My other gripe was that I wasn't so keen on the textbook being used, but I was a little scared to not use it to some degree in case someone who has a hand on my job took a look at my syllabus. Last, it seemed strange to not include number theory in the list of topics as something like the Euclidean algorithm is a staple for both math and CS students in this type of course. 

Ironically, most of the faculty in the department were in agreement that the official syllabus was outdated and the recent professors who taught the course weren't even using it and were teaching more similarly to what I had in mind. I didn't find this out until I wrote my syllabus which was a nice confidence boost to know that I wasn't practicing some kind of mathematical heresy in my choices.

Here is what I listed in my eventual syllabus:

- Main text: Schaum's Outline of Discrete Mathematics 3ed by Lipschutz and Lipson
- Additional texts:
	- A Transition to Advanced Mathematics 7ed,8ed - Andre, Eggen, Smith
	- Discrete Mathematics and Its Applications 7ed - Rosen
- Topics:
	- Logic and Proofs
		- propositions and connectives
		- quantifiers
		- proof techniques (direct, exhaustion, contrapositive, contradiction)
	- Set Theory
		- basic concepts
		- set operations
		- mathematical induction
	- Introduction to Combinatorics
		- basic counting principles
	- Introduction to Number Theory
		- divisibility and modular arithmetic
		- prime numbers and gcd
		- the Euclidean algorithm
	- Functions (injections, surjections, bijections, inverses, compositions)
	- Cardinality
		- countable sets
		- uncountable sets

The topic titles comes mainly from the first additional text, which I used in my introduction to proofs course in my undergraduate institution. It was intented for upper division math majors, but the material was fine for lower division discrete math students too. I took some notation conventions from Rosen's text, which has a little more emphasis on algorithms and topics a CS student would be interested in. I tried to balance both, but it's probably obvious by now that I leaned toward the one that I'm more familiar with. 

My thought process for the topics was to get through all the logic stuff upfront and to go through the major proof techniques by using simple examples from calculus or number theory. Induction was placed in the set theory chapter because that's where it is in the additional text. It's possibly the most important topic in the course for CS students. At first, I was debating whether to exclude the function chapter entirely but after a desire sparked in me to talk about cardinality, I had to include it just to reach bijections. And as mentioned earlier, I wanted to include number theory just to reach the Euclidean algorithm. 

I've included my [lecture notes](https://github.com/elin35/elin35.github.io/blob/master/assets/pdfs/lec_notes.pdf) for anyone interested. 

Some things I was happy about:
- I felt my organization in the course was good in terms of the housekeeping. I kept to my syllabus strictly in terms of quizzes, exams and grading. I graded quickly and I used the grading scheme of another professor who taught the same class in which I was a TA. It seemed a little too nice at first, but I think it was sufficient.
- I think my lecturing was okay for the most part. I was a little afraid at first of pacing and covering everything I wanted to cover, but I ended up covering everything while keeping a good pace. My board usage was hopefully organized and I was very careful to keep to my number scheme in my lecture notes so that when I referenced something, it was clear what I was refering to. 
- Keeping up on typing the lecture notes also went better than I initially anticipated. I quickly realized that I could cover about 2-3 pages in a single 1 hour lecture, so it made typing faster since I knew where to stop and I was usually well ahead of schedule in typing. 
- My language felt good in lecture in the sense that students seemed receptive to matching loose casual descriptions to the formal definitions. 
- My evaluations were strong as usual, but there are many factors which might skew this one way or another.

Some things I wasn't so happy about:
- I was hoping to have more time during lecture for students to work on examples and discuss a bit with each other as practiced in active learning techniques and "think-pair-share", but after a few weeks, I realized I wouldn't have time to keep this up to a satisfactory degree. 
- I felt my problem choice was quite poor. I didn't dedicate enough time to really thinking about why I was choosing the examples I chose for lecture notes and also the problems I chose for homework and exams. I stuck to a kind of "easy-medium-hard" type of scheme in the examples, but that was about as much depth of thought that I put in. In an ideal world, I would've given reason to each problem in the sense that
	- the exercise reinforces a definition or theorem (this one I did consciously think about)
	- the exercise motivates an idea or technique that wasn't made explicit in lecture
	- the exercise explores a new topic (I did do a little of this in quizzes and exams)
	- other pedagogically intelligent things that I can't currently think of

In summary, the class was great (minus some student conflict), and I'd love to do it again. 
