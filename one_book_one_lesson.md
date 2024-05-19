# One Book, One Lesson

Okay so here's an idea...

It's pretty common to boil a book down to one idea or at least a simplified version of it\* - so my thought is, why not lean into that and explicitly call out the main thing I took from various books that have resonated strongly with me. That's not to play down the importance and value of reading a book in full, but noone has time to do that for _everything_, and I think being explicit about going only-so-deep while also providing a personal angle and encouraging people to dive deeper seems... maybe pretty valuable?

_In case the obvious needs stating - I encourage you to go and actually-buy and actually-read any of the below that sound interesting..._

Also - disclaimer - at least for the first draft(s) of this post, I haven't re-read any of the books in question - even though they are on a shelf in full view from where I'm typing this - but am going on memory, which is partly the point in terms of what has made a lasting impression and honestly, partly laziness! As this post may very well have zero readers I think that's fine, but I may revisit them and update in future.

So:

## Camille Fournier - The Manager's Path

This is a _huge_ one for me - despite the fact that I took the decision several years back to not take the Path in question, I still think this is one of the best-written and most useful books for understanding technical leadership in general and how to survive in the tech industry at any level above just pushing code in the narrowest possible sense. If you want to have a decent sense of what your direct manager does vs the director a couple of levels up that you have only a loose relationship with, this book is a good use of your time.

For me though what I _love_ about is that it starts not with "here's how to be an effective line manager", but rather talking about what one as an entry-level "Individual Contributor" (coding/ non-manager) should expect from your relationship with your immediate boss, and then really nails the key decision point - which I was 100% trying to work my way through at the time I read it - of "I have some level of recognition as a strong technical person who can be trusted to represent the team in meetings, do I want to cash that in to start transitioning into management or stay on the technical track?"

The big takeaway from it for me was "this isn't going to be easy either way". Camille breaks down both paths in terms of "these are your likely expectations, and this is the reality". If you go down the tech path, you may think you'll get to design huge systems and have people respectfully coming to you for input, but there'll be a lot more politics and meetings than you expect and a lot more dissenting voices. Similarly, as a manager you won't automatically get granted authority and larger and larger teams - you have to work for it and a lot of stuff is just going to be _grindy as fuck_ :smiley:.

Personally I'm pretty happy with _the Non-Manager's Path_ - getting better at dealing with people and organizational problems has been a huge force-multiplier for me, but coding and architecture is still where I get my energy and motivation from, and what makes the rest of it worth the effort. Ultimately though, it's a choice everyone has to make for themselves and this book is great for understanding the factors at play.

