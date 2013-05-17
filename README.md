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
4. Run the executable
5. Submit your first turn, and wait for your friend to submit theirs.

## Writing games

The gitwar script is actually very dumb about
what's going on in the game. It just adds files, commits, pushes,
pulls, and spits out a log. Normal git stuff. The game script can be pretty much anything you want.

Here's the best way to use gitwar when commiting an action:

```bash
getPlayerMove
executeMove
../gitwar "$human_readable_commit_message" "$machine_readable_action"
```

Reading the log:

```bash
log=`../gitwar -l`
# loop over the log to recreate
while read line; do
  action=`echo "$log" | cut -d, -f3`
  # recreate all past actions
done < <(echo "$log")
```

It might also be nice to include a file just to save users' names and
properties. See `gitwar.users` in either gitfight or gitchess.

Make sure you send a pull request with your new game when you're done so everyone can enjoy it.

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
