# Vending Machine

You are developing a vending machine. Your component deals with monetary
exchange. A user deposits money into the vending machine, selects a product, and
the product is provided along with proper change. This program computes the
change to give back.

## Demo

[vending-machine-demo.js](./vending-machine-demo.js)

## Getting Started

This assignment involves building a terminal program using Node.

Start with a fresh repository. You can use `npm init` inside the root of your
new repository to give you a fresh `package.json`.

You can create an `index.js` file. This file can be run using:

```sh
$ node index.js
```

Don't forget that `$` is typically showing off the prompt. You omit that if you
copy+paste that into your terminal.

## Learning Objectives

1. Get comfortable with technical interview submissions.
2. Learn how to add a little extra on your interview submissions to make it
   stand out.
3. Add more to your repetiore of writing CLIs (command line interfaces).

## Description

This vending machine challenge is a actual technical challenge that has been used
in the outside world. It's complex enough that the candidate gets to show off
some logic skills, while also being straightforward enough to get done in an
amount of time that is respectable to the candidate and allows them to do it
live.

The vending machine program accepts an item's cost and payment as input, and
outputs how much change is returned.

Proper change is defined as using the largest denominations possible using
American coinage. If the change is 86 cents, the output will be 3 quarters, 1
dime, and 1 penny.

### Time Constraints

Timing and software engineering have a fickle relationship. Sometimes it takes
just a few minutes to bump a button over a few pixels, and sometimes it takes
hours. Your interviewers will account for this - getting a complex code
challenge complete is generally not on their minds, but it certainly helps to
complete the challenge.

Keep in mind your time constraints, and remember that this is your chance to
show off what you can do and what you value in your code. Make sure your code is
readable and understandable. If you're having trouble understanding your own
code, revisit it so you can.

### Additional Interview Tips

See [the root README](./README.md) for tips and notes on technical interviewing.

### Floating Points

Beware strict floating point comparisons! Try this in your Browser's console:

```js
0.1 + 0.2 === 0.3
```

It will evaluate to false, because `0.1 + 0.2` doesn't give exactly `0.3`.
Floating point numbers are approximations and should only be used when
approximations are appropriate. For money, approximations are not appropriate.
You can instead treat the numbers as cents internally (multiply by 100 or divide
by 100 depending on input or output).

If you actually did need to compare floating point numbers, you would have some
kind of "wiggle" room or percentage decided upon, and you would compare to see
if the number landed within that range.

```js
const floatWiggle = 0.0001;
const x = 0.1 + 0.2;
const y = 0.3;
if(x + floatWiggle < y && x - floatWiggle > y) {
  // Close enough, consider them the same.
} else {
  // Too far apart.
}
```

Some trivia: Floating point numbers are represented by a base number (mantissa)
and an exponent, which combine together to produce the final number.

## Acceptance Criteria

Once your submissions is ready, open a pull request as normal and schedule time
with a TA to go over your code.

## Rubric

| Rubric                                                                           | Points |
|----------------------------------------------------------------------------------|--------|
| The program accepts inputs of `--item-cost` and `--payment`.                     | 5      |
| The program prints the coins returned (see formatting section) and success/fail. | 5      |
| Select and implement one of the personal flair items.                            | 5      |
| Select and implement another of the personal flair items (extra credit).         | 10     |


## Formatting

The program must output all coin types supported, each with its own line. The
general format is `<coin name>: <number of coins>`. So for quarters, you would
see `Quarters: 3` for 75 cents. Numbers should be padded out to the largest
coin type, plus a space between the colon and the number. For example:

``` text
Quarters: 3
Nickels:  1
```

Coin types are sorted from highest denomination to lowest denomination.

Total change is printed afterwards as `Total Change: <amount>`. Include the
currency glyph in the appropriate location for that currency.

All submissions will be run through automation prior to being submitted to the
development team for deliberation. Candidates whose submissions that fail to
follow the formatting rules will not be considered for employment. Here at
Widget Co, we really value the exactness of our requirements for our widgets.

## Personal Flair

For the first half of the assignment, work on the minimum requirements for the
implementation. Afterwards we'll get together and expand the program to include
something additional that shows off your skills and values.

### Part 1

In the first half of the assignment, just do the first two rubric items (rubric
without flair).

### Part 2

You have strengths and weaknesses like everyone else. It's time to show
off what you value and what you're good at. Select one of these flair (there are
rubric entries for each). A second one is worth extra credit.

When doing these, any additional functionality or code brought about by flair
still is subject to the other bit of flair you have. So if you chose TDD and
Support Other Currencies, the additional currency support needs to also be
tested, and test coverage needs to still be at 100%. If you chose JSDoc and
Support Other Currencies, the `--currency` argument needs to be in the usage
print out.

### JSDoc Everywhere!

You live by this mantra:

> Programs are meant to be read by humans and only incidentally for computers to
> execute.
> 
> -Harold Abelson

Your programs are not only readable, they are understandable! Part of how you
accomplish this is you add lots of comments to your code everywhere. Your
program uses [JSDoc](https://jsdoc.app/) to comment every function, class, and
each file has a comment header with an explanation of why you have it and what
it does.

Additionally, your program prints [usage
information](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html)
when given the `--help` argument, or if the `--item-cost` and `--payment`
arguments are not supplied.

Be sure to note this in your submission.

### TDD - Test Driven Development

You wrote unit tests for every bit of functionality in your code. You live by
this sentiment: If it's not tested, it doesn't exist.

Your submission includes running the test suite in its GitHub Actions.

### Support Other Currencies

To solve a problem in the small case shows both small understanding and is a
waste of time. You prefer to solve a problem once, and forever for all of its
cosmetic variations. To you, fundamental, logical laws are your `food-transport`
and `edible-lubricant`. 

Don't just add support for one more currency, add support for _all existing and
future currencies_. Your program looks for a `currencies.json` file which
defines currency types, their formatting, and an abbreviation for the currency.

Additionally, your program now accepts a `--currency` argument (which defaults
to `USD` for backwards compatibility purposes) that allows selecting from
`currencies.json`.

A `currencies.json` looks like this:

```json
{
  "USD": {
    "abbreviation": "USD",
    "format": "$%amount%",
    "coins": [
      {
        "name": "Quarter",
        "value": 25,
      },
      {
        "name": "Dime",
        "value": 10,
      }
    ]
  }
}
```

Remember - you solved this problem permanently - so any future or imaginary
coinage should work with this system, so long as it is provided in the
`currencies.json`.
