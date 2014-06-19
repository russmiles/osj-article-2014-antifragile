# Microservices in Stark Relief

## What matters?

For the past 14 years we’ve done a wonderful job of creating processes and embracing practices that make our organisations and workloads more ‘agile’. Now those processes are beginning to be embraced across all areas of modern successful organisations, and that’s also an inevitable result of the need to compete and innovate faster in the modern marketplace. 

Innovation is becoming the norm, and agility and agile processes have now come of age and are leading the way in how companies can compete. However all is not blissful on mount agility, there’s a skeleton in the closet and it’s a big enough skeleton that it has the potential to blow the whole escapade sky high…

Let’s meet that skeleton…

## Where agility ends…

It’s sprint 10 and you’re feeling good. The software is in good shape, the customer is happy and there are birds in the trees singing just for you. Life could not be better.

 You head in to your daily standup and, like any sane individual, the first thing you do is sit down and get set for chatting with your peers on the challenges of the day. It’s at that moment that the world ends…

It starts with a perfectly innocuous phrase from your product owner (or anyone else who is responsible for directing the development of your product), it starts with “I’d just like one small change…”

You catch your breath. You hope you misheard, but apparently not. Then your emotions kick into gear.

“How dare you ask for a change?”, “What do you mean you changed your mind?!”, “We can cancel the sprint you know…”. Anger overrides reason for a few moments, before transitioning to…

Ugh. Guilt. You see, you know deep down that you’re supposed to be an ‘agile’ software developer. That’s what all that budget for Scrum Master training was for. Worse than that, you know that at the core of being agile is a single principle that tends to be forgotten; something crucially important but that gets lost in the majority of other messages around the ossifying manifestos. You see, you’re supposed to “Embrace Change”…

The problem is not that you needed more time. It is not that you could have easily avoided the problem with better foreknowledge. The problem is what we’ll call “The Elephant in the Standup”, a term originally coined by Rich Hickey.

The Elephant is all the code your wrote yesterday. It is all the decisions and assumptions that you baked into your architectural and design decisions. It is all the legacy that is fundamentally in conflict with reality today.

We can do better, but first we need to dispel some illusions. Particularly, the illusion of perfection and that you can get things ‘right’.

## A Different Architecture, a Different Philosophy

"We build software to deliver ideal solutions to have the right impact and deliver the right value to the world."

At first glance, this statement feels correct. Who wouldn't want to build the ideal solution to deliver the right value? The problem is in the words "ideal" and "right".

The Theory of Ideas goes right back to Plato, student and literarily embellishing mouth peace to the legendary Socrates. This theory, in gross summary, conceptualises perfect ideas as 'forms' that have their imperfect representation here on the mundane Earth. 

Plato talked of a Philosopher guiding a two-horsed chariot towards the ethereal plane of Forms, one horse being his reason driving him upwards, the other horse his own vices and earthly appetites that will drag him back down to the unsatisfactory world of the 'real'.

