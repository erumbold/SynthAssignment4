# SynthAssignment4

### Q1
Bubble sounds are essentially sinusoids that quickly decay, commonly with a rise in pitch as the bubble rises to the surface. There are two characteristics that are key to distinguishing bubbles from any other sinusoids. First, is the relation between the frequency ($f$) and damping ($d$) of the bubble sounds given by $$d = 0.043f + 0.0014f^\frac{3}{2}$$

The second characteristic to identify a bubble made near the surface is a rise in pitch. This frequency increase can be modeled as a function of time $$f(t) = f_0(1 + \sigma t)$$ where $f_0$ is the Minnaert frequency, or the frequency of a water drop falling into water, and $\sigma$ is the slope of the frequency rise.

### Q2
To replicate complex liquid sounds, a statistical approach is more appropriate because these sounds are comprised of multiple bubble sounds of various sizes, depths, and durations. Instead of a user needing to individually create 50+ bubble sounds, they can set just a few parameters within the bubble simulator presented in this paper to create a complete, complex liquid sound. This tool only calls for the range of bubble sizes, the average number of bubbles per second, the fraction of bubbles with rising pitch, and the distribution of the bubble population over the size range.


The creation of a bubble is modeled as a Poisson process, meaning the average time between events (bubble creation) is fixed, but the actual timing of these events is random. Sounds like rain and other water phenomena are not uniform; two rain drops in water may not sound like each other, and the time between two rain drops isn't always the same. A Poisson process is well suited to recreate this relation.
