---
layout:     post
title:      "Sprints in Web Development Considered Harmful"
subtitle:   "Stop running, start delivering"
date:       2013-12-30 12:00:00
author:     "John Kleijn"
header-img: "img/bible.jpg"
---

### Don’t get me wrong…

Lets start by putting aside some of the preconceptions you might have
about this post after reading the title. Firstly, I am not saying Agile
Development or Scrum as a whole is “bad”.  On the contrary, I contest
the use of sprints for many of the same reasons Agile Manifesto signees
contested traditional waterfall methods. The “old ways” are inflexible,
give a false sense of predictability or provide predictability at the
expense of efficiency and/or time-to-market.

But the Agile umbrella does not give clear guidance when trying to give
body to your product development strategy. Nor is it, in my opinion,
analogous with flexibility, despite its name.  There’s stuff like AUP
and DSDM, methodologies claiming to be “Agile”, a proposition which only
has merit when looking through eyes blinded by the complexity of RUP.
Granted, Scrum (by itself) is not a complete product development
framework, and I’m sure more elaborate methodologies work for many
organizations on some level, but I’m not a fan.

And of course, there’s Kanban and aforementioned Scrum. The latter has
become extremely widespread, even a de-facto standard. Or rather: it has
become the standard to claim Scrum development. At least in my circles,
I’m sure there are plenty of companies not *pretending* to do Scrum. I
of course stress *pretending* because very little companies actually
implement Scrum. It has only a few rules but if you don’t follow them
strictly technically you are not doing Scrum, and there’s no sense in
pretending: it crumbles like a house of cards if you ignore but one of
these rules in favor of convenience. That is to say: if you question or
ignore one of them, you should question them all, properly.

The concept of  Iterative Development, more precisely the concept of and
practice of having “sprints” is one of the properties of Scrum that I
believe you should question. First of all, I dislike the name “sprint”,
it implies we should be running, all the time. When a sprint ends, here
comes the next one, get ready to start tripping over your own legs
again. No breaks, just running. Semantics, yes, but I value semantics.
But of course the naming is not what makes sprints, or iterations in the
now conventional sense, harmful.

### So why *are* sprints “bad”®?

Quite a number of reasons, actually…

#### Sprints create an artificial unit of work

Lets take some features, see how many think we can fit into a period of
two or three weeks, and tell the world that we will be demonstrating the
fruits of our labor at the end of this period. Backlog grooming should
ensure the features with the highest business value are on top (a
practice which is often neglected), but what about that little window of
2 days that is left? Do we give the team 2 days off, do we plan the
sprint 2 days shorter, or do we try to cram in some random items from
the backlog to make sure the team is fully loaded? Usually the  latter
happens. Sprints also invite sequential coupling of features. Features
are *supposed* to be independent, so that you can drop a feature from a
sprint when needed. But this takes effort and thought and if the
features are in the same sprint, why should I care, right? Just be a
good development team and finish all of the stories and everything will
be peachy.

#### Sprints set teams up for failure

Sprint planning can easily become too ambitious, usually due to
stakeholder pressure and developer overconfidence (“we got this,
right?”). I’d be lying if I said that never happens with my own
estimations. Not completing all the features planned for a sprint should
be a fact of life and not something that invokes negative sentiment, but
in practice a sprint not fully completed is experienced as a failure, by
both the development team and the stakeholders. Even if 80% of features
are completed, and done well, that 20% can totally knock down
stakeholder confidence and team spirits. You ran and you ran, and in the
end your best fell short of stakeholder expectations. The past 3 weeks
are just another nail in your coffin, whether death is analogous to
getting fired or burning out. Even when you do make it, your velocity
goes up, and with it stakeholder expectations. Which is fine, as long
those expectations are not translated directly to external commitments,
also known as “deadlines”. With time, practice and stability within a
team, predictability will go up, and sprints will fail less often. It’s
just that it’s a little too easy to cram in that little bit extra, in
particular because stakeholders will have to wait weeks before reaping
any benefit. And in general, a Product Owner will be a mid-level manager
of sorts, held responsible for making sure those external commitments
come to be.

![](/img/pipmo-whip.jpg)
<span class="caption text-muted">So does your PIPMO</span>

Especially harmful are the situations where the expected velocity is
baseless, based on a deadline, or where velocity is a capacity measure
which translates into hours. Your
Product-slash-Iteration-slash-Project-Manager-slash-Owner (P/I/PM/O, or
just “PIPMO”) likes to speculate using hours, they will usually continue
to do so whether your team estimated in story points or not. They’ll
have a nice Excel sheet, where they guesstimate that 1 story point
equals 3.14159265359 hours, with 80% efficiency and x developers that’s
y hours, divide by Pi, that means we can cram in these stories. Or
worse: that means we need “y” more developers. And no, this has nothing
to do with Scrum nor sprints *as intended*, but it is relevant to why
Sprints are failing in real life.
 

