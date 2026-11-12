[[AI Documentation]] loves to pollute PR descriptions with long lists of what changed, what it tried but ultimately didn't do. Things which is imperatively impossible for human to read about, or even care about when looking at a PR, and just makes it so much harder to understand and read.

A PR Description is the only human readable part of a code change, and it ultimately is a source of history of _why_ the code changed, and therefore should be preserved as such. It should capture:
- Why are we opening the PR
- What is the reason for the code change

A PR description should focus on the _intent_ of the code change. It should be targeted towards new people in order to help them focus on what bits are important vs not important.

Also, if you encode too much information into a PR description then it just pollutes any future agent trying to review that PR, since you are giving it too much information off the bat and not actually allowing it to discover any flaws in the code. In these cases it's almost better when having an agent review to ask it to ignore the PR description so it can build its own world view.

Ultimately a PR description is a human to human conversation, and it should be maintained as such. It can have relevant information added to it, that's gleaned from working with an agent, but it should at the end of the day be treated as you talking to another person and defending your code changes.
