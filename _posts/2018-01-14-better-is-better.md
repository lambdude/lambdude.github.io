---
layout: post
title:  "Better is Better"
date:   2018-01-14 20:06:10 -0500
comments: true
published: false
---

In 1991, Richard Gabriel published [Lisp: Good News, Bad News, How to Win Big](https://www.dreamsongs.com/WIB.html).
In the paper, Richard uses the phrase _"[worse is better](https://www.dreamsongs.com/WorseIsBetter.html)"_ to explain
why people believed C was better than Lisp. The crux of the essay, according to Richard, is
[The Rise of Worse is Better](https://www.dreamsongs.com/RiseOfWorseIsBetter.html).

Richard talks about four components of program design: simplicity, correctness, consistency and completeness. He
contrasts two styles, which he terms _the right thing_ and _worse-is-better_. We will be looking at this in the
context of Rust.

## The Right Thing

> - Simplicity -- the design must be simple, both in implementation and interface. It is more important for the interface to be simple than the implementation.
> - Correctness -- the design must be correct in all observable aspects. Incorrectness is simply not allowed.
> - Consistency -- the design must not be inconsistent. A design is allowed to be slightly less simple and less complete to avoid inconsistency. Consistency is as important as correctness.
> - Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases must be covered. Simplicity is not allowed to overly reduce completeness.

This is the Lisp way.

## Worse Is Better

> - Simplicity -- the design must be simple, both in implementation and interface. It is more important for the implementation to be simple than the interface. Simplicity is the most important consideration in a design.
> - Correctness -- the design must be correct in all observable aspects. It is slightly better to be simple than correct.
> - Consistency -- the design must not be overly inconsistent. Consistency can be sacrificed for simplicity in some cases, but it is better to drop those parts of the design that deal with less common circumstances than to introduce either implementational complexity or inconsistency.
> - Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases should be covered. Completeness can be sacrificed in favor of any other quality. In fact, completeness must be sacrificed whenever implementation simplicity is jeopardized. Consistency can be sacrificed to achieve completeness if simplicity is retained; especially worthless is consistency of interface.

This is the C way.

## Hold Your Horses

Before we get too far ahead of ourselves, let's take a moment to remember that A LOT has changed since 1991.

- TDD
- Agile

## Better Is Better

But what is the [Rust](https://www.rust-lang.org) way? Or, rather, what should the Rust way be?

### Simplicity

Rust encourages simplicity by using zero-cost abstractions.

### Correctness

The design must be correct in all aspects. It is slightly better to be simple than correct, but there are
certain aspects in which incorrectness is not allowed.

Rust forces type correctness by using strong static types.

Correctness is usually framed in terms of behavior. Rust encourages us to be correct with built-in testing.
However, the coverage is all up to us.

### Consistency

Rust forces interface consistency by using composition via traits.

### Completeness

The design must cover all situations. Rust forces completeness in several ways: exhaustive pattern matching,
trait-based composition.

Rust forces branching completeness by using exhaustive pattern matching.

## Security In An Insecure World

## Tradeoffs, Thinking And Judgement