#### Sprint failure breeds distrust

When uncertainty is high, developers will not be able to (truthfully)
provide the answers stakeholders want to hear. A a result your
PIPMO might take matters into his own hands, resorting to techniques
like the above, and the spiraling descend into a deep pit of mutual
distrust kicks off. Even Uncle Bob is [seeing the pattern](http://www.youtube.com/watch?v=OIHvp7WzuH0&list=PLE7AF2F360F1C0BF3#t=890).

Then there’s the sprint, the whole of which the team has to commit to.
If the team has a positive attitude, thumbs will go up. But if a feature
or two turns out to be more work than estimated, pressure will likely be
applied to still finish every last feature in the sprint, especially if
the sprint is coupled to a release. Every time that happens, the
commitment will be more hesitant. I don’t believe applying a lot of
pressure leads to better results, it generally leads to taking
shortcuts, to developers looking to find loopholes in the QA
infrastructure. I doubt this is a very conscious process: when the walls
come in to crush you, you instinctively try to find any way out you can.
Sprints impose commitment on a relatively large scope, and you give
commitment “as a team”. The idea is that the team helps each other to
live up to the created expectations. But whether the team itself created
these expectations or not, if the team fails it starts to distrust its
own: “why do I always have to be the one to fix things”, “I worked late
so that we can make this deadline, when Susan is clearly only here for
her paycheck”, and so on. Granted this is a possible concern whenever
professionals are dependent on each other, Sprints aggravate this issue
by causing unneeded dependencies. Dependencies are bad, hmkay?

### Sprints create process overhead

A Sprint planning meeting is prescribed to take no less than 8 hours.
I’ve seen it take twice that. Then another 7 or 8 for Sprint Review and
Retrospective. Basically two working days per sprint. Let me get in my
PIPMO chair and do the math: a Sprint of three weeks has 15 working days
so just sprint meetings add 13.33% of process overhead. For a 2 week
sprint, 20%.  Add to that the overhead not directly related to sprints
and the PIPMO in me starts wondering how we get any work done at all.

Not to mention meetings this long are notoriously ineffective. Most
people know this, but Scrum prescribes this so who are we to question
the word of Scrum?

### Sprints create inefficient teams

A development team is **not**  like a team in a team sport, no matter
how appealing the analogy is. A rugby team does not have 12 balls, and
in a development team it is not acceptable to chill out in the back
until the ball comes your way. In an ideal world, you pick a story off
the the top of the board and finish it with the whole team before moving
on to the next. In practice, this is rarely practical. When you have
team members with very similar skill-sets working on the same story you
can easily get in each others way or do work twice because the division
between tasks turned out to be less apparent than originally thought.
When you have specialists, you create a lot of idle time if you wait for
the whole story to complete before moving on to the next. Because of
these impracticabilities, usually quite a number of stories is worked on
at the same time: there’s more than one ball in the field.

![](/img/rugby-scrum.jpg)
<span class="caption text-muted">Also, this just doesn't look familiar</span>

I’d say a development team should be more like a speed skating team, or
any other individual sports team. You should care about each others
results, and in the end the team score does count, but you have a focus
on individual performance. Critics will argue that the performance of
the team is more important than that of individuals, and they are right.
That is, getting things done is more important than individual
performance. Teamwork is extremely important, exactly because employees
are *always* dependent on one another. But dependency is not something
to promote, is it?

Sure, the team should be self-organizing, and a team might correct its
own when someone is being lazy or screwing up, but it can be very
forgiving as well, especially if you have a few introverts on the team.
Within a sprint there are many things you can do to address individual
responsibility (I’ve tried many variations). That just adds an another
opaque layer between the development team and other stakeholders
(perpetuates the division). But worse, it adds more process overhead.

I realize it might seem like I am depicting the
average developer as a lazy SOB who sits on the sideline as a small
number of others do all the work. I don’t believe laziness has anything
to do with it. In fact I think the few that take on most of the work
should be curtailed from doing so. Others might be inclined to let the
few take on more and more, because of the perception that they can do it
faster, better, whatever. As long as a Sprint is not allowed to fail,
individuals do not get room to learn, if the few pick up the slack to

prevent the Sprint from failing. I see how this might obscure the point
of this post for anyone lucky enough not to have experienced the woes of
wildly varying competence and/or involvement within a team. If this is
somehow unfamiliar to you, ignore and read on.

![](/img/veteran.jpg)
<span class="caption text-muted">Save a sprint, get a medal but lose the war</span>

#### Sprints inhibit “release often”

Probably the most important point I am trying to make. If stories were
truly independent, and we finished them one by one, why should releasing
the feature wait for the sprint to end? When finished means shippable,
you could. But generally the focus is on a sprint being shippable, not
whatever it contains. And as I stated before, those preconditions are
rarely true, in part because the practice of “Sprinting” obscures their
necessity. And releasing while in a sprint creates a risk of more
interruptions: what if after a feature goes live and despite your
rigorous QA processes, has issues? Whether they’re bugs or
misconceptions about the needed functionality, this would probably cause
a good deal of disruption to the development process.

There are probably cases where stakeholders want to wait to make new
features (fully) public, for some strategic reason. But releasing
something and exposing it to the public doesn’t need to be the same
thing, and for example exposing it to specific targets only  opens up
opportunities for real-world testing. I can’t think of one valid reason
to wait for something to go live under the conditions that are required
for a successful sprint, except for the fact that it is still in a
sprint. How’s that for a paradox.

#### Sprints do not work well with (partly) outsourced teams

I have been put in this situation 4 times now, in a period of 5-6 years
or so: being the technical lead for a team that is distributed across
different locations. Some teams were mixed between company employees and
outsourced capacity. What happens is the CFO/CEO or whoever has to pay
the bills, and by extension the PIPMO, wants a clear measure of how much
bang they are getting for their buck. They want the outsourced
developers to be accountable, and their results to be measurable. I can
without a doubt say that this does NOT work when you put them in the
same sprint as in-house developers or differently sourced developers.
And parallelizing sprints has its own issues, specifically overhead and
inequality in determining priority. You’ll hopefully see this after
reading the next section.

#### Sprints do not parallelize well with operational needs

Two weeks is already considered short for a Sprint, but stakeholders
rarely want to wait two or even three weeks for some business
optimization to go live, or some bug that is costing them money, to be
fixed. And rightly so: this is causing the company, the same company
that pays your salary or fee, revenue loss. This means, when living by
the word of Scrum, they want (at least) a second development stream; one
with shorter iterations.

There is no way to do this efficiently when using Scrum sprints. You can
have two dedicated teams on each stream, if you are in that luxurious
position. But because of the difference in length, there’s no way you
can make sure the capacity is being used where it is needed most. When
you have multiple streams, you have multiple backlogs, at the very least
for the duration of the stream with the longest iterations. You can’t
just exchange items between teams. And exchanging people between streams
doesn’t work very well either, both for the same reason: the persons
that are suddenly expected to perform a task are missing the context.

Context switching is extremely disruptive and in my opinion one of the
main causes of inefficiency in development. One PIPMO demonstrated his
failure of understanding of this fact when claiming: “yes, but you and
me do it all the time”. However true, I still don’t think that in any
way negates its negative effects. It takes focus to perform complex
tasks well, especially tasks with a lot of context. The more context,
the focus and contiguous blocks of time is needed.

The same PIPMO came up with the following solution to handling multiple
streams: estimate the minor iteration (then called “Customer Sprint”,
but it goes by many names) in Story Points, and take out Stories that
amount to the same from the “regular sprint”. Nominally this makes
perfect sense: the expected velocity stays the same. But it only works
when (again) Stories in the sprint are truly independent, and it doesn’t
address the issue of context switching. Not to mention every minor
iteration the major iteration was disrupted.

So then you are left with but one option: merging the streams. Which
presents two rather unappealing implementation alternatives: either you
try to cram a full Scrum iteration with all the associated overhead into
a shorter period, say a week, or you tell stakeholders of the more
pressing, smaller issues to go stuff it until the Sprint is done.

Or, you can just get rid of sprints.

### A World Without Sprints: Rainbows and Unicorns

![](/img/double-rainbow.jpg)
<span class="caption text-muted">Yes it's a double rainbow, try not to freak out</span>

#### Scrum Level 3

Something I stumbled across while looking for opinions on this subject
is the concept of Scrum Levels. Apparently these are being thought at
some CSM courses. Mine did not cover this, but I did find [a
presentation](http://www.agilesparks.com/files/Scrum_levels_Danko_Danny_Kovatch.ppt)
explaining what these Scrum “levels” entail. I’ll summarize:

-   Level 0: waterfall
-   Level 1: Scrumfall, basically only development takes part in sprints
-   Level 2: Plain by-the-book Scrum
-   Level 3: Shippable at any time using automation

The funny thing is that at level 3, the author claims “no real meaning
for sprints”. But while hanging on to the concept of sprints, apparently
just for the sake of being able to call it proper Scrum. To be fair, the
author does mention Kanban on the Level 3 slide. Personally, I think
Level 3 is just hogwash to keep people with the Church of Scrum instead
of moving on to greener pastures. Call me a cynic.

#### Kanban

Once you drop Sprints, Scrum starts to look a whole lot like Kanban. Or
rather, what people mean when they refer to Kanban in a Software
Development context.

Just in case you’re not familiar with Kanban, it’s a system for “lean
manufacturing”, developed by Toyota. Then someone apparently found a
Software Product Development chain pretty much analogous to a big ol’
car factory, and adapted the system for the former. Don’t ask me how or
why exactly that happened, possibly David Anderson had something to do
with it with his book, or maybe it happened way before that in some
board room where they looked with with envy at the efficiency of a lean
factory. Certainly “lean” has found its way into pretty much every
discipline of pretty much every industry. In the end, who cares. Some
Scrum evangelists even argue: [Kanban is NOT for Software Development,
but
Scrum is!](http://scrumcrazy.wordpress.com/2013/02/04/kanban-vs-scrum-kanban-is-not-for-software-development-but-scrum-is/ "Kanban vs. Scrum:  Kanban is NOT for Software Development, but Scrum is!").
Again, who cares. If it works, it works. And it does work,
or *can* work.

Kanban has a few properties that give it an edge over Scrum:

-   Firstly of course: no sprints. Features get knocked off one by one
    (partly parallel for the same reasons as mentioned above, but
    despite focus on WiP this is actually less of an issue than when
    using sprints), without that unnecessary devil’s brain child.
-   Kanban calls for “start with what you do now”, and promotes change
    with minimal resistance. This makes it much easier to adopt by an
    organisation.
-   By extension, Kanban (technically the Kanban *method*) does not
    invent new roles and responsibilities. Your PIPMO can finally return
    to just being a PM. Or simply a manager, IT-process facilitator,
    whatever pleases him most. Not to say such a role becomes
    irrelevant, but it is much easier for our former PIPMO to find a
    position where he can both live up to upper management expectations,
    while actually being in service of the production team as opposed to
    being a disruptive factor or oppressive force.

Because Kanban does not have sprints, features become deliverable
(mostly) one by one. There’s no freakin’ “hardening” (or worse
“hardening sprint” — eeek), done means done. This requires lightening
fast Quality Assurance and Management on multiple levels, or you’ll end
up with insane overhead (release managers, full-time testers, and a
crazy amount of human enforced procedures).

So to make Kanban work, you need to be able to do Continuous Delivery,
or preferably, Continuous Deployment. There no such thing as a Release
Sprint, as there are no Sprints. It takes considerable effort to get the
infrastructure in place to ensure high quality and fast delivery, but
that’s mostly a one-time investment. “First time right”, a credo from
the Dark Side, suddenly applies to development as well, as it moves from
being project-based to just another part of operations.  As Vader said:
“You underestimate the Power of the Dark Side, suckah” (paraphrased).

Now  you can set an example for other operational departments, show them
what “Operational Excellence” really means, and you can fulfill their
needs in a timely fashion instead of telling them to stuff it because of
some poorly justifiable process restriction. There is only one stream,
and project or operational, everything goes on the same board, *the*
board. The urgency of all tasks can be judged equal.

Of course this is wildly optimistic. Estimations will be made, at times
they will be optimistic and stakeholders will be disappointed. But at
least failures and successes will be on a case-by-case basis. You win
some, you lose some. Whole features can be completed by a small
cross-section of the production team, allowing more objective evaluation
of individual competence, more independence and self-determination for
team members.

#### A Temptation From the Dark Side: Scrum-Ban

But the Church of Scrum is not letting go of its followers that easy.
Kanban is a lot less restrictive than Scrum, and Scrum certainly has
elements that are usable when implementing Kanban. Personally I don’t
believe in Scrum-ban as methodology in its own right and look at it much
like I look at Scrum Level 3.  To be honest I’ve read so many different
descriptions of what it should entail that I regard it as a meaningless
handle. Just employ Kanban, drop sprints, and if there’s anything in
Scrum that you, after careful consideration still find useful, why not.
A prime example is backlog grooming. You’ll need that even more with
Kanban, in my opinion. Ironically, backlog grooming was a bit of an
afterthought in Scrum, but that’s beside the point.

![](/img/tommy-vader.jpg)
<span class="caption text-muted">They're in your senate, even</span>

### In conclusion

I think your most important take-away from this rant should be this:
when you build your own products involving development, those processes
are operational processes. And operational processes are continuous, not
iterative.

So to reflect on the title of this post, I guess that nuance should be
implied; if your business creates software on a project basis, Scrum
sprints could possibly (somehow) be a better fit. Even then I would at
least try to avoid them, and very thoroughly and critically evaluate WHY
you think you need them.

I realize, BTW, that this post was lacking a bit in providing concrete
guidance towards implementing Kanban in your own organisation. But there
are already a lot of sources out there to help you with that, and
considering the unrestricted nature of Kanban and endless variation
possibilities. Hopefully I have at the very least made you question Scrum by-the-book
and sparked some interest for Kanban.


Thanks for reading.

##### Attribution
 * Darth Vader pic is actually U.S. Senator Tommy Williams, picture taken from [theatlantic.com](http://www.theatlantic.com/)