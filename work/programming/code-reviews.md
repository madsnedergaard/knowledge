---
description: How to be help both you and others improve through code reviews
---

# Code Reviews

What you should do as...

### What to do as: The developer who wrote the code

#### Review your own PR!

Read through your changes in a PR and make sure you did not...

* commit debugging code \(like console.logs or out-commented code\)
* commit the wrong files
* forget to comment something that makes no sense for someone else

#### Don't ask for a review before ALL automated checks have passed!

Your CI should catch errors and you as a developer should fix them, before you're asking your human friend to waste their time doing that. 

#### DO AS LITTLE AS POSSIBLE PER PR!

Scope creep sucks and makes it harder for everyone. A PR should address just one thing!

#### If you disagree, but neither feels strongly - the reviewer wins!

After all, that person just read your code with fresh eyes, where you have been deep down into this code.

#### Make sure everyone involved know what the state of a PR is

* Is it still a draft and not ready for review? Convert to draft PR!
* Use the "re-request review" feature in Github to ensure the reviewer knows exactly when they should take a look agian

### What to do as: The reviewer who's reading code

* Be nice and over-explain - your job is to teach & help your teammate

TBD...







## Links

* [How to Make Your Code Reviewer Fall in Love with You](https://mtlynch.io/code-review-love/)
* [How to Make Good Code Reviews Better - Stack Overflow Blog](https://stackoverflow.blog/2019/09/30/how-to-make-good-code-reviews-better/)
* [Guidelines for better pull requests - Kenneth Skovhus](https://skovhus.github.io/blog/better-pull-requests/)
