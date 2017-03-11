---
title: "Differential equations"
id: 47
categories:
  - Outreach
date: "2015-09-13 16:36:26"
banner: "/images/integration.jpg"
---

If you read the post about [Boolean algebra](https://jldinh.com/2015/09/13/boolean-algebra-and-adaptive-programs/), you might have noticed a substantial limitation: it can only deal with binary (True/False) variables.

How, then, can you make predictions for quantitative variables? You probably already know the answer.

If you are going to the seaside by car, the seaside is 100 km away, and you are driving at 50 km/h, how long will it take you to reach the seaside?

![](/images/drive_river.jpg "Endless Possibilities by Zach Dischner") <small>Photo by [Zach Dischner](http://www.flickr.com/photos/35557234@N07/11533326155) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by/2.0/ "Attribution License")</small>

2 hours, of course.

To introduce a new tool - differential equations - here is another way to see the problem.

Let $x$ be your position on the way to the seaside. $x=0$ is the starting point, $x=100$ is the arrival.

Your speed is the rate of change of $x$, denoted as $\frac{dx}{dt}$.

$$ \frac{dx}{dt}=50$$

This is a differential equation. It describes the rate of change of a variable. This example is simple, because the differential equation is constant, but it could potentially be more complex and depend on your current position, e.g.:

$$ \frac{dx}{dt}=100-\frac{1}{40}(x-50)^2$$

![](/images/eqdiff.png)

Even if the differential equation is complex, you can still use it to plot the state of the system (e.g.: your position) at any instant in the future. This is what makes differential equations powerful.

This is a process called "numerical integration", and is generally handled by dedicated computer programs, but the idea is quite simple:

1.  Check your current position in the simulation.
2.  Compute your current speed.
3.  Compute how far you are going to travel at that speed in one second.
4.  Add the result of step 3 to the value observed at step 1.
5.  Update your current position in the simulation based on the result of step 4.
6.  Go to step 1 and repeat.
You then just have to look at when $x$ becomes greater than 100 to know when you will arrive.

![](/images/beach.jpg "Lano Beach by NeilsPhotography") <small>Photo by [NeilsPhotography](http://www.flickr.com/photos/21976354@N07/2348897751) ![](/images/cc.png#cc "Attribution License")</small>

<small>Banner photo by [Internet Archive Book Images](http://www.flickr.com/photos/126377022@N07/14596416049) </small>