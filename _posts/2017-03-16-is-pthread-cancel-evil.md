---
layout: post
title:  "Is pthread_cancel evil?"
date:   2017-03-16 20:55:00 +0100
categories: multi-threading
---

What's wrong with pthread_cancel()? It would like tidy and easy to
cancel a thread at any time. Wouldn't that be a clean way to terminate a
thread?

Well, yes and no. The main problem with this method is that it typically
gives rise to deadlocks and other unclean things. Looks at this code:

    void* mythread(void*)
    {
        for (;;) {
            pthread_mutex_lock(mymutex);
            doSomething();
            pthread_mutex_unlock(mymutex);
            doSomethingElse();
        }
    }

Now what would happen if you cancel this thread? You can't choose where
it is cancelled. According to the pthread documentation, it can be at
any 'cancellable point', which could or could not occur within
`doSomething()`. If that's the case, your `mymutex` will stay locked
forever.

The best way to terminate a thread is to stay in control at all time.
Somehow signal the thread it must terminate, and design it so it acts
quickly on such signal.

I have been bitten by that kind of bugs for far too long, so that's why
I developed the 
[SKAL framework](https://github.com/fabricetriboix/skal), which
safely abstracts away all those complexities.
