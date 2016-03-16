There's an easy way to reference ranges of commits by partial string matches on their messages.

Given four commits:

```bash
758d337 Freeze-dry ice cream
f983ef8 Update firmware
7ba375f Fix heat shields
cd1ccfc Add rocket thrusters
```

To interactively rebase the last three commits, I might have previously done:

```bash
git rebase -i HEAD^^^

# Or:

git rebase -i HEAD~3
```

The same thing can be accomplished with the much more readable:

```bash
git rebase -i :/rocket
```

Note that the range is referencing the fourth most recent commit, which will tell `rebase` to give us the last three.

This technique is also useful when using `git commit --fixup`.
