+++
title = 'Algorithmic Poems'
date = 2019-01-14
draft = false
+++

> This post was first published in my old blog, hosted at `blog.neerajadhikari.com.np`.
> I have since taken down the old blog and copied some of its posts here.

While there are now algorithms left and right writing poetry (or, depending on
your opinion, writing stuff that is not quite poetry), let's talk about
something even more interesting - poetry that describe algorithms.
Surprisingly, I couldn't find more than a few such poems. It is difficult
enough to exactly and concisely express most algorithms even in prose, so
perhaps it is not so surprising after all. But simpler, elegant algorithms are
relatively easier to express in prose and as we shall see, poetry. As we can
expect, these poems do not provide a complete specification of algorithms, but
nevertheless describe their general working very well. Here I list the ones
that I have found, and I'll keep expanding this list as I hopefully find more
in the future.

## Sieve of Eratosthenes

> Sift the Two's and Sift the Three's,
>
> The Sieve of Eratosthenes.
>
> When the multiples sublime,
>
> The numbers that remain are Prime.
>
> -- Anonymous

The [sieve of
Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes) is an
ancient algorithm for finding all primes up to a given limit. It is a simple
algorithm, discovered by the Greek mathematician Eratosthenes of Cyrene
millennia before there were computers or even the formal study of algorithms.
It works by starting with a list of all natural numbers less than a limit and
crossing out multiples of discovered primes one by one, starting with two. Once
there are no bigger primes to cross out multiples off, the algorithm ends and
all numbers that remain unmarked are primes.

## Gradient Descent

> Still the fog persists.
>
> Let the incline have its way
>
> and set your compass.
>
> Keep taking footsteps
>
> until that first suspicion
>
> of an uphill slope
>
> then turn left or right,
>
> just one of many zig-zags.
>
> Will it ever end?

This poem by Michael Bartholomew-Biggs appears in his paper titled [Algorithms
and Poetry](https://www.researchgate.net/publication/282948019_Poetry_Algorithms), along with other poems describing algorithms for
optimization problems. This one describes the gradient descent or steepest
descent method of finding the minimum of a function in possibly
high-dimensional space. It is the most common method used for optimizing neural
network weights. It works by starting at some initial position and gradually
moving in the direction (in the input space) of the steepest descent of the
function value. The algorithm stops at the "first suspicion of an uphill
slope", or the point from which there is no way downhill. The fog in the poem
refers to the fact that at a time we can only 'observe' the immediate
surroundings of the point we are at, instead of the entire topography.

## Spanning Tree Protocol

> I think that I shall never see
>
> A graph more lovely than a tree.
>
> A tree whose crucial property
>
> Is loop-free connectivity.
>
> A tree which must be sure to span
>
> So packets can reach every LAN.
>
> First the root must be selected.
>
> By ID it is elected.
>
> Least cost paths from root are traced.
>
> In the tree these paths are placed.
>
> A mesh is made by folks like me
>
> Then bridges find a spanning tree.

This one by [Radia Perlman](https://en.wikipedia.org/wiki/Radia_Perlman) is my
favorite. It describes the algorithm for the [Spanning Tree Protocol](https://en.wikipedia.org/wiki/Spanning_Tree_Protocol), which is used implemented by
layer-2 bridges in a network which may have cycles in the topology which lead
to *broadcast radiation*, the situation when broadcast frames flood the
network. To prevent that, the bridges compute a loop-free subset of the network
topology that spans the entire network, in other words, a spanning tree. The
algorithm runs on each bridge in the network, and they communicate by sending
out configuration messages to their neighboring bridges. First they agree on a
root bridge for the tree based on an ID derived from the MAC address, and keep
the links that provide shortest distance paths to the root bridge in the
spanning tree. The links not in the spanning tree are deactivated.

While working at Digital Equipment Corporation (DEC), Radia Perlman was tasked
with developing a constant-memory protocol that enabled bridges to locate loops
in a local area network. Legend says that she was given a week to finish the
job, but she invented the protocol in a day and spent the rest of the time
writing this poem.

*Do you know of, or have yourself written, a poem that describes an algorithm?
If so, send it to me and I'll add it to the list.*
