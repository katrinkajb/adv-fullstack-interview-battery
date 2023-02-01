# Fizz Buzz

Fizz Buzz is a very typical kind of interview challenge. It's straightforward,
it's quick (to not waste the interviewee's time), and answers a rather
fundamental question: Can you write any simple program at all?

## Getting Started

This will be a simple command line application. You can create a new repository
in GitHub, clone it, and create an `index.js` in the repository.

You can run this `index.js` with `node index.js` from the command line.

## Description

Here's how the program goes:

1. The program prints 1 to 100.
2. Each number that is evenly divisible by 3, instead of writing the number,
   write `fizz`.
3. If the number is evenly divisible by 5, instead of writing the number, write
   `buzz`.
4. If the number is evenly divisible by _both 3 and 5_, instead of writing the
   number or `fizz` or `buzz`, write `fizzbuzz`.

To help us out with readability, write out each number or word on its own line.

An additional perk to this exercise is it allows interviewing engineers to ask
you why you wrote the code the way you did. Be prepared to offer explanations.

### Modulo

"Evenly divisible", "remainder", and "modulus" math terms are your cue to use
the modulo operator `%`, which produces a modulus (remainder). This operator is
relevant for this exercise.

For example, you can determine if `number` is evenly
divisible by two with `number % 2 === 0`. The `number % 2` expression will
divide `number` by `2` and provide a whole number with the "remainder".

`7 % 3` is the same as saying 7 divided by 3. 3 goes into 7 two times (2) and
has one left over (1). So the expression `7 % 3` would evaluate to `1`.

The modulo operator tends to come up in more math related domains. Some
examples:
1. Detecting if a number has even divisibility (by comparing the modulus to 0).
2. Converting a 1 dimensional position to a 2 dimensional position. The quotient
   (the result of division) can be thought of as the y position, and the modulus
   (the remainder of the division) can be thought of as the x position.
3. Constraining a number to a range by "wrapping" it. This is useful for random
   number generation and working with array "slotting".
   1. For random number generation, you can take the modulus to constrain the
      random number into the range you desire. `randomNumber % 100` produces a
      number between 0 and 99, regardless of what `randomNumber` is.
   2. Slotting: If you have an array of 5 elements, you can take the modulus of
      some unknown number and 5 to ensure you always get a number between 0 and
      4, which are valid array positions for an array of length 5.

## Learning Objectives

1. Learn how to implement FizzBuzz, a common interview challenge.
2. Learn about the modulo operator (`%`).
3. Learn some common questions that arise in technical interviews and how to
   answer them.
4. Grow more comfortable with technical interviews, and having your code
   reviewed under a technical interview setting.

## Acceptance Criteria

1. Run the program with `node index.js`, and it should print the results to
   `stdout` (`console.log` does this).
2. Each number or word is on its own line.

## Rubric

| Rubric                                       | Points |
|----------------------------------------------|--------|
| Implement fizz and buzz.                     | 5      |
| Implement fizzbuzz.                          | 5      |
| Defend a question about your code.           | 5      |
| Answer what you would've if given more time. | 5      |
