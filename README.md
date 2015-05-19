Dominion cards randomizer
-------------------------

`dominion` is a command to prepare a [Dominion](http://riograndegames.com//search.html?s=Dominion) game.
It picks 10 random Kingdom cards from one or several Dominion sets at the start of a game.

### Getting started

- Make the `dominion` script executable.
- Put it somewhere in your `PATH`.
- Put the `cards.json` file in the same directory.
- Use it (see Usage section below).

### Supported Dominion sets

- Base
- Intrigue
- Seaside
- Alchemy
- Prosperity
- Dark Ages

### Usage

```
usage: 
    dominion [set [set ...] [-n [number [number ...]]] [-s] [-t] [-d]]
    dominion [-l [set [-s] [-t] [-d]]]
    dominion [-c card]
    

Dominion cards randomizer.
--------------------------

positional arguments:
  set                   set is a dominion set name. Pick 10 random cards from
                        this dominion set. If several sets are passed, then
                        pick 10 random cards from all passed sets. If -n
                        option is not used, the number of cards will be
                        balanced between each set.

optional arguments:
  -h, --help            show this help message and exit
  -n [number [number ...]], --number [number [number ...]]
                        Numbers of cards to pick from each set. The first
                        number will be applied to the first set in argument,
                        the second number to the second set and so on. Numbers
                        must be integers.
  -s, --sort            Sort cards by card name instead of card value.
  -t, --type            Also print card type.
  -d, --description     Also print card description.
  -l [set], --list [set]
                        List dominion sets if no argument is passed. List
                        cards of a set if a dominion set name is passed.
  -c card, --card card  card is a card name. Print card details. If there are
                        several words in the card name, use "".

Examples:
    dominion base
    Print 10 random cards from dominion base.

    dominion base -s
    Print 10 random cards from dominion base, sorted by name instead of value.

    dominion base -td
    Print 10 random cards from dominion base including their type and
    description.

    dominion base seaside
    Print 5 random cards from dominion base and 5 random cards from dominion
    seaside.

    dominion base seaside -n 4 6
    Print 4 random cards from dominion base and 6 random cards from dominion
    seaside.

    dominion -l
    Print list of supported dominion sets.

    dominion -l base
    Print list of dominion base cards.

    dominion -c Market
    Print Market card details.

    dominion -c "Council Room"
    Print Council Room card details.
```

### Data

All data in `cards.json` are scraped from [dominionstrategy.com](http://dominionstrategy.com/all-cards/).

### License

All code is licensed under the GNU General Public License version 2. See `LICENSE.txt`.