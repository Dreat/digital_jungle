---
title: Signals
tags: se
---

<status>Status: 🌿 </status>

Signals, as <a class="external-link" href="https://sandimetz.com">Sandi Metz</a> calls them (not sure if she came up with the name or just passed along) is obvious in hindsight but brilliant programming tool.

Here examples will describe best what they are, so:

1. Prime/large numbers - pick arbitrary prime/large number, so it signals insignificance of a number. For example, in tests, you can write 5000 where any other number is not bigger than 10; this is a **signal** for others to not search for a meaning behind a number. Personally, I prefer `0` or large numbers instead of primes, as they are more clear on intent.
2. Strings. Same as with numbers, but there's more flexibility. For example, if I need to pass a user ETH wallet address, but it's irrelevant for testing I will go with `"0xfakeaddress"` - so it's clear that it's there just as it's needed and there's no special meaning. If it was a legit address it could make someone believe it's important.

Signals can also imply meaning. While I'm yet to find this usecase, Sandi shown this example

In Ruby code blocks can be in `{ }` or `do end`

1. code in `do end` has side effects
2. code in `{ }` has no side effects

*(note that it's not any official standard and it's not enforced by anyone or any tool)*

This is example of syntax based signal that gives clear understanding of a code (outside tests) to show what's happening even before reading the code in the code block.