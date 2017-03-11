+++
title = "Boolean algebra and adaptive programs"
id = 36
categories = ["Outreach"]
date = "2015-09-13 15:34:56"
tags = []
menu = ""
banner = "images/boole.jpg"
+++

If you have any experience of programming, you probably know that interactive programs rely on testing conditions and acting according to the outcomes.

If not, imagine programming a self-driving racing car. If you give it a predetermined set of instructions, it might be able to drive itself on a given racing circuit. However, you are going to run into a wall if you put that car on another circuit (literally), or if you add other cars to the circuit.

![](/images/carcrash.jpg "Ferrari Kiss by Valentini.antoine") <small>Photo by [Valentini.antoine](http://www.flickr.com/photos/47918183@N04/9129393830) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by-sa/2.0/ "Attribution-ShareAlike License")</small>

In order for a program to be robust and able to adapt to its environment, it needs to check its state and the state of its environment (e.g.: is there a car ahead? If so, am I driving faster than it?) and act accordingly (e.g.: overtake it or just keep driving normally).
<pre>if {there is a car ahead} and {I am faster}:
    {I overtake it}
else:
    {I keep driving normally}</pre>
This holds for computer programs, but also for biological programs. Let's take the example of plants. If you have plants, you might have noticed that they have a tendency to grow towards the light. This is particularly striking if you have a potted plant on a window sill.

![](/images/phototropism.jpg "dsc_2948.jpg by r_neches") <small>Photo by [r_neches](http://www.flickr.com/photos/66777430@N00/2081938105) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by/2.0/ "Attribution License")</small>

Their program is something like:
<pre>if {I am growing towards the light}:
    {I keep growing}
else:
    {I bend towards the light}</pre>
In the EpiTraits project, I am working on something a little different: the control of flowering. Still, it can be summarized in a similar way:
<pre>if {days are long} and {the cold weather is over}:
    {I make flowers}
else:
    {I make leaves}</pre>
![](/images/flower.jpg "White Flower by Jeff Kubina") <small>Photo by [Jeff Kubina](http://www.flickr.com/photos/95118988@N00/8156603) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by-sa/2.0/ "Attribution-ShareAlike License")</small>

You might have noticed that, in both computer and biological programs, the conditions we want to test for may be composed of several sub-clauses:

*   {there is a car ahead} and {I am faster}
*   {days are long} and {the cold weather is over}
These are examples of Boolean algebra. Boolean algebra deals with variables that are either True or False, and the operations used to combined them, which include "and" (as seen above), "or", "not", and all combinations of the above.

If we consider two statements A and B:

*   (A and B) is true if and only if both A and B are True
*   (A or B) is true if and only if A is True, B is True, or both are True
*   (not A) is true if and only if A is False.
As you can see, "and" and "or" are binary operators, and "not" is a unary operator.

However, it is possible to use them to combine an arbitrary number of statements into a single statement. For instance, with 4 statements A, B, C and D, we could have:

(A and B) or (C and (not D))

Biological applications of Boolean algebra include Boolean models of Gene Regulatory Networks. Indeed, biological programs result from the coordinated expression of genes that regulate each other, so the activity of a gene can be described using Boolean algebra.

In the flowering example I mentioned above, the gene that represents flowering is SOC1\. It is activated by a day-length dependent gene, FT, and repressed by FLC, a gene that is itself repressed when the temperature is low.

We therefore have:
<pre>FT = {daylength is long}
FLC = {winter is not over}
SOC1 = FT and (not FLC)</pre>
SOC1 is on if FT is on and FLC is off.

We can do this for any gene of interest. The end result is a model able to predict the evolution of a biological system based on the inputs of the model (here, how long days are, and whether winter is over or not).

![](/images/crocus.jpg "Snowy Crocus by Red Junasun") <small>Photo by [Red Junasun](http://www.flickr.com/photos/41994050@N07/6823430303) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by/2.0/ "Attribution License")</small>

<small>Banner photo by [OpenPlaques](http://www.flickr.com/photos/39377065@N08/6921390393) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by/2.0/ "Attribution License")</small>