![Plato, don't build software like him!](images/plato-head-shot.jpg)

Plato popularised for millennia the idea of the perfect and that it was worth striving for, and like idiots we all bought it. Excellence, Arete, was the goal, and it was attainable with the right amount of reason and thought.

All this would be academic (ironically, the Academy was Plato's school in Ancient Athens; now academic is a term of derision in many quarters, capturing a quaint image of a leather-path-wearing professor, hiding behind a desk and shuffling research reports that will never have an impact on the world) except that software development is an intellectual pursuit, and so is an easy target for the philosophical striving for perfection.

With no necessarily real manifestation, and working in the realm of problems with infinite space for a variety of solutions, software development has, time and again, fallen victim to Plato's promise; i.e. that with the ideal design, and the right amount of time, we can deliver the perfect solution.

We can't. It's time to wise-up to that fact.

We've seen what happens when we do apply this philosophy; we even have a name for it. The idea that with the right design, and the right architecture, and the right amount of time we can deliver the right solution was the driving force behind what we would now retrospectively label as "Waterfall", or "Big, Up Front Design". An approach that guaranteed failure by building software on the assumption that perfect knowledge could ever be had. This is a mentality that has permeated everything from our processes, to our practices, to our project management, but the times they are a-changing.

	"No promise has been given you for this night - no, I have suggested too long a respite - no promise even has been given for this hour", Seneca the Younger[2]

TBD Picture of Seneca - If he could have built software, it would embrace change.

Software in its design and development has to consider something different, something a certain group of primarily Roman philosophers would have assigned a deity to called "Fortune". We'll simply refer to it as "Change".

Those philosophers were Stoics and their strongest position was that all things change (borrowed in fact from Heraclitis who famously said that you could "never step in the same stream twice"). "Reckon on Everything, expect everything" Seneca the Younger, one of the most famous of the classic Stoic philosophers  of the first Enlightenment, warned in his Premeditatium. A poetic way of saying "when it comes to reality, you don't know what is going to happen next, the best you can do is be prepared to react!".

Software does not live in a vacuum, or some rarified air reserved for philosophical and intellectual elites. Software is entirely useless unless it has some impact in the world, and in order for it to have an impact means that it needs to deal with the imperfect nature of reality.

In fact, software's position is worse than it first seems. Software not only has to interact with reality but of course is also affected in every sense by reality. Without hardware, and reality, software doesn't exist.

Agile Software Development made us a new promise. With agility, the aim was to be able to 'adapt', to be able to react to, embrace and even thrive on change, and even though we got bogged down in discussions around processes and principles the underlying thinking was the important thing. And it had changed fundamentally from the Platonic ideal. Software development was becoming pragmatically stoic. 

Our software has to consider change, both in terms of its design and its requirements as well as change at runtime.

Software developed that doesn't consider the vagaries, the oddness, the sheer unpredictability of reality will fall far short, time and again. Change is essential, so we need to embrace it in our software as well as in our processes and practices.

Good enough for now and able to change is the goal.

## Embracing Change Matters

Agile software development processes have asked us to consider change, and we’re getting fairly good at that. The problem is that our software has been left behind, still dwelling in the platonic assumption that ideal is possible and being built into a waterfall that is ready to swamp your need to change tomorrow.

What’s needed is an architectural style and some tools to help us build software that, at least, embraces as much change as our software processes do. There is plenty of work that could be done there with modularising monolithic applications along the lines of change and the “Life Preserver” pattern and tool that I invented and is described in the book “Antifragile Software: Building Adaptable Software with Microservices” can be used in just this way. However a monolith will always result in a monolithic deployment, and since a deployment is the unit of change for a production system it might be better to come up with something more granular, but that is also arranged along the important lines of change for an application.

This is where microservices come in, an architectural style that embraces change at both design and runtime and gives you the possibility to group and arrange services at the right level of granularity to deploy, failover and scale according to your needs.


## Embracing Change with Microservices

So what are microservices? Like many terms in our crazy industry, it’s a blurry statement and open to huge misrepresentation. I’ve worked now on what are commonly understood to be microservice-based software systems for around 4 years, long before the term moved into the common lexicon. More important than the term itself is the situations and constraints it has emerged to deal with, I call those properties the system’s “stressors”.

Stressors are forces that work on a given software system at design and runtime. Like weights being lifted by a muscle, a stressor can be dealt with, can break the system or, if considered carefully, can actually improve the system.

When it comes to microservices, and software systems in general, there are a subset of stressors that have the most impact and they are typically organised along two lines:

* Runtime
* Design-time

At runtime the stressors fall into three main categories: Wild Success, Wild Failure, Updating and Failure. 

Wild Success is where a software system becomes more popular than it was ever originally dreamed to be. Wild Failure is of course the cousin of Wild Success in that it labels when your system is underused, sometimes to the point of being a candidate for removal. Although it can seem that Wild Success is the only possibility that should be designed for, in fact both are equally important when it comes to making best use of the resources that you have. 

The Update stressor is the measure of how simply and easily an update can be performed to the system. Often regardless of whether a system is wildly successful or wildly a failure, it will come under the stress of needing to be updated.

The final runtime stressor is simply “Failure”. Not to be confused with Wild Failure, which is more a measure of the utility of a system. Simple failure is when bad things happen at runtime and your system comes under attack against its ability to function.

Design-time stressors fall into one clear category: Change. What happens when the natural force of change comes into contact with your design and architecture? When should you make the ‘big’ architectural decisions? Or can those decisions themselves be minimised in terms of their impact?

## Microservices, a Definition

It is within this framework of stressors that we can begin to define microservices. The key to a system that can embrace change is granularity and modularity of design, code and deployment.

With that in mind, here are the properties that commonly come under the banner of being a microservice:

> Single-purpose, simple (i.e. disentangled), autonomous and separately deployed services organised according to the change stressors on the system and that share nothing, especially state!

That’s it. No mention of Source Lines of Code (it’s not the 80s after all), and no mention of whether a service is an object or a function. No mention of whether the service is invoked synchronously or asynchronously using HTTP or something else. Those are detailed design decisions and there will be highly context-dependent reasons for choosing one option over another.

A microservice-based architecture is simply a one that contains microservices, with the devil in the details of how those simple microservices interact with one another while still supporting the runtime and design-time stressors. Microservices provides the right level of granularity to support change, but it is in the links between microservices that change needs to the be accommodated.

## Embracing or even Thriving on Change in the Links between Microservices 

The various design and runtime stressors are prepared for if you build a system of microservices, but the challenge then shifts into the links between services. 

For example, if you are going to deal with Wild Success, then microservices allow you to scale at the individual services that are most challenged by the shape of that success. Depending on how you’ve designed the incoming and outgoing connections from those services, you may still find that the scaling can be a challenge.

Currently the majority of microservice-based architectures use a simple selection approach to the links between services. The first-line choice is often to use HTTP, possibly RESTful and possibly asynchronous, as HTTP is a wonderful protocol for supporting many of the stressors that can be applied to those links. Second-line choice is usually some sort of messaging approach with a broker involved. Third-line, usually reserved for low-latency options, is to use something more bespoke that might require more effort to achieve the level of de-coupling between microservices to support the stressors being applied.

Embracing change and its stressors is an excellent starting point, and is the aim of designing your system using microservices. Finally we have an architectural approach that looks to embrace change on its own terms. 

You can go even further. You could design the links between services such that you can embrace change and for the majority of microservice-based systems that is good enough. It’s certainly a lot better than where we were. However if you go beyond that you can end up with a system that not only embraces change but in fact thrives on those stressors. A system that doesn’t just adjust but *improves* based on the stressors it encounters. This is where microservices provide the foundation of *antifragile* software systems.

Antifragile systems, as described by Nassim Nicholas Taleb in his excellent book “Antifragile: Things that Gain from Disorder”, are the opposite of “Fragile” systems. Different system can be arranged along a triad:

TBD Triad diagram

While fragile systems will collapse in the face of stressors, and robust/resilient systems will ideally ignore or be oblivious to those stressors, antifragile systems will embrace and *thrive* on those stressors, gaining from the presence of those stressors in the first place.

The best metaphor I’ve found is given by Taleb in his book and it likens an antifragile system to a muscle. When you go to the gym, you apply weight stress to the muscle and effectively convince the muscle that it had better be prepared for a world where gravity is much stronger. The muscle responds by improving itself into a stronger muscle with possibly ascetically pleasing side-effects.

This is often an extremely valuable effect to enable in our software systems. Imagine a system that didn’t just embrace design-time change but actually thrived and improved on it. Where wild success was a stressor that actually improved the emergent runtime architecture? Where wild failure simply results in the system adjusting things down to a minimum, like a muscle rarely being used taking less and less resources from the rest of the system.

Where I’ve seen this achieved a system provides a fertile landscape for innovation just not possible with a monolith. New languages and frameworks can be experimented with and applied on a service-by-service basis, reducing the risk of these so-called ‘big decisions’ to small decisions that use the objective measure of simplicity as guidance. 

So microservices are an excellent first step to embracing change, by looking at the links and the system as a whole you can even go as far as enabling antifragility and its powerful benefits as well. But what does a microservices architecture look like?

## Peers and Pipelines

The way that the parts of your system in a microservices-based architecture are organised is quite different from more traditional, SOA-labelled architectures. Rather than organising ‘macroservices’ according to somewhat arbitrary lines according to perhaps a typical ‘enterprise’ layered architecture, microservices are arranged in a flatter, peer arrangement:

TBD typical layered architecture.

TBD Picture of peers interacting in a microservices based architecture.

Those microservice peers work with one another to implement important data flows, and so the data flow actually becomes the unit of conversation when discussing features enabled by a microservices-based architecture rather than discussion around potentially complex hierarchical structure.

One layer of small hierarchy is sometimes introduced into a microservices-based architecture: the Explicit Pipeline Microservice. This is where the actual flow between services is extracted out into a microservice of its own that then simply captures the data flow, allowing the underlying microservices to be simplified in that they will have no knowledge of the flow that they participate in.

TBD Picture of extracted pipeline.

Not all microservice-based architectures feel the need to extract out explicitly microservice pipelines, however if it is done then the new pipeline microservices often become a convenient place to hook in management interfaces that produce actionable information about the data flows.

## Where does this leave the Architects?

In a microservices-based architecture there is the potential for every independent microservice to be implemented in any language/frameowkr combination that simplifies the service’s implementation. This leaves the choice of technology, even the choice of whether to construct ‘Reactive’ microservices, up to the teams and developers involved. These decisions used to be ‘high risk’ when they impacted an entire monolith, but in a world of rapidly evolving microservices that impact is transient and far lower risk.

So what decisions are left to the architects? What is the architects role in a microservices-based architecture?

The main job of the architect in a microservices-based architecture is to identify and optimise for the varied design and runtime stressors that are important within the given project or product context. The architect role should be looking at the breakdown of microservices to ensure that they are optimally granular for design-time change, and that there is adequate granularity to support the scaling and failover characteristics that are important at runtime to deal with their corresponding stressors.  At a minimum an architect will be looking to optimise for the following properties:

* Simplicity of the Microservices Design and Implementation
* Optimise for Change at Design and Runtime
* Optimise for Human Comprehension to ensure Humans are not the limiting factor on System Evolutiom (simplicity is a big contributor here)
* Antifragility where it is important for a system to thrive on a particular stressor’s presence

The architect of a microservices-based architecture is less concerned with language/framework/technology choice, and much more interested in the system-wore properties, fragile/robust/antifragile, that are important and works hard to ensure these are at the forefront of the minds of the developers and teams working on the system.

## Remember & Apply

I could have called this section “Summary”, but I thought I’d name it exactly after what I’d like you to do. So here are the key points from this article around microservices to take away:

* Change is an inevitable stressor on design-time and runtime in our software systems
* We need an architectural approach that embraces, possibly even thrives, on change
 * Microservices are: Single-purpose, simple (i.e. disentangled), autonomous and separately deployed services organised according to the change stressors on the system and that share nothing, especially state!
* A microservices-based architecture is more often a collection of peer services, possibly with a set of pipeline services, and asks you to focus on data flow rather than hierarchy.
* You can go beyond mere resilience and robustness to the benefits of antifragility with a microservices-based architecture.

## Where to go next?

Designing and building microservices-based architectures to embrace, and possibly thrive, on stressors such as change is not easy. First stop for more information would be to take a look at my book, ["Antifragile Software: Building Adaptable Software using Microservices"](https://leanpub.com/antifragilesoftware) available on LeanPub. 

As a side-note, the book has recently been discounted in-line with the amount of the book written during its development so its a good time to grab a copy to get future updates for free. Also 20% of the proceeds of the book are being donated to the [YoungMinds.org.uk](http://www.YoungMinds.org.uk) charity so you’ll be doing some good as well. 

For a deeper and more practical treatment of the subject you can check out my course ["Antifragile Software with Microservices"](https://skillsmatter.com/courses/498-antifragility) being run at Skills Matter.

Finally if you're in London in November and would like to learn how many different organisations are getting the most out of the benefits of microservices then attending the inaugural run of [µCon](https://skillsmatter.com/conferences/6312-mucon) is very much recommended.