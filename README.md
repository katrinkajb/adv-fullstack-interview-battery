# Interview Battery

This is a battery of interview technical challenges that typically arise.

Each subdirectory has a set of requirements, notes, and rubric all found in
their readme files.

Name your submission branch after the challenge you're working on instead of the
typical `dev`.

Challenges:
1. [Vending Machine](./vending-machine/README.md)
2. [Fizz Buzz](./fizz-buzz/README.md)
3. [Bowling Ball](./bowling-ball/README.md)

## Notes on Technical interviewing

### The Interview Itself

#### It's Supposed to be Hard

A good interview challenge is designed to challenge you and _make you think_,
so your interviewers can observe how you handle problems you've never
encountered before. Typically rote memorization is not valued, but being able to
reason about and solve a fresh problem is highly valued. If the problem were
easy, or one you've seen before, then the information from the interview is
soiled. This isn't to see if you'll crack under the pressure - but to ensure the
team can leave you to solve problems on your own as an individual contributor.
You don't need to be able to solve all problems, but show that you're capable of
solving unknown problems by breaking them down.

#### These are not Pass/Fail Quizzes

Form, approach, mentality - these all surpass _actual working code_ in an
interview setting. Interviewers want a glimpse into how you work. Do you reach
out for help? Do you give up? Do you reach to tools like documentation, Google ,
and Stack Overflow when you encounter some API or error you've not seen before?

A candidate that shows attentiveness to quality of code, testing, documentation,
and is capable of looking something up before tugging on the coat-tails of a
colleague will show better in an interview than someone who turns in a working
version with no real communication and only the interviewee can understand the
code.

#### There is a Deliberate Vagueness

Providing vague challenges to candidates will oftentimes yield surprising and
pleasing results. For example, some candidates, unprompted, will write unit
tests in their submissions. Others will write documentation. Others still will
write robust error handling. What will you do when you're given free reign over
the output?

#### The Code Challenge is a Talking Point

Interviewers will want to pick at your code and ask you questions about it. Why
did you make the choices you did? If you had more time, what would you have done
differently? Do you see any pitfalls with your solution? Being able to answer
these questions shows you put thought into your solutions, and you didn't just
rush to the answer as fast as possible without thinking of any kind of
trade-offs.

#### Brevity is Understood, but Bring it up Anyways

Have an answer ready in the pipe for "What would you do if you had more time?"
or even leave comments in your code saying "eh this is quick-n-dirty - with more
time I would do X". This is a quick nod to code quality, even if time and scope
does not permit you to engage it now. A candidate that is aware that they are
cutting a corner is far better than a candidate that has no idea the ruin they
leave in their wake.

#### You Might do Everything Right and Still Get Passed

There's a lot of factors that play into candidate selection, some of which are
simply limited resources of the organization doing the hiring. In that sense
it's kind of a zero sum game - a candidate will occupy the position eventually,
and sometimes there's just someone who is a better fit than you, even if you
were still a good fit. Don't take this as a personal failing. The dice won't
favor you every time.



### Interview Tips
#### Verbalize

Talking through a challenge is important because it gives the interviewers a
window into your thought process.

Try to talk out loud about what kind of assumptions you're going to make, or
ask questions about the assumptions.
1. Can I assume valid input?
2. Roughly how many records is the data set anticipated to have? (does it need
   to be fast?)

#### Admit When Guessing

Software Engineers are severely hampered if they can't use document / Google /
Stack Overflow to answer questions about a great many APIs. Even someone highly
familiar with a particular library or framework still needs to look things up on
a daily basis.

When asked a question about something you don't know, it's okay to admit you
don't know, but also try to guess anyways. Admitting you're unsure softens your
guess if you get it wrong, and it also communicates to your interviewer that
you're aware of gaps in your knowledge. This is preferable to people who take
blind leaps.
