---
layout: post
title:  "Better Is Better"
date:   2018-01-12 20:06:10 -0500
comments: true
published: false
---

In 1991, Richard Gabriel published [Lisp: Good News, Bad News, How to Win Big](https://www.dreamsongs.com/WIB.html).
In the paper, Richard uses the phrase _"[worse is better](https://www.dreamsongs.com/WorseIsBetter.html)"_ to explain
why people believed C was better than Lisp. The crux of the essay, according to Richard, is
[The Rise of Worse is Better](https://www.dreamsongs.com/RiseOfWorseIsBetter.html). This work was __very__ controversial
when it was released. The history around it is pretty interesting, so check out the links if you have a chance.

Richard talks about four components of program design: simplicity, correctness, consistency and completeness. He
contrasts two styles, which he terms __The Right Thing__ and __Worse Is Better__. We will be looking at this in the
context of [Rust](https://www.rust-lang.org).

## The Right Thing

This is the Lisp way. This is the MIT/Stanford style of constructing programs as if they were bridges. This style of
construction led to the mentality of specification documents and the waterfall method. The idea is pretty straight-forward.
You want to design all of your components up front with complete correctness and then solve the problem the program was
intended to by aggregating different functionality. But writing code is not like building bridges and in practice this method
hasn't been effective.

> - Simplicity -- the design must be simple, both in implementation and interface. It is more important for the interface to be simple than the implementation.
> - Correctness -- the design must be correct in all observable aspects. Incorrectness is simply not allowed.
> - Consistency -- the design must not be inconsistent. A design is allowed to be slightly less simple and less complete to avoid inconsistency. Consistency is as important as correctness.
> - Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases must be covered. Simplicity is not allowed to overly reduce completeness.

## Worse Is Better

This is the C way. This method is nicknamed the New Jersey style. The idea is to get the product done in the fastest,
most direct way possible. This approach is much more interested in practical gains than ideal principles. This has found
its way into companies that are focused on results. The task needs to be completed in the most direct and efficient way.
What _should_ be is often dismissed in the face of business needs.  However, the amount of technical debt that is accrued
in this process often becomes insurmountable and the program lurches toward spaghetti.

> - Simplicity -- the design must be simple, both in implementation and interface. It is more important for the implementation to be simple than the interface. Simplicity is the most important consideration in a design.
> - Correctness -- the design must be correct in all observable aspects. It is slightly better to be simple than correct.
> - Consistency -- the design must not be overly inconsistent. Consistency can be sacrificed for simplicity in some cases, but it is better to drop those parts of the design that deal with less common circumstances than to introduce either implementational complexity or inconsistency.
> - Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases should be covered. Completeness can be sacrificed in favor of any other quality. In fact, completeness must be sacrificed whenever implementation simplicity is jeopardized. Consistency can be sacrificed to achieve completeness if simplicity is retained; especially worthless is consistency of interface.

## Hold Your Horses

Before we get too far ahead of ourselves, let's take a moment to remember that A LOT has changed since 1991.
A myriad of languages have been written. New technologies have emerged. Innovative techniques have revolutionized
how many programmers work. Let's focus on two of the most important techniques and how they relate with the two styles.

### TDD

Test-driven development shares the same notions as The Right Thing.

### Agile

Agile processes share the same notions as Worse Is Better.

## Better Is Better

But what is the Rust way? Or, rather, what should the Rust way be? We have been talking about design
in the context of programming languages. This is because our programming language gives us the tools
that we use to build our program. But it is also because our programming language models how we think
about programs. The Right Thing emerges from Lisp. Wrong Is Better emerges from C (and many other C-like
languages). What emerges from Rust? I call it Better Is Better.

### Simplicity

Rust encourages simplicity with its high-level syntax by using zero-cost abstractions.

Rust encourages simplicity with clearly defined idioms and patterns.

### Correctness

Rust forces type correctness by using strong static types.

Rust encourages behavior correctness with built-in testing.

### Consistency

Rust forces interface consistency by using composition via traits.

Rust encourages interface consistency with common interfaces in many different crates (libraries).

Rust forces data consistency with its ownership model, which guarantees memory safety.

Rust encourages data consistency by making data immutable by default.

### Completeness

Rust forces branching completeness by using exhaustive pattern matching.

## Better Is Better Is Better

Better Is Better is a fusion of the best parts of The Right Thing and Worse Is Better.

> - Simplicity -- the design
> - Correctness -- the design
> - Consistency -- the design
> - Completeness -- the design

