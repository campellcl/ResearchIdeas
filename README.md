# Research Ideas
My collection of general avenues and potential research directions in the AI/ML space that personally interest me.

Some people have a book of business ideas, whereas I have a "book" of research ideas. Here it is. 

## General Process
I will start by dumping my research ideas in this document as I formulate them. As the list of research ideas
grows, I will start segmenting this README document into separate fields/areas of interest. Naturally, some ideas
that I propose in this document will be either: a) not feasible, b) already sufficiently investigated, c) poorly defined/scoped. 
There will be a natural process of refinement that will look something like this:
```
Research idea/whim -> brain storming -> literature review -> concrete hypothesis -> testable experiment -> implementation
```  
Don't expect all ideas you find in this document to be in the final stages (e.g. well formulated testable experiments).
This document is public facing in case anyone has any interesting contributions (although they are surely not anticipated,
they are welcome). This document is not public facing because I believe it has evolved to a level of maturity that would warrant 
peer review, or public exposure; it hasn't. Do not expect everything this document to be developed to the point that I 
would personally deem worthy of suggesting to an interested collaborator. In short, do not judge me for any half-formulated
thoughts presented herein. Judge me instead by my final research project formulations and proposed research experiments/implementations.  

## General Research Ideas:
### Inspiration: 
I have been watching the excellent [Lex Fridman Podcast](https://lexfridman.com/podcast/) which features hours of 
interview footage with experts and leading researchers in the field of Machine Learning. I have been attempting to 
assemble a dossier on the opinions and research directions by these famous researchers (which you can follow [here](https://github.com/campellcl/DeepMinds.git)), in order to inspire new novel
directions of research. The idea is that, if there is some overlap among proposed avenues of research by the best minds
in the field, those areas of research may warrant special consideration. An ancillary to this, is that such conversations
may serve to inspire new novel directions of research by identifying unsolved questions that frequently arise during these
interviews.

### Alternate Learning Processes for Neural Networks:
#### The General Ideas:
##### The Method of Learning: Alternative to Back-propagation? 
There is an increasing disillusionment among the "great minds of deep learning" with our current neural network training
processes. The "Godfather of Deep Learning" Geoffrey Hinton has famously said:
> My view is throw it all away and start again. Max Planck said: "Science progresses one funeral at a time". The future
> depends on some graduate student who is deeply suspicious of everything I have said. -[Dr. Geoffrey Hinton (Axios Interview)](https://www.axios.com/artificial-intelligence-pioneer-says-we-need-to-start-over-1513305524-f619efbd-9db0-4947-a9b2-7a4c310a28fe.html)

Hinton suggests that to approach human-level intelligence via unsupervised/self-supervised learning, that:
> I suspect [this] means getting rid of back-propagation. I don't think it's how the brain works. We clearly don't need
> all the labeled data. -[Dr. Geoffrey Hinton (Axios Interview)](https://www.axios.com/artificial-intelligence-pioneer-says-we-need-to-start-over-1513305524-f619efbd-9db0-4947-a9b2-7a4c310a28fe.html)

There are some ([noteably Dr. Ilya Sutskever](https://youtu.be/13CZPWmke6A?t=2480)) who disagree with this, and think that
back-propagation is here to stay because of its utility, irrespective of whether or not we find out that a similar 
mechanism exists in the brain. Similarly, to Dr. Ilya Sutskever, Dr. Yann LeCun seems particularly fond of gradient-based learning, irrespective of whether or not more
biologically inspired processes exist: 
> Another question is all of our... models of what reasoning is, that are based on logic, are discrete and therefore incompatible
> with gradient-based learning. I was a very strong believer in this idea of gradient-based learning. I don't believe in other
> types of learning that don't use, kind of, gradient information, if you want. -[Yann LeCun (Lex Fridman Interview)](https://youtu.be/SGSOCuByo24?t=679)

When asked about the biological process of learning via synaptogenesis in relation to the ANN approach of back-propagation, Jeff Hawkins responded:
> It [synaptogenesis] is even easier [than backpropagation]. **Back-propagation requires something that really can't 
> happen in brains, this back-propagation of an error signal.** Synaptogenesis is pure Hebbian learning. - [Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=5677)

This suggests that there may be other alternatives which are computationally feasible to implement, in the way that 
back-propagation has been computationally feasible to implement via the medium of automatic differentiation.

However three of these researchers appear to agree on two ideas: 
1. The implementation of the learning process in the biological brain most likely does not employ back-propagation of 
error signals, or any similar-typed mechanism.
2. There exist alternative learning processes other than back-propagation that are worth investigating.

##### The Cycle of Learning: Recurrence, Open-Endedness, and Continuous Learning:
Another key difference between the human brain and modern day ANNs is the continuity of the learning process itself,
irrespective of the actual method of learning which it employs. 

On this topic, Jeff Hawkins says the following:
> Brains are continuously learning [there is no separate learning and inference stage]. That is not something we said 
> "oh we can add that later". That is something that was upfront and had to be there from the start. **Our brains infer 
> and learn at the same time**. Our [Numenta's] models do that, and they're not two separate phases. 
> -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=5276)

He goes on to say:
> There are cycles of activity in the brain and there is very strong evidence that you're doing more of inference in one part
> of the phase, and more of learning in the other part of the phase. So different populations of cells are going back-and-forth
> like this. But in general I would say that's an important problem we have. **All of [Numenta's] neural networks do both,
> they are continuous learning networks.** -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=5276)

On the topic of potential essential ingredients for a human-level learning system,  Yann LeCun says:
> Another thing you need is some sort of network that can access this memory, get an information back, and then kind of
> crunch on it, and then do this iteratively multiple times. **Because a chain of reasoning** is a process by which you update
> your knowledge about the state of the world, about what's going to happen, etc., and that **has to be this sort of
> recurrent operation basically**. -[Yann LeCun (Lex Fridman Interview)](https://youtu.be/SGSOCuByo24?t=896)

While Ilya Sutskever states

##### An Evolutionary Approach to Open-Endedness
https://www.oreilly.com/radar/open-endedness-the-last-grand-challenge-youve-never-heard-of/
##### Learning with Less Labeled Samples:

In addition to the distinction between the separate learning and inference cycles that are found in modern artificial
neural networks, another key difference between the human brain is the number of labeled training samples required
to achieve a good identification accuracy on a specific task. This can be summed up rather simply: humans learn
much more quickly than neural networks do. Whereas humans need only a couple labeled (supervised learning) samples, our
best machine learning algorithms need as many as 10-to-100 times as many labeled training samples. 

Speaking to this, Hawkins reiterates:
> In the brain the way learning occurs... Imagine I am a section of the dendrite of a neuron, and I am going to learn 
> something new (recognize a new pattern). I'm going to form new synapses, rewire the brain onto that section of the dendrite.
> Once I have done that, everything else that neuron has learned is not affected by it [the new wiring]. That's because
> it's isolated to that small section of the dendrite. **They are not all being added together like a point neuron.** If
> I learn something new on this segment here, it doesn't change any of the learning that occurs anywhere else in that neuron. 
> So, **I can add something without affecting previous learning, and I can do it quickly**. The idea of synaptogenesis 
> (the growth of new synapses) that is well described and understood, [that] *is* learning.  -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=5433)


The importance of active learning or learning by self-play?


### Biologically Inspired Neural Network Architectures:
### The General Idea:
Jeff Hawkins has said:
> Real neurons in the brain are time-based prediction engines, and there is no concept of this at all in artificial, 
> what we call, point neurons [which artificial neural networks leverage]. **I don't think you can build the brain without them. I don't think you can build intelligence
> without them.** -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=4142)

In the real brain time plays a much more important role than it does in our current neural network architectures:

> I would say that point neurons sort of model a piece of that [the importance of time], and not very well at that either.
> For instance, synapses are very unreliable. You cannot assign any kind of precision to them, even one digit of precision is
> not possible. The way real neurons work, is they don't change these [synaptic] weights accurately like artificial neural 
> networks do. They basically form new synapses. So what you are trying to always do, is detect the presence of some 10 to 20
> active synapses [firing] at the same time. In real neurons the synapses are almost binary, because you can't really represent 
> anything finer than that. I think that is another essential component because the brain works on sparse patterns. -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=4174)

Jeff Hawkins has said (in regards to our current deep learning architectures):
> The first thing we've [Numenta] done is focus on the sparse representations in the brain. In the brain if I have like 10,000
> neurons, what you would see is maybe 2% of them active at a time. You don't see 50%, you don't see 30%, you might see 2%, and
> it is always like that in any part of the brain. -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=4652)

> The way the representations occur in the brain, it is always a sparse representation. It is a population code. **So 
> which 200 cells are active tells me what's going on. Individual cells are not that important at all, it is the 
> population code that matters.** The brain uses sparse population codes, we've written and described the benefits
> of [using such sparse codes] in some of our papers. They give this tremendous robustness to the system. We've shown that if
> you enforce sparseness in convolutional neural networks in both: which neurons are active, and the connections between them,
> you get some very desirable properties. -[Jeff Hawkins (Lex Fridman Interview)](https://youtu.be/-EVqrDlAqYo?t=4686)

Jeff Hawkins and his team at Numenta have shown that if you enforce sparse representations (in the firing and 
connections between neurons) in convolutional neural networks, the networks have increased robustness to adversarial
attacks. The research being done at Numenta tries to come up with incremental ways of moving brain theory into machine
learning. Their next goal ([according to Hawkins](https://youtu.be/-EVqrDlAqYo?t=4931)) is to incorparate some of the
ideas of [*The Thousand Brains Theory of Intelligence*](https://numenta.com/blog/2019/01/16/the-thousand-brains-theory-of-intelligence/) into machine learning. 

> A real neuron in the brain is a complex thing. Real neurons can have anywhere from five to thirty thousand synapses 
> on it. The [synapses] that are close to the cell body (the soma) these are like the ones that people model in artifical
> neurons. There [are] a few hundred of those maybe, they can affect the cell, [and] they can make the cell become active. Ninty
> five percent of the [other] synapses can't do that, they are too far away. If you activate (even a mass) of these synapses it 
> just doesn't effect the cell body enough to make any difference. -[Lex Fridman Interview](https://youtu.be/-EVqrDlAqYo?t=3970)

> What real neurons do is the following: If you get 20 synapses or 40 synapses active (all receiving an input) at the 
> same time, and within a very short distance on the dendrite (like 40 microns, or a very small area) what happens is it
> creates what is called the dendritic spike. The dendritic spike travels through the dendrites and can reach the soma 
> (or the cell body). When it gets there it changes the voltage enough to almost make the cell fire, but not enough to 
> make it fire. It's what we call depolarizing the cell, you raise the voltage a little bit but not enough to do anything.

> We proposed a theory... the basics are: what's happening there is that ninety-five percent of those synapses are 
> recognizing dozens to hundreds of unique patterns. These 20 to 40 [active] synapses are acting like predictions. **The
> neuron actually is a predictive engine on its own**. It can fire when it gets enough of what they call approximate input
> (from when those [dendrites] near the cell fire), but it can get *ready to fire* from dozens-to-hundreds of patterns
> that it recognizes from the other guys. The advantage of this to the neuron is that, when it actually does produce a
> spike in action potential, it does so slightly sooner than it would have otherwise. 

> Well what good is slightly sooner? All of the excitatory neurons in the brain are surrounded by inhibitory neurons. The
> inhibitory neurons are very fast (these basket cells). If I (as a neuron) get my spike out a little bit sooner than someone
> else, I inhibit all my neighbors around me. What you end up with is a different representation. You end up with a representation
> that matches your prediction. It's a sparser representation (meaning much fewer neurons are active) but it's much more specific.
> Networks of these neurons can do very specific temporal predictions.  

> Real neurons in the brain are time-based prediction engines, and there is no concept of this at all in artificial, 
> what we call, point neurons. I don't think you can build the brain without them. I don't think you can build intelligence
> without them. -[Lex Fridman Interview](https://youtu.be/-EVqrDlAqYo?t=4142)

Likewise OpenAI's Ilya Stuskever, when asked: "Is there other things about the brain that pop into your mind that might be 
different or interesting for us to consider in designing artificial neural networks?" responded with:
> I mean one thing which may potentially be useful, I think neuroscientists figured out something about the learning
> rule of the brain: I'm talking about [spike-timing dependent plasticity](https://en.wikipedia.org/wiki/Spike-timing-dependent_plasticity) 
> it would be nice if some people were to study that in simulation. -[Ilya Sutskever (Lex Fridman Interview)](https://youtu.be/13CZPWmke6A?t=733)



#### Multi-Modal Learning in ANNs:
