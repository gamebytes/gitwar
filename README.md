![](https://secure.gravatar.com/avatar/a52f0b5df73d445c85ffcbb6ac4b1d8b?s=50) Gitwar
======

A platform for git-based turn-based command-line games.

Gitwar and each of its games are written in BASH. That's right.
Git, shell scripting, and playing games has never been so... weird.

## Games

1. [Gitfight](http://github.com/gitwar/gitwar/tree/master/gitfight)
2. [Gitchess](http://github.com/gitwar/gitwar/tree/master/gitchess)
3. Gitcastle - Coming Soon

## How to play

1. Fork this repo
2. Add a friend as a collaborator
3. CD into the game you want to play
4. Run the executable: `./gitfight`
5. Submit your first turn, and wait for your friend to submit theirs.

## Writing games

Here's what's needed to write a Gitwar game:

**Nothing.** The gitwar script is actually very dumb about
what's going on in the game. It just adds files, commits, pushes, and
pulls. Normal git stuff.

The game script can be pretty much anything you want. Just remember to
use `../gitwar <commit message here>` to submit a turn and wait for your
opponent.

## Gitfight-style

Here's what you will need if you want your game to be anything like
gitfight:

1. gitwar.log - gitfight can replay the entire game sequence so leaving the game
   and re-entering is a breeze.
2. gitwar.users - gitfight uses this file to make sure your
   gitconfig's user.name is on the list of players
3. The rest of it: theme, user-input, scoring system, algorithms are all
   up to you.

Make sure you send a pull request when you're done so everyone can enjoy it.

## Note

This is more for fun than for anything else. It's just yet another way
of showing how cool git and Github are.

Have fun!

------
http://tybenz.com

*[Gitwar logo](http://thenounproject.com/noun/soldier/#icon-No1697) designed
by [Simon Child](http://thenounproject.com/Simon Child) from the [Noun
Project](http://thenounproject.com) and [Jason
Long](http://twitter.com/jasonlong) from
[git-scm.com](http://git-scm.com/downloads/logos).
