---
layout: post
title:  "Bug-free software: Does such a thing even exist?
date:   2017-04-03 20:55:00 +0100
categories: software-engineering
---

It is received wisdom that bug-free software does not exist. I believed
it myself for a very long time. In actually, the immense majority of
people believe it, and think that bug-free software is so unattainable
that it's not worth pursuing it. Some say such a thing can't possibly
exist.

Or can it...

Let's have a look at a simple piece of C code:

    #include <stdio.h>

    int main()
    {
        printf("Hello, World!\n");
        return 0;
    }

So... Is it bug-free? Yes? No? What's your take?

The answer, as always, is: "it depends". What if the client (i.e. the
user of this code) actually wanted the greeting message to be displayed
in the current locale? Bug! So we come back to requirements, as always.
Poor requirements means the software will probably not do what the
customer want, even though it would comply with some kind of half-baked
requirements, if they even exist... So we do need high-quality, testable
requirements.

On the other hand, the client can't spend ages writing down
requirements, and trying to imagine all the corner cases he wants the
software to handle. That's essentially the waterfall model, which never
works. We want to be agile! Scrum and Kanban and that kind of stuff!

And we come down to the second half of the problem, which I think is the
most critical. Because people consider software bugs to be as natural and
unavoiable as flu or other illnesses in human, they consciouly or
unconsciously limit their effort to eliminate them. Oh sure! they will
establish coding standards, bug-tracking systems, and various procedures
to limit the proliferation (well, in the best organisations, that is).
But at its core, bugs are essentially accepted as a natural phenomenon.

I think there is another way, which is to not tolerate any bug. My
personal experience over many years working as a software engineer in
different companies taught me that bugs that are intentionally left in
the system cause tremedous amount of pain and grief later. Cold sweat,
compromises, lying to the client, days spent chasing bugs that would
have taken hours if tackled immediately, delays in delivery, poor
quality, lack of stability, you name it.

So we need to be brave and accept a short-term pain (fixing the bug as
soon as it is discovered) for a long-term gain (good quality software
and avoiding headaches down the line). Short-term gain (releasing poor
quality software early to get a promotion or calm down the client) for
long-term pain (poor quality software, angry clients, loss of business)
is for [toddlers who will eat one marshmallow now instead of two
later](https://www.youtube.com/watch?v=Yo4WF3cSd9Q).

So in conclusion, it could be the case that a complex software might not be
bug-free, but at least it can be free of ANY KNOWN bug. If you have an
extensive test suite, not tolerating any bug will make a world of
difference between "acceptable" software that is still crashes under
vague, uncertain and unclear circumstances, and outstanding software
that the client can't manage to break despite its best efforts!
