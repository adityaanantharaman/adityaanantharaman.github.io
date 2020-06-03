---
layout: post
title: Algorithms In Nature [Part-1]
---
_Simulating birds flocking_

![](/images/boids/boids1.jpg)

Have you ever wondered how flocks of birds fly in such a synchronous manner? Making these complex but clean shapes along the way, all while not bumping into each other and creating havoc. It is difficult to imagine that such **“sync”** can be achieved without choreography or practice. But birds definitely haven't been found practicing to fly in sync. At Least not that I've heard of.

Then how is it that such complex behaviour and seemingly choreographed and smooth movement can be observed when birds fly? The answer: Algorithms in Nature

![](/images/boids/boids2.jpg)

Algorithms are present all throughout nature and can be seen if one simply observes. A flock of birds flying with sync, a shoal of fish moving and avoiding predators, fireflies flashing in sync, ants moving in complex paterns etc. are all examples of something called **emergent behaviour**.

Emergent behaviour is when all the individual elements in a scene follow a set of simple rules and this in turn gives rise to a surprisingly complex behaviour of the group of elements as a whole. 

In the case of the flocking birds, the simple rules are:
1. Try moving in the same direction
2. Stick together
3. Don't fly into each other 

The bird flocking algorithm or boids algorithm is an artificial-life algorithm that was created by Craig Reynolds in 1986. Each of the boids or bird-oids follow just 3 simple rules and what results is this complex and seemingly choreographed movement of the flock as a whole. What’s surprising, is the fact that each of the individual birds decides its actions only considering the few birds within its **local perception radius**. 

The 3 simple rules, in a programmable sense, are:
1. **Alignment** : each bird attempts to move in the average direction of the birds within its perception radius. 
2. **Cohesion** : each bird attempts to move towards the average position of the birds within its perception radius.
3. **Repulsion** : each bird attempts to move away if it gets too close to any of its neighbours.

By making each of the boids/bird-oids follow these simple rules, what emerges is this complex movement of flocks making turns, avoiding obstacles, and merging with other flocks, all of which has not been explicitly programmed. 

Although I learnt about the emergent behaviour that arises, seeing it in action was surprising and scary at the same time. In the process of coding this simulation, I spent a good hour or two, just observing the movement of these boids and drawing obstacles of different shapes and sizes and experimenting with different levels of alignment, cohesion and repulsion. Something about this kind of emergent behaviour is magical. So I would suggest you to turn down all the 3 rules completely using the **sliders**, and then see how each rule affects the flock one by one. The **Draw** button can be turned on to draw obstacles on the screen. The **walls** button enables boundaries, which the boids sense, and move away from. The **shape** button changes the shape of the boids.

**Here’s the simulation I made using P5.js**

[**Boids Simulation**](http://adityaanantharaman.github.io/boids)

![](/images/boids/boids3.jpg)

Here’s the link to the github repo:
[Boids Repository](https://github.com/adityaanantharaman/boids)

There are a lot of parameters in play, the most important being the perception radius, max_speed and max_force. By tweaking the above parameters, different emergent behaviours can be observed. 
 
**References:**
Here are some blogs and videos that got me interested in the topic of emergent behaviour.
1. [smarter everyday video on boids algorithm](https://www.youtube.com/watch?v=4LWmRuB-uNU)
2. [Craig Reynolds' official blog post](https://www.red3d.com/cwr/boids/)
3. [coding Train video on simulating boids](https://www.youtube.com/watch?v=mhjuuHl6qHM&vl=en)



