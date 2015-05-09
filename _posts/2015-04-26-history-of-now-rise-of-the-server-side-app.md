---
layout:     post
title:      "Rise of The Server Side \"App\""
subtitle:   "The History (and Future) of Now"
date:       2015-04-26 12:00:00
author:     "John Kleijn"
header-img: "img/lego.jpg"
---

Being Presumptuous
-----------


I loved Lego as a kid. I think most programmers over 25 did. It allowed
us to create imaginative things in a very short time. And historically,
having "building blocks" has been very helpful: try building a pyramid
by sticking dung to a framework of twigs and branches.

The finer points of concerns like cohesion, decoupling, abstraction,
encapsulation and modularity aside, basically we developers have been
trying to make code into Lego all along. There is no single programming
platform as ubiquitous as Lego, as the needs of the adult world are a
little more complex than the need to create of infants, giving rise to
the popularity of networked APIs. Hiding complexity behind interfaces,
whether using a native API or one that’s network based, has worked,
and is somewhat reminiscent of building with Lego. Or maybe an odd mix
of Lego, Duplo and Knex. In any case, the world has an insatiable hunger
for *real* Lego-like solutions. That killer solution to fully modular
applications in "the cloud"...

### PaaS Will Dominate: Resistance Is Futile

You’ve probably heard the term "PaaS", and/or heard of Heroku. This service
gained a lot of popularity since its inception in 2007. Since then there
has been a boom in PaaS providers (too many to list), attracting even
the big boys: Google (Google App Engine, 2008), Microsoft
(Windows/Microsoft Azure, 2010) and IBM (IBM SoftLayer, 2013). There are
differences between how different vendors handle the technical details,
but the common denominator is that PaaS applications run as isolated
instances (in whatever form) on the host infrastructure. Running web
applications on a PaaS has many advantages: it’s scalable, fast to
deploy and upgrade, reduces cost and eliminates server admin tasks. Some
offerings include a Continuous Deployment stack, most if not all offer
ready-to-use components offering storage, search and indexing, and even
Big Data tooling and Business Intelligence services. Building Web
applications this way makes it easy to create middleware applications,
or more generally
design [Microservices](http://martinfowler.com/articles/microservices.html). Promoting
further modularity, more fine grained and immediate capacity up and down
scaling.

> Aside: I highly recommend that anyone interested in developing apps
for a PaaS platform read ["The Twelve-Factor App"](http://12factor.net/).

### Meanwhile, In The Office Space

The "enterprise" is slow to adapt. In part because of vendor lock-in by
companies like IBM, Microsoft, Oracle, SAP, Cisco, EMC (VMware), and HP.
One of those is being an extra nuisance. Who else than our old nemesis,
the company that brought us IE6 and made every Web developer cry tears
of despair. Microsoft may have [already lost the game](http://www.paulgraham.com/microsoft.html) back around 2005 (a year
after Gmail was released), it still dominates the desktop market with
almost [80%](http://gs.statcounter.com/#desktop-os-US-monthly-201501-201503-bar) in the U.S., over [85%](http://gs.statcounter.com/#desktop-os-eu-monthly-201501-201503-bar)
in Europe and a whopping [96.5%](http://gs.statcounter.com/#desktop-os-CN-monthly-201501-201503-bar) in China. I wouldn’t say 
[corporations are people](http://www.theatlantic.com/business/archive/2012/01/citizens-united-v-fec-turns-2-and-its-still-wrong/251706/),
but I would certainly argue that people work there. So called
"Enterprise" vendors give them what they know, a Windows-based UI. This
runs deep, and Microsoft is going to ride that bull onto its inevitable
demise. Presumably, a lot of companies and institutions outside of the
U.S. are uneasy with using a hosting partner subject to U.S. law. Who
can blame them, especially after Snowden leaked what everybody already
knew: the U.S. government will do whatever is in the best interest of
the U.S. And "a big FU to the rest of the world, [even our so-called close
allies](http://usnews.nbcnews.com/_news/2014/01/26/22454373-snowden-says-nsa-engages-in-industrial-espionage-german-tv?lite)".
Of course, U.S. companies are not a fan of NSA practices either, and
everyone is worried about corporate espionage and random acts of
terrorism. The point is that corporations, worldwide, are not standing
in line to throw their IT infrastructure "off-premises", unless they
have a trusted local provider.

![](/img/growth-of-cloud-computing.jpg)
<span class="caption text-muted">From a ZDNet blog post by Dion Hinchcliffe which has disappeared</span>

#### The OpenStack Revolution

Back in 2010, [Rackspace](http://www.rackspace.com/) and NASA started a
little project called "OpenStack". Five years later, the open source
IaaS solution has massive corporate support. To quote Wikipedia:

> More than 200 companies have joined the project, including Acelio,
> Arista Networks, AT&T, AMD, Avaya, Canonical, Cisco, Citrix, Dell,
> Dreamhost, EMC, Ericsson, Go Daddy, Hewlett-Packard, Huawei, IBM,
> Intel, Internap, Juniper Networks, Mellanox, Mirantis, NEC, NetApp,
> Nexenta, Oracle, PLUMgrid, Pure Storage, Qosmos, Red Hat, SolidFire,
> SUSE Linux, VMware, VMTurbo and Yahoo!.

What the fuss is all about? OpenStack provides a suite of components
integrating scalable, redundant storage and virtual machines with a
**hypervisor of choice:** KVM, Xen, VMware, and even the Microsofts
Windows-based Hyper-V. And it does this using an **open source** code
base that can be **self-hosted**. Since then, more components have been
added to create a more complete environment. Rackspace originally
created OpenStack to compete with Amazon
([AWS](https://aws.amazon.com/)), and soon after decided the best way to
do that would be [to provide a transparant
alternative](http://www.eweek.com/cloud/rackspace-openstack-bet-is-paying-off.html).

> "Amazon is a very well-known technology, but it’s still their
> technology; it’s a black box," Curry said. "OpenStack is a known
> standard; anyone that wants to use OpenStack has free access to it and
> they can see the code."

#### VMware Has Identity Crisis

OpenStack is [going head to head](https://www.mirantis.com/blog/cloud-prizefight-vmware-vs-openstack/)
with VMware’s own IaaS solution, vCloud, and [may have
joined](https://gigaom.com/2012/09/07/finally-vmware-joins-the-openstack-foundation-this-time-for-real/)
the OpenStack Foundation in an attempt to stay ahead, or worse. It might
even use some [plays from Microsofts
book](http://www.computerworlduk.com/blogs/open-enterprise/how-microsoft-fought-true-open-standards-i-3569201/).
The same could be said for IBM or even Red Hat. In the end, I doubt it
will really matter. OpenStack is extremely well backed; proprietary IaaS
solutions are going down, eventually. VMware *has* flirted with open
source before, most notably by acquiring
[SpringSource](http://spring.io/), the company behind the popular Java
framework, and by developing [Cloud
Foundry](http://cloudfoundry.org/index.html), an open source PaaS
solution. Parent company EMC, having acquired Agile Methodology
consultants and developers [Pivotal Labs](http://pivotallabs.com/), has
since decided that Pivotal would be a more [appropriate
home](https://gigaom.com/2012/11/27/remember-that-vmware-spin-off-its-baaa-aack/) for
its "open" endeavors than VMware. EMC has been smarter than Oracle in
this regard. How are you liking open source, Oracle? ;)

> "VMware made waves this summer when it talked up a paid commercial
> version of its Cloud Foundry open-source PaaS, and that ruffled
> feathers among many of the partners VMware had encouraged to build
> PaaSes of their own based on Cloud Foundry. By offloading Cloud
> Foundry, VMware can avoid that distraction."

#### Red Hat Throws In Its Open Source PaaS Solution

But VMware’s move may have come too late. Four years ago, May 2011, Red
Hat went to market with OpenShift. OpenShift was originally a fully
hosted IaaS and PaaS solution. It didn’t take off until they provided
on-premises solutions, and released the code as the open source
"OpenShift Origin". *It doesn’t show in this graph, but head over to
Google Trends to see the correlation between news headlines and the
spike of interest in OpenShift*. The moment Red Hat
[announced](http://www.zdnet.com/article/red-hat-to-debut-openshift-paas-solutions-for-on-premise-enterprise-use-soon/)
it would offer a "on-premises" solution, interest in Cloud Foundry
waned. The move to Pivotal was late and unconvincing. Not surprisingly,
most of the interest comes from companies outside of the U.S., China
leading the flock.

#### Google Supports Open Source App Engine Compatible Project

Contrary to Red Hat and EMC, Google has not open sourced the code behind
its PaaS solution: [Google App
Engine](https://cloud.google.com/appengine/). Maybe the platform code
relies on exotic Google specific infrastructure details, or maybe Google
just didn’t want to give away its hand, and with it its USP of "Hosted
by Google, so you know it’s fast, massive, and shiny". Most likely, it
is because Google is targeting the same crowd as Heroku: smaller
companies looking for solutions that are both advanced and
cost-effective. No need to open source anything, no need to provide
on-premises solutions. Google is not really an "enterprise cloud"
player. 

But hey, if people really want to run App Engine apps on-premises, or
are comforted by the idea of having that option, Google is all for it.
Coming out of a research project by the U.S. National Science
Foundation, but funded by IBM and Google,
[AppScale](http://www.appscale.com/) provides just that: portability for
App Engine apps across different IaaS solutions. As always, Google is
thinking long-term and cares more about you using their technology than
you paying them money (right now). Luckily, interest in Google App
Engine has been steadily declining. It doesn’t look like Google is going
to win this one. But then Google gets in the container game (see below)
by developing [Kubernetes](http://kubernetes.io/), a technology juicy
enough for Red Hat to jump on it for the upcoming OpenShift 3 release.
And of course, it offers [hosting for
containers](https://cloud.google.com/container-engine/) driven by
Kubernetes. Google is not just going to roll over and die.

#### Heroku Sells Out

That brave startup from 2007, breaking new ground and empowering
startups, sold out to Salesforce.com in 2010. Not many seemed to care
though, as Heroku continues to grow. Salesforce fairly recently added
"Heroku Enterprise" to its portfolio, but it’s targeted purely at
customers of their CRM package. Heroku is still on top in startup
circles, but that is going to change very soon…

### The "New" Kid

Remember those "slumlord hosting" companies back in the early years of
this century? You would get a [Virtuozzo](http://www.parallels.com/)
"virtual machine", which was actually a container to provide isolation,
sharing the kernel of the host machine. These servers were notoriously
overbooked, undeservingly giving Virtuozzo a bad rep. In 2005, an open
source version was released by parent company Parallels, called
[OpenVZ](http://openvz.org/). This required custom Linux kernels, but
Paralells teamed up with the Linux community and Google to release
built-in containers 3 years later: LXC (Linux Containers). Cloud hosting
company [dotCloud](https://www.dotcloud.com/) saw the potential and
their solution, originally built for in-house use was released as open
source in early 2013, giving birth to Docker. 

In a very short time, Docker has grown from a side project to one of the two most raved-about
developments in "Cloud Land" (alongside OpenStack). Despite
[warnings from its creators](https://blog.docker.com/2013/08/getting-to-docker-1-0/) that
they did not consider Docker production-ready, A-list
companies like eBay and again Rackspace [jumped on
Docker](https://blog.docker.com/2013/08/docker-hack-day-6-lightning-talks/)
like lions on a steak. Docker’s aim is quite a bit broader than LXC (and
uses its own libcontainer in place of LXC since version 0.9), but at its
core has a more modest scope than full blown PaaS solutions. 

Simply put,
Docker provides a standard way to run PaaS**-style** apps, not bogged
down by any vendor’s attempt to dominate the future of Web computing.
Similar to OpenStack in that respect. Understandably, client companies
and especially their developers are psyched. Enterprise PaaS providers
are doing what they can to get on the docker train in time, including
[Microsoft](http://azure.microsoft.com/blog/2014/10/15/new-windows-server-containers-and-azure-support-for-docker/),
[Red Hat](http://www.openshift.org/#v3),
and [IBM](http://www-03.ibm.com/press/us/en/pressrelease/45597.wss). But
also new PaaS solutions, such as [Deis](http://deis.io/), used and
developed by startup [OpDemand](http://opdemand.com/), then bought
by [Engine Yard](https://www.engineyard.com/engine-yard-and-deis), a
company in the business even before Heroku. But Docker has a wider
applicability than any specific PaaS platform. You don’t need all the
entrails of PaaS hosting for Docker to be useful. The lightweight
containers also make excellent Continuous Integration and Deployment
tools, which is relatively easy to set up. 

Making developers not in the position to use a PaaS platform in combination with a CD stack, drool
all over Docker. And to seal the deal, Docker’s "Registry" is a lot like
the application level [package managers](https://en.wikipedia.org/wiki/List_of_software_package_management_systems#Application-level_package_managers)
developers already use and love. On your average PaaS platform there’s
something more analogous to the App Store or Google Play.  

### What’s To Come?

![Mah Crystal Ball](/img/crystal-ball.jpg)

Let’s start with the obvious predictions: both OpenStack and Docker are
going to the skies. They have both the business and developers behind
them: there is no stopping these two any time soon. Whether full private
PaaS solutions will take off is less certain. There is a challenger to
Dockers rise: early Docker adopter and
contributor [CoreOS](https://coreos.com/) has developed an alternative
to Docker, initially named Rocket, later renamed "rkt". Pronounced
pretty much the same. Design wise, it offers some
[advantages](https://coreos.com/blog/rocket/) over Docker, and CoreOS
itself is certainly an interesting option for running Docker containers.
CoreOS is unlikely to drop Docker support any time soon so for rkt to
replace Docker, CoreOS would first have to become the undisputed
superior way of running Docker containers. Then maybe developers will
slowly move to rkt, if by that time the network effect hasn’t already
made that too much hassle. 

But there are also alternatives to CoreOS, for one [Project Atomic](http://www.projectatomic.io/docs/introduction/), 
which is what Red Hat uses for OpenShift 3. Project Atomic in turn relies on
Kubernetes, developed by Google. Engine Yard is still small, and relies
on AWS for infrastructure, but OpenShift still has Cloud Foundry to
contest with. For a while at least. With Deis, Engine Yard hopes to
ride the Docker train early (and Web developing Twitter has noticed),
finally taking off. OpenShift will switch to Docker (as it’s a
downstream dependency of Project Atomic) in June, which may already be
too late in this game. I might be wrong on this one, but hey where’s the
fun in only obvious predictions. Google is probably not going to push
very hard on its own Container Engine service for a while. They label it
alpha, at most it’ll attract some early adopters fond of Google. They’ll
probably let their Kubernetes project mature a bit first. It doesn’t
need to make money, it needs it foot in the door.

What about Heroku? Doomed, unless they fully integrate Docker very, very
soon. Which is unlikely, unless it can somehow run "Dyno’s" and
containers alongside each other, effortlessly. Even then, their growth
potential is limited. Goodbye Heroku. Nodejitsu already
[bailed](https://blog.nodejitsu.com/nodejitsu-joins-godaddy/) in
Februari, Google App Engine will soon follow. And IBM, Microsoft? I
don’t see much happening there either way. They’ll probably keep trying
for few more years, they can afford it. Rackspace is likely to keep
growing at a decent pace. So will PaaS become the de-facto standard
everywhere? Probably not in the near feature. Containers such as Docker
and Rocket are on a much more likely trajectory of fast ubiquitousness,
so are Microservices. These, and not PaaS, are the Lego developers have
been waiting for. Maybe we could stop using the term PaaS too, that’d be
nice.

Thanks for reading.

##### Attribution
 * Original header image by [Benjamin Esham](https://www.flickr.com/photos/bdesham/)