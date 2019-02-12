---
layout: post
title: Lightning strike + short attention span = brief math musing
excerpt_separator:  <!--more-->
---

![Me]({{ "/assets/images/lightning.gif" | absolute_url }})

### Problem statement

While browsing Reddit last week, I stumbled upon a relatable GIF. There was a girl staring out her window at a storm, apparently waiting for lightning. Just as she turns around to complain about the lack of lightning, immediately behind her, of course, the lightning strikes (a watched storm never thunders?). The setup reminded me of geometric probability questions from math-contests-past, and I felt like working out something concrete. The question, in a generalized form: 

The girl will watch for the lightning over an $$ n $$ second interval. The lightning strike lasts $$ x $$ seconds, and will strike at a random time in the $$ n $$ second interval. The girl will look back for $$ y $$ seconds at a random time during the $$ n $$ second interval. What are the chances that she misses the lightning strike?

### Basic technique

The idea here is similar to a bus-stop problem the I remember. There's a man who needs to catch a bus. He will arrive at the stop for a random five minute period within an hour, and wait for 10 minutes. The bus will arrive at the stop at a random time in the hour and wait for 5 minutes. What are the chances he catches the bus?

For me anyways, this was a tough one to approach. Let's throw it on a graph and make it clearer! Dropping the time for the man's arrival on the $$ x $$ axis and bus arrival on the $$ y $$, we get this:

![Me]({{ "/assets/images/bus-diagram.jpg" | absolute_url }})

The cross-section in the middle represents the times that the man will catch the bus. Now, we've turned this into a geometry problem. If we consider this a $$60$$x$$60$$ square, then then we have a $$50$$x$$50$$ isosceles right triangle on the top, and a $$55$$x$$55$$ isosceles right triangle on the bottom. Therefore, chances of him catching the bus should be:

$$ \frac{3600-\frac{50*50}{2}-\frac{55*55}{2}}{3600} = \frac{3600-1250-1512.5}{3600} = \frac{837.5}{3600} \approx 0.23 $$


### Generalization

Here, we can use the same exact principle from before. There's really not a single difference in it's application to the lightning problem as I laid it out.

The total area of the region will again be $$ n^2 $$ units. The region carved out will be $$ \frac{1}{2}((n-x)^2 + (n-y)^2) $$ 

Therefore, the overall odds of her **missing** the lightning should be:

$$ 1 - \frac{(n-x)^2 + (n-y)^2}{2n^2} $$


### Further thoughts

It would be more interesting to delve into complications of the problem. For example, what if rather than it being an equal chance to look back at a given time, there is some known, continuous function that describes both the chances for a lightning strike at a given instant, and the chances for the girl to look back? What if the lightning can strike more than once in the interval?