For further reading that is management-related but still with a distinct tech flavour:
- Charity Majors has some decent stuff ([1](https://charity.wtf/2017/05/11/the-engineer-manager-pendulum/), [2](https://charity.wtf/2022/03/24/twin-anxieties-of-the-engineer-manager-pendulum/)) to say around the decision to go into (and stay in?) management
- IMHO, [Dave Anderson's "Scarlet Ink" substack](https://www.scarletink.com/) is worth the price of entry

## Tanya Reilly - The Staff Engineer's Path

Okay so we are temporarily hitting a bit of a theme here - again, let's lean into it...

This book was fairly explicitly intended as a follow-on/ companion-piece to The Manager's Path for those not choosing to go into management. Symptomatic of an _excellent_ recent trend to actually start looking at what the higher levels of the "Technical Track" look like in companies sufficiently large/ tech-focused for it to be An Actual Thing - Will Larsons's "Staff Engineer" (all the key parts of which can be read for free at [staffeng.com](https://staffeng.com/)) also covers similar ground, and is very solid but for me didn't have one specific impactful moment.

This book though  - Reilly's - is really good, although less life-changing for me than Fournier's. The thing that has stayed with me is **very** simple and concise:

> Wrong is better than vague

Which is to say, in my own much-more-verbose way:

There is almost always a lot of uncertainty when trying to find the optimal (or at least good-enough) solution for a technical problem. As one individual, no matter how senior and knowledgable, you necessarily have a finite and non-exhaustive set of information and are only really going to find out the problems with something by soliciting alternative points-of-view.

It's incredibly tempting on a human level to hide behind vague statements that noone can really disagree with, and hope that someone else will bring clarity - that way you never have to take the bump of being publicly wrong. But that doesn't move things forward - the job of a technical leader is to put one's ego aside, do the best one can to put forward a position that is `in the ballpark of right` based upon what you know and understand right now, and then _give other people the chance to explain why you may be wrong_. If you do this right - calmly and openly - it's can be a huge source of increased credibility and stronger relationships, but it so often feels painful and counter-intuitive

I can't tell you how often I have found this a useful mantra to push myself to do the right thing in the last few years.

## Fred Brooks - No Silver Bullet

And now we're definitely breaking the pattern in that this isn't even a book - rather it's a paper.

For those who don't know, Fred Brooks worked at IBM in the mid-20th-Cenury and is by far best known for his 1975 book "The Mythical Man Month". That book is excellent and does in fact have One Key Lesson (adding software engineers to a project can actually slow it down, because it increases commmunication and coordination costs), but is so well dug over already that I don't think I need to say much more on it.

The just-slightly-more-hipster choice, and a genuine unironic favourite of mine though, is ["No Silver Bullet — Essence and Accident in Software Engineering"](https://worrydream.com/refs/Brooks_1986_-_No_Silver_Bullet.pdf), which Brooks wrote in the '80s.

The exact claims about what productivity improvements are possible from what sources are probably debatable - the text itself specifically refers to not getting an "order of magnitude" improvement in productivity from a single source "within a decade". Since then, we've had many, many years of improvement in languages, tooling and people from DORA telling us how to measure stuff, and obviously everyone is currently getting very excited about Generative AI. It's all a bit hard to align to specific claims and I'm not particularly bothered to try.

The more abstract and more useful thing that I frequently revisit though is the distinction between complexity that is "Essential" - an irreducible part of the problem you need to solve - and "Accidental" - a factor of the tools, processes etc that you use to try and create that solution. The latter type of complexity you should try and resolve out through better tooling, better design etc - the former you can handle better or worse (basically, create more or less "noise" and accidental complexity around it), but as implied by it being _Essential_, you can't get rid of it in any meaningful way.

This concept continues to be very useful to me - a good lens for design review of others' work, or planning one's own, is to get as clear as picture as possible of what the essential complexity of a problem is. Similar to [Amdahl's Law](https://en.wikipedia.org/wiki/Amdahl%27s_law), it should give a strong intuition of what the maximum improvement you can expect is - removing all the parts which don't address the core complexity which the whole value of your work is in addressing.

The essential complexity **can** be business logic and the accidental parts technical, but it's definitely possible to view it on multiple levels - for example if you _essentially_ need to scale processing across different units of infrastructure to take the required load, certain nasty distributed-systems problems become part of the essential complexity - even if you lean on an existing component to handle some of the dist-sys implementation you still need to understand the specific failure states of the system, whereas rolling that component from scratch yourself or using a poorly-designed client library would add accidental complexity. Conversely, if you are distributing your workload to preemptively add scalability for workloads you may never actually have to support - dist-sys implementation problems are firmly in the Accidental class and you should do something basic and monolithic at least to start with.

-----------------------------------------------------------------------------------------------------------------------------------------------

 \* _Incidentally, [the If Books Could Kill podcast](https://podcasts.apple.com/us/podcast/if-books-could-kill/id1651876897) is interesting in considering the toxic effects of this in certain cases, although they're surely not always right and have a distinct political flavour that isn't exactly wrong but is definitely to the left of where I land on a lot of issues. If you're working in tech, you're almost certainly exposed to enough well-expressed right-libertarian talking-points that you can listen in without being at any risk of losing track of other perspectives._
