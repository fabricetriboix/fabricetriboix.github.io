---
layout: post
title:  "What's wrong with C++?"
date:   2017-04-19 20:43:00 +0100
categories: coding
---

I would like to avoid here to descend into useless flame wars about "C++ is better than XYZ", "C++ is incomprehensible", "C++ is the best invention since toasted bread", etc. But I do have an opinion about whether C++ should be chosen on a given project or not.

It can't be argued that C++ is a powerful language that provides a lot of freedom to developers. It is still very low level, however, and thus come the risk of shooting yourself in the foot. But with great powers come great responsibilites, and that's where I think the curx of the matter is, because I think some C++ developers do not take their responsibilities well.

My general observation is that too often, C++ developers are too emotionally attached to their favourite design patterns, libraries, coding style, etc. They do tend to be quite smug and have an "I am right, and anyone who disagree with me is wrong" attitude. They can't understand the value of commenting the code, so they don't do it. They spend far too much time striving for the ultimate elegance, absolute genericity, or 0.1% CPU optimisation. I won't give any names here, but you just need to search for the blogs or youtube videos of the recognised C++ authorities of the day to get a feel of what I mean.

It's like it doesn't occur to them that they could aim to increase their employer's revenues, decrease their costs, or better understand what the customers really want.

Because these top-gun developers are so expert in their language, they tend to write code that looks like ancient runes and forbidden arcanes. You can't figure what it does just by reading it, but it works, just like a magic incantation. But if there's a subtle bug in it, and if the spirit who produced that work of art is no longer in your organisation, you have a choice between re-writing the code and hiring a super-expensive C++ master guru (who will throw it anyway because it's rubbish according to his taste).

I am always amazed when I see job postings for C++ contractors paying GBP800/day or permanents paying £100k. That does not make business sense to me, because these guys won't be able to work together, they will write obscure code using their idiosyncratic style, and obviously will leave no comment or documentation whatsoever. And don't think about code reviews. Because such developers don't think about the business aspect of their work, the organisations that hire them will just continue paying through the nose for expensive work of arts that most probably won't ever fulfil their requirements.

So my take is that their is a problem with C++ and it is of a social nature, not technical. I still believe C++ is a powerful and versatile language.

Great care should be applied when choosing a programming language for your project. Don't just go for the default option your or your dev team is used to. Choosing the right programming language for the right task could be the difference between success and failure of the project, and must be a deliberated decision.

As addendum, here are some examples of criteria for choosing a programming language:

 - Is it available for the target platform?
 - Is CPU performance critical for success? (if yes, you should probably avoid interpreted languages)
 - Will you have suitable tools to debug and test the software?
 - Will your software use third-party libraries?
 - Do you require some level of deterministic behaviour?
 - Is portability a requirement? If yes, portable to which platforms?
 - Will you easily find developers for that language?
 - What kind of salary will you have to pay those developers